# Documento de Requisitos: Sistema de Coleta de Dados de Estações Meteorológicas

Este documento detalha os requisitos funcionais e de qualidade para o desenvolvimento do Sistema de Coleta de Dados de Estações Meteorológicas, um projeto em parceria com a Tecsus.

---

## 1. Visão Geral do Projeto

### 1.1 Título do Projeto
Sistema de Coleta de Dados de Estações Meteorológicas

### 1.2 Problema
Como coletar, processar e visualizar dados de estações meteorológicas de baixo custo para expandir o portfólio da empresa para o monitoramento ambiental e, ao mesmo tempo, criar uma ferramenta de engajamento educacional para alunos do ensino médio.

### 1.3 Descrição
O projeto visa o desenvolvimento de uma solução completa para monitoramento ambiental através de estações meteorológicas de baixo custo. A plataforma será responsável por recepcionar, tratar e armazenar dados de sensores (vento, chuva, umidade, temperatura, pressão) enviados via redes IoT.

Os dados serão exibidos em um portal web com dashboards interativos e relatórios analíticos. Um diferencial do projeto é seu forte componente educacional: o portal incluirá uma área para explicar os conceitos matemáticos e estatísticos por trás dos parâmetros medidos, relacionando-os à importância do monitoramento para a prevenção de desastres naturais. As estações desenvolvidas serão instaladas em instituições de ensino parceiras para uso prático no aprendizado baseado em problemas.

### 1.4 Perfis de Usuário (Personas)

* **Administrador:** Responsável por gerenciar o sistema, cadastrar estações, configurar parâmetros, criar regras de alerta e gerenciar usuários.
* **Usuário Público/Estudante:** Acessa o portal para visualizar os dashboards, consultar dados históricos, gerar relatórios públicos e acessar o conteúdo educacional.

---

## 2. Requisitos Funcionais (RF)

Os Requisitos Funcionais descrevem **o que** o sistema deve fazer.

### RF-01: Gerenciamento do Sistema (CRUD)
* **RF-01.1:** O sistema deve permitir que Administradores gerenciem (Criar, Ler, Atualizar, Excluir) as **estações meteorológicas**, associando seus respectivos sensores e localização.
* **RF-01.2:** O sistema deve permitir que Administradores gerenciem os **parâmetros** de medição que podem ser recebidos pelo sistema.
* **RF-01.3:** O sistema deve permitir que Administradores gerenciem as **regras de alerta**, definindo limites para parâmetros específicos (ex: velocidade do vento > 60km/h).
* **RF-01.4:** O sistema deve permitir que Administradores gerenciem as **contas de usuário** e seus níveis de permissão.

### RF-02: Coleta e Processamento de Dados
* **RF-02.1:** O sistema deve possuir um serviço (API) para **recepcionar** os pacotes de dados enviados pelas estações meteorológicas.
* **RF-02.2:** O sistema deve **processar e validar** os dados recebidos, tratando possíveis inconsistências antes do armazenamento.
* **RF-02.3:** O sistema deve **armazenar** os dados em um banco de dados otimizado para séries temporais e dados relacionais.
* **RF-02.4:** Um **datalogger** deve ser desenvolvido e implementado em hardware para coletar, registrar e transmitir os dados dos sensores da estação.

### RF-03: Visualização e Análise
* **RF-03.1:** O portal deve exibir **dashboards interativos** com visualizações (gráficos, medidores) dos dados meteorológicos em tempo real e históricos.
* **RF-03.2:** Os dashboards devem permitir a filtragem de dados por estação e por período de tempo.
* **RF-03.3:** O sistema deve ser capaz de gerar pelo menos **três tipos de relatórios** distintos (ex: consolidados diários, picos de chuva, médias mensais).
* **RF-03.4:** O sistema deve aplicar **conceitos estatísticos** básicos (média, mediana, desvio padrão) nas análises apresentadas nos dashboards e relatórios.

### RF-04: Alertas e Notificações
* **RF-04.1:** O sistema deve **gerar alertas automáticos** quando os dados recebidos de uma estação ultrapassarem os limites definidos nas regras de alerta.
* **RF-04.2:** Os alertas gerados devem ser notificados aos usuários administradores por um meio a ser definido (ex: e-mail, notificação no portal).

### RF-05: Conteúdo Educacional
* **RF-05.1:** O portal deve ter uma área dedicada com **tutoriais e guias** explicando o significado de cada parâmetro meteorológico e como ele é medido.
* **RF-05.2:** O conteúdo deve ser apresentado de forma didática, visando engajar estudantes do ensino médio.

### RF-06: Hardware
* **RF-06.1:** Uma **estação meteorológica** física e funcional deve ser montada utilizando os componentes e sensores definidos.

---

## 3. Requisitos de Qualidade (Não Funcionais - RNF)

Os Requisitos de Qualidade descrevem **como** o sistema deve operar, definindo seus atributos e restrições.

### RNF-01: Usabilidade e Experiência do Usuário (UX)
* **RNF-01.1:** A interface do portal, especialmente os dashboards, deve ser intuitiva, esteticamente agradável e de fácil navegação para engajar os usuários.
* **RNF-01.2:** O sistema deve ter um design responsivo, adaptando-se a diferentes tamanhos de tela (desktop e smartphones).
* **RNF-01.3:** O conteúdo educacional deve ser apresentado de forma clara e acessível, cumprindo o objetivo de **engajamento estudantil**.

### RNF-02: Segurança
* **RNF-02.1:** O sistema deve implementar um **controle de acesso** baseado em perfis, com no mínimo dois níveis: **Administrador** (acesso total) e **Público** (acesso somente leitura a dashboards e conteúdo educacional).
* **RNF-02.2:** A API de recepção de dados deve ser protegida para garantir que apenas estações autorizadas possam enviar dados.

### RNF-03: Desempenho
* **RNF-03.1:** O serviço de recepção de dados deve ser robusto e escalável, capaz de processar um alto volume de transmissões simultâneas das estações.
* **RNF-03.2:** As consultas nos dashboards e relatórios devem ter um tempo de resposta rápido, mesmo com um grande volume de dados históricos.

### RNF-04: Manutenibilidade e DevOps
* **RNF-04.1:** Toda a API do sistema deve possuir uma **documentação detalhada** e clara, incluindo exemplos de requisição e resposta para cada rota (endpoint).
* **RNF-04.2:** Um **pipeline de Integração Contínua (CI)** deve ser implementado para automatizar a execução de testes e validações a cada nova alteração no código.
* **RNF-04.3:** O processo de **deploy (implantação)** da aplicação em ambiente de produção deve ser automatizado para garantir consistência e agilidade nas atualizações.