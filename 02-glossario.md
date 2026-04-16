# Glossário ou vocabulário da disciplina
Neste arquivo, são armazenadas palavras ou expressões estudadas na disciplina, com uma breve descrição delas

## Palavras ou expressões
  - <b>ARQUITETURA DE COMPUTADORES</b>: Em termos simples, é o projeto conceitual e a estrutura operacional que define como os componentes de hardware (processador, memória, entrada/saída) se interconectam e funcionam para executar instruções.
  - <b>SISTEMA</b>: conjunto de elementos que interagem entre si em prol de solucionar e fazer funcionar um esquema.
  - <b>MODELOS ARQUITETURAIS DE SERVIÇO</b>: Tudo é nuvem, serviços que estão em outro lugar, serviço contratado.
    
    - **DaaS:(Desktop as a Service)** Desktop virtual Computador virtual na nuvem, acesso ao PC  de forma remota, não precisa instalar nada.
      Exemplo de aplicação: Microsoft Windows 365, Amazon Web Services WorkSpaces.
      
    - **DBaaS:(Database as a Service)** Banco na nuvem- Banco de dados na nuvem pronto para usar. Criar banco sem instalar MySQL no computador. 
    Exemplo de aplicação: MongoDB Atlas

    - **FaaS: (Function as a Service)** Funções na nuvem- Envia apenas funções, elas executam quando necessário. Apessoa controla a lógica e as fuções. (Firewall)
    Exemplo de aplicação: Amazon Web Services Lambda

    - **IaaS: (Infrastructure as a Service):** Máquina virtual-  O provedor te entrega uma máquina virtual "limpa/crua". Você tem acesso via SSH, escolhe o Linux, instala o Docker, configura o Firewall e o IP manualmente. Você é a Administradora de Sistemas. **Recursos**(CPU, RAM, Disco, Rede)
    Exemplos de aplicações: Google Cloud Compute Engine.

    - **PaaS: (Platform as a Service)** Plataforma pronta- Essa arquitetura de software, ela oferece toda a infraestrutura (servidores, sistemas e banco de dados) para o programador focar apenas no desenvolvimento do código, é a camada **intermediária** que remove a complexidade de configurar máquinas só injeta somente a lógica de negócio (código) e os dados. Você apenas faz o "Upload" do código, a plataforma decide em qual máquina o código vai rodar e como a rede será isolada, é como construir um resteurante mas ele já vem imobiliádo. **Workflow** (Build, Deploy, Escalonamento) 
    Exemplos de aplicações: Google Cloud App Engine e Microsoft Azure App Service

    - **SaaS: (Software as a Service)** Software pronto- O software já está pronto, você só usa, sem instalar nada. Importante é que se não pagar não tem acesso mais.
    Exemplos de aplicação: Netflix e Spotify.

    - **SECaaS:(Security as a Service)** Serviços de segurança na nuvem. Proteger site contra ataques.
    Exemplo de aplicação: Cloudflare e Kaspersky. 
    - **CaaS:** Conteiners, máquinas virtuais em forma de software dentro de outra. "Compartilha hardware" no mínimo 16GB- 8GB DE RAM
    Exemplos de aplicação? VitualBOX da Oracle.

    ## **Tipos de Sistema de Informação**
    - Sistemas de Processamento de Transações (TPS)
Registram e processam operações rotineiras do dia a dia (ex: vendas, pagamentos).

    - **Sistemas de Informação Gerencial (SIG)**
Transformam dados em relatórios para auxiliar gestores no controle e planejamento.

    - **Sistemas de Apoio à Decisão (SAD)**
Ajudam na análise de dados complexos para decisões estratégicas.

    - **Sistemas de Apoio Executivo (ESS/EIS/SAE)**
Fornecem informações resumidas e estratégicas para altos executivos. (Análise de clientes, dashboard)

    - **Sistemas de Automação de Escritório (SAE)**
Facilitam tarefas administrativas (e-mails, documentos, agendas). 

    - **Sistemas de Gestão do Conhecimento (SGC)**
Armazenam e compartilham conhecimento dentro da organização.
(Problemas podem acontecer quem resolveu e como resolveu, normalmente há um portal)

    - **Sistemas Empresariais (ERP)**
Integram diferentes áreas da empresa (finanças, RH, produção) em um único sistema.

    - **Sistemas Especialistas / Inteligentes**
Utilizam regras e inteligência artificial para resolver problemas específicos.

    - **Sistema CRM (Customer Relationship Management)** 
    Uma plataforma de gestão de relacionamento que centraliza dados de clientes, interações, vendas e marketing em um único local, em forma mais simples, o software de CRM ajuda a gerenciar, com eficiência, as informações que coletou sobre seus clientes, conhece o cliente. 
    Sistema de 

## *Exemplos:*
- Minha Agenda UFN:
Sistema OAS (Automação de Escritório)
Função: Organizar compromissos acadêmicos (aulas, provas, tarefas)
Automatiza rotinas administrativas do estudante facilita comunicação e organização
Atua no nível operacional, ajudando no dia a dia dos usuários.

- Sistema de Imposto de Renda (Receita Federal)
Tipo principal: TPS + MIS
Função: Receber, processar e analisar declarações fiscais
Processa milhões de declarações (transações) todo ano
Gera dados para controle e fiscalização do governo
Classificação: TPS + MIS

- CRUD:  Gerenciando Etapas, quatro operações fundamentais realizadas sobre dados em qualquer aplicação de software.  Create (Criar), Read (Ler), Update (Atualizar) e Delete (Deletar) 

