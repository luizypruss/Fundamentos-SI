### GUIA COMPLETO CRIAÇÃO DOCKER

## 1. O que é Docker?
O Docker é uma tecnologia de virtualização a nível de sistema operacional. Ao contrário de uma Máquina Virtual (VM) tradicional, que precisa de um sistema operacional inteiro para cada instância, o Docker compartilha o núcleo (kernel) do sistema operacional hospedeiro. Ele empacota o código do seu aplicativo junto com todas as dependências (bibliotecas, variáveis de ambiente) em um único arquivo chamado Imagem. Quando essa imagem é executada, ela se torna um Contêiner isolado e leve.

## 2. Para que usar o Docker?
Fim do "Na minha máquina funciona": Garante que o sistema rode exatamente igual no Windows de desenvolvimento e no Ubuntu de produção.
Isolamento total: Permite rodar diferentes versões de Python ou bancos de dados na mesma máquina sem conflitos.
Portabilidade ultra-rápida: Facilita migrar o aplicativo entre computadores ou servidores em poucos minutos.
Instalação simplificada: Você não precisa instalar Python, PostgreSQL ou Redis diretamente no seu Windows.
## 3. Passo a Passo: Configuração Local (Windows) com Python-Django

# Requisitos Iniciais no Windows

- Baixe e instale o Docker Desktop para Windows.
- Certifique-se de ativar o recurso WSL 2 (Windows Subsystem for Linux) durante a instalação, pois o Docker no Windows depende dele.
- Abra o terminal (PowerShell ou Prompt de Comando) e verifique se foi instalado corretamente:
docker --version docker-compose --version

Criando a Estrutura do Projeto Django 
Crie uma pasta para o seu projeto no Windows (ex: meu-projeto-django) e monte a seguinte estrutura de arquivos básicos: 

meu-projeto-django/ 
├── Dockerfile 
├── docker-compose.yml 
├── requirements.txt (ARQUIVOS OBRIGATÓRIOS)
└── (O código do seu projeto Django ficará aqui dentro)

# Passo A: Criar o arquivo requirements.txt Adicione as dependências básicas do seu projeto:

Django>=5.0 gunicorn

# Passo B: Criar o arquivo Dockerfile O Dockerfile é a receita para construir a imagem da sua aplicação.

Usa uma imagem oficial do Python adaptada para Linux leve
FROM python:3.11-slim (UTILIZA A VERSÃO MAIS LEVE DO PYTHON, MAS ISSO É OPCIONAL, VOCÊ PODE CRIAR VÁRIAS VERSÕES)

- Define o diretório de trabalho dentro do contêiner
WORKDIR /app

- Evita que o Python grave os arquivos .pyc no disco
ENV PYTHONDONTWRITEBYTECODE 1

- Evita que o Python faça buffer das saídas stdout e stderr
ENV PYTHONUNBUFFERED 1

- Instala as dependências do sistema
RUN apt-get update && apt-get install -y --no-install-recommends gcc libpq-dev && apt-get clean

- Copia o arquivo de requisitos e instala as dependências do Python
COPY requirements.txt /app/RUN pip install --no-cache-dir -r requirements.txt

- Copia todo o restante do código do computador para o contêiner
COPY . /app/

- Expõe a porta padrão que o Django/Gunicorn vai rodar
EXPOSE 8000

- Comando padrão para iniciar o servidor de desenvolvimento
CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]

# Passo C: Criar o arquivo docker-compose.yml O Compose gerencia múltiplos contêineres (como sua aplicação + banco de dados) de forma simplificada.

version: '3.8' services: web: build: . command: python manage.py runserver 0.0.0.0:8000 volumes: - .:/app ports: - "8000:8000" environment: - DEBUG=1

# Passo D: Iniciar o projeto Django

Com o Docker Desktop aberto, execute o comando abaixo no terminal do Windows para gerar o código inicial do Django através do próprio contêiner:

docker-compose run web django-admin startproject meu_projeto .

(Note o ponto . no final para criar na pasta atual).

# Passo E: Rodar a aplicação localmente

Agora basta subir o contêiner:

docker-compose up

Abra o navegador no Windows e acesse http://localhost:8000. O Django estará rodando perfeitamente de dentro do Docker.

## 4. Passo a Passo: Levando para o Servidor Ubuntu
Para mover o projeto para produção, a prática moderna e recomendada é utilizar o Docker Hub (um registro de imagens online gratuito).

No Windows (Preparando e Enviando)
Crie uma conta gratuita no Docker Hub.
No terminal do Windows, faça login na sua conta:
docker login

Construa a imagem de produção da sua aplicação (altere o arquivo Dockerfile se necessário para usar gunicorn em vez de runserver):
docker build -t seu_usuario_dockerhub/django-app:latest .

Envie a imagem construída para o Docker Hub:
docker push seu_usuario_dockerhub/django-app:latest

No Servidor Ubuntu (Baixando e Executando)
Acesse o seu servidor Ubuntu via SSH.
Instale o Docker no Ubuntu rodando:
sudo apt update sudo apt install docker.io docker-compose -y sudo systemctl start docker sudo systemctl enable docker

Crie uma pasta para o projeto no servidor e crie apenas o arquivo docker-compose.yml de produção dentro dela:
version: '3.8' services: web: image: seu_usuario_dockerhub/django-app:latest ports: - "80:8000" environment: - DEBUG=0 restart: always

(Note que alteramos o mapeamento de porta para 80:8000 para que o servidor responda diretamente na porta padrão da web).

Baixe a imagem e execute o projeto no servidor em segundo plano (modo detached):
sudo docker-compose up -d