- *Throughput de Rede*   Seria o volume médio de *dados* que podem realmente passar pela rede em um período específico. Em outras palavras, throughput nada mais é do que uma medida de requisições realizadas com sucesso por unidade de tempo.
- Latência:  tempo  que leva para resposnder. (Vemos isso no PING)

## Internet das Coisas
  - IoT: são as redes dos dispositivos físicos que se conectam e trocam de dados através da internet. Conecta dispositivos do dia dia para facilitar a comunicação, interação e integra à internet. Com isso eles transmitem dados a partis da nuvem.
  Isso muda como as pessoas lidam com dados e interagem com dispositivos, facilitando que as pessoas possam ter mais informação e agilidade em acessa-lás. É possível  gerenciar os objetos  e dispositivos à distância.
    - Exemplos: eletrodomesticos, aplicativos, carros...
    - Funcionamento a partis de conexão a rede (Wi-fi) ou Bluetooth , acessando a nuvem, sensores, machine learning, inteligência antificial. 
    - Identificados através dos endereços IP
  # Sistemas Pervasivos e Sistema Obíquos
<img width="405" height="124" alt="images" src="https://github.com/user-attachments/assets/3ded5f8f-2268-481f-b473-ce1e64711223" />

- *Sistema pervasivos:*  São sistemas que estão espalhados por vários lugares e dispositivos ao mesmo tempo, fazendo parte do nosso dia a dia sem que a gente precise ficar buscando por eles. A ideia é que a tecnologia esteja presente no ambiente ao redor, conectando diferentes dispositivos para facilitar a vida das pessoas. Um exemplo simples seria uma casa inteligente, onde as luzes, o ar-condicionado e as câmeras se comunicam entre si e reagem automaticamente ao que acontece no ambiente.

- *Existem 3 tipos de sistema pervasinos:*
  
  - *Sistemas pervasivos por rede de sensores:*
  São sistemas formados por aparelhos eletrônicos, como: Ipad, tablets, tv’s, geladeiras. Compõe todos os aparelhos que compõem um sistema domésticos de uma casa e são ligados a um únicos sistema distribuído, que mais comumente é um modem roteador que dará acesso a rede. Esse sistema tem como principal característica e também vulnerabilidade, não ser autoconfigurável e nem auto gerenciável. O que torna um aspecto importante a ser melhorado. 
  
  - *Sistemas pervasivos para tratamento de saúde:* Esse sistema tem como principal objetivo evitar a hospitalização do paciente. Ele leva o médico a ter um controle 100% do tempo do paciente, onde estaria no corpo do mesmo alguns sensores instalados que levariam a informação sobre a monitoração que exerce a cada momento. Necessita de uma rede de dados sem interrupções e também não tem a finalidade de incomodar o paciente no seus trabalhos diários. 
O principal problema ainda é além de uma rede de dados que esteja sempre em bom funcionamento é também o custo, que fica relativamente alto com esse método.

  - *Sistemas pervasivos domésticos:* Estas se caracterizam por possuírem um elevado número de nodos (dispositivos), geralmente de tamanho reduzido e com possibilidade de mobilidade. Cada sensor e um elemento autônomo capaz de captar a informação do meio, tratar e enviar estas informações através de uma infraestrutura de comunicação sem-fio, para isso e necessário ter no mínimo um transceptor para comunicações, uma unidade de sensoriamento, fonte de energia, memoria e uma unidade de processamento. 

- *Sistema Oblíquo:* "São sistemas que, assim como os pervasivos, estão em todo lugar, mas com uma característica especial: eles funcionam de forma tão discreta e natural que a gente mal percebe que estão ali. O conceito foi criado por Mark Weiser e propõe que a tecnologia se torne parte invisível do cotidiano, como se fosse algo tão comum quanto a luz elétrica, que a gente usa sem nem pensar. Um exemplo seria o celular que automaticamente muda o fuso horário quando você viaja para outro país.
  
 - *Exemplo:*  Smartphones que automaticamente ajustam o idioma, fuso horário e configurações ao detectar a localização do usuário. Uma casa inteligente, em que vários sensores e atuadores atuam integrados para que se tenha as condições desejadas no ambiente, tais como controle de luminosidade, controle de temperatura, entre outros. 
  - *Exemplos:*
  -  Quando você entra no carro e o bluetooth conecta sozinho no seu celular.
  -  O reconhecimento de rosto que desbloqueia o celular sem você fazer nada.
  -  A Netflix que te recomenda séries baseada no que você já assistiu.
  -  O Google Maps que já sabe o trânsito em tempo real sem você pedir.

# ioT e Modelo TCP/IP
Anotações em aula: 
    Computadores se comunicam (trocar informação) atravéz de um cabo de rede que tem portas lógicas, passa comunicação, escrita ou leitura. Sem isso (TCP)  não tem internet das coisa. 
    Conjunto de protocolos para ter comunicação.
    
    reiniciar o modem,  pela um novo servidor, cria um nova rota pq cai por ter um um ta sobrecarregado. 
    Teu wi-fi trava que tem tanto sinal na mesma frequencia ele trava.
    Principio do wi-fi é  regra de fidelidade, celular fiel a uma torre, tentando garantir a comunicação. (isso em redes de telefonia)  
    
    Camadas:
    - Aplicação: Navegador
    - Transporte:UDP  
    - Internet: quando tu monta uma mensagem, é enviada em pacotes (cortam), final se encontra e monta a mesagem. 
    - Camada de acesso a rede: Nem sempre tem uma comunicação ponto-a-ponto, eu falo diretamente com a pessoa. 
    Passa por uma rede, comunicando dadot. 
    Uma vez conectado,
    Tem vunerabilidades: Falta de criptografia
      
