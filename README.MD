# ☁️ Nimbus - Sistema de Coleta de Dados de Estações Meteorológicas

## 📖 Índice

- [📝 Descrição do projeto](#-descrição-do-projeto)
- [📋 Backlog / User Stories](#-backlog--user-stories)
- [📅 Cronograma de evolução do Projeto](#-cronograma-de-evolução-do-projeto)
- [⚙️ Tecnologias utilizadas](#️-tecnologias-utilizadas)
- [🚀 Como executar, usar e testar o projeto](#-como-executar-usar-e-testar-o-projeto)
- [📂 Link para Pasta de Documentação](#-link-para-pasta-de-documentação)
- [👥 Equipe](#-equipe)

---

## 📝 Descrição do projeto

A empresa Tecsus, especializada na coleta e processamento de dados de redes de sensores sem fio (IoT) para utilidades como água, energia e gás, busca expandir seu portfólio para o monitoramento ambiental. Para isso, a empresa deseja desenvolver estações meteorológicas de baixo custo.

O desafio consiste em criar um sistema completo que colete periodicamente dados de sensores de direção e velocidade do vento, índice pluviométrico, umidade, temperatura e pressão. Essas informações serão enviadas a um servidor para tratamento e exibição em um portal com relatórios e dashboards. Um aspecto fundamental do projeto é o seu caráter educacional: o portal deverá demonstrar os conceitos matemáticos por trás dos cálculos dos parâmetros meteorológicos e ressaltar a importância do monitoramento ambiental na prevenção de desastres naturais.

Ao final, kits de estações meteorológicas serão instalados na Escola Estadual Elmano Ferreira Veloso e na Faculdade de Tecnologia de São José dos Campos (Fatec SJC), envolvendo alunos do ensino médio em uma aprendizagem baseada em problemas.

---

## 📋 Backlog / User Stories

| Ranking | Prioridade | User Story | Estimativa | Sprint |
| :--- | :--- | :--- | :---: | :---: |
| 1 | 🔴Alta | Como Desenvolvedor, quero projetar e implementar um banco de dados (relacional/não-relacional) otimizado para receber e armazenar grandes volumes de IoT. | 5 | 1 |
| 2 | 🔴Alta | Como Administrador, quero cadastrar e gerenciar as estações meteorológicas, definindo sua localização (ex. Fatec) e sensores associados. | 8 | 1 |
| 3 | 🔴Alta | Como Administrador, quero criar regras de alerta baseadas em limites dos parâmetros (ex: velocidade do vento > 60km/h) para identificar condições de risco. | 8 | 1 |
| 4 | 🔴Alta | Como Administrador, quero um sistema de controle de acesso com pelo menos dois níveis (administrador e público) para gerenciar as funcionalidades. | 5 | 1 |
| 5 | 🔴Alta | Como Desenvolvedor, quero documentar a API de recepção de dados para facilitar a integração de futuras estações ou sistemas. | 8 | 1 |
| 6 | 🔴Alta | Como Sistema, quero ter um serviço para recepcionar, processar e armazenar os dados de sensores (vento, chuva, umidade, temperatura, pressão) enviados pelas estações. | 13 | 2 |
| 7 | 🔴Alta | Como Desenvolvedor, quero configurar um pipeline de Integração Contínua (CI) para automatizar a compilação (build) e a execução dos testes a cada nova alteração no código. | 8 | 2 |
| 8 | 🔴Alta | Como Desenvolvedor, quero configurar um pipeline de Entrega Contínua (CD) para automatizar o deploy da aplicação em um ambiente (ex: desenvolvimento) após a Integração Contínua ser bem-sucedida. | 8 | 2 |
| 9 | 🔴Alta | Como Usuário, quero acessar um dashboard principal que exiba em tempo real as medições mais recentes de cada estação meteorológica. | 8 | 2 |
| 10 | 🔴Alta | Como Usuário, quero visualizar um painel interativo (dashboard) com gráficos e estatísticas históricas dos dados coletados, permitindo filtrar por período e estação. | 8 | 2 |
| 11 | 🔴Alta | Como Desenvolvedor, quero desenvolver o Datalogger para coletar os dados dos sensores e transmiti-los para o servidor. | 13 | 3 |
| 12 | 🔴Alta | Como Sistema, quero gerar notificações automáticas quando os dados recebidos de uma estação ultrapassarem os limites de alerta definidos. | 5 | 3 |
| 13 | 🟠Média | Como Usuário, quero a capacidade de gerar pelo menos 3 relatórios distintos (ex: consolidados diários, picos de chuva) para análises aprofundadas. | 8 | 3 |
| 14 | 🟠Média | Como Usuário, quero uma área educativa no portal que explique de forma simples o que cada parâmetro meteorológico significa. | 5 | 3 |
| 15 | 🟡Baixa | Como Usuário, quero que o sistema tenha uma interface responsiva (UX), que se adapte bem a diferentes tamanhos de tela, como celulares e computadores. | 5 | 3 |

---

## 📅 Cronograma de evolução do Projeto

O desenvolvimento do projeto foi dividido em três Sprints principais, com os seguintes focos de entrega:

- **Sprint 1:** Arquitetura, modelagem do banco de dados e CRUDs.
- **Sprint 2:** Recepção de dados, parser e armazenamento.
- **Sprint 3:** Datalogger, alertas e relatórios.

---

## ⚙️ Tecnologias utilizadas

### Desenvolvimento Web & Backend
![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)
![Express.js](https://img.shields.io/badge/Express.js-000000?style=for-the-badge&logo=express&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black)
![Tailwind CSS](https://img.shields.io/badge/Tailwind%20CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)

### Banco de Dados & Infraestrutura
![Prisma](https://img.shields.io/badge/Prisma-2D3748?style=for-the-badge&logo=prisma&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazon-aws&logoColor=white)

### IoT & Hardware
![Arduino](https://img.shields.io/badge/Arduino-00979D?style=for-the-badge&logo=Arduino&logoColor=white)
![ESP32](https://img.shields.io/badge/Espressif-E7352C?style=for-the-badge&logo=espressif&logoColor=white)
![MQTT](https://img.shields.io/badge/MQTT-3C5280?style=for-the-badge&logo=eclipse-mosquitto&logoColor=white)

---

## 🚀 Como executar, usar e testar o projeto

O guia completo para clonar, instalar as dependências, executar o projeto em modo de desenvolvimento e rodar os testes está disponível em nosso guia de instalação.

**[➡️ Ver Guia de Instalação e Execução](./docs/Guia.md)**

---

## 📂 Link para Pasta de Documentação

A documentação detalhada do projeto, incluindo manuais, documentação de Sprints e definições (DoR/DoD), pode ser encontrada em nossa pasta de documentação.

**[➡️ Acessar a Documentação Completa](./docs/)**

---

## 👥 Equipe

| Foto | Nome | Papel | Link para GitHub | Link para LinkedIn |
| :---: | :--- | :--- | :--- | :--- |
| <img src="https://github.com/DMBMz.png" alt="Foto de Davi Marinho" height="64" width="64"> | *Davi Marinho* | *Scrum Master* | *https://github.com/DMBMz* | *https://www.linkedin.com/in/davi-miguel-a90821214/* |
| <img src="https://github.com/MagNumGomes.png" alt="Foto de João Góes" height="64" width="64"> | *João Góes* | *Product Owner* | *https://github.com/MagNumGomes* | *https://www.linkedin.com/in/joaovitorgoes* |
| <img src="https://github.com/danprsp.png" alt="Foto de Daniel Piloto" height="64" width="64"> | *Daniel Piloto* | *Developer* | *https://github.com/danprsp* | *https://www.linkedin.com/in/daniel-piloto-98b717226/* |
| <img src="https://github.com/joaosuzuki98.png" alt="Foto de João Suzuki" height="64" width="64"> | *João Suzuki* | *Developer* | *https://github.com/joaosuzuki98* | *https://www.linkedin.com/in/jo%C3%A3o-suzuki-6a2b02192/* |
| <img src="https://github.com/AvyaAquino.png" alt="Foto de Avya Alex" height="64" width="64"> | *Avya Alex* | *Developer* | *https://github.com/AvyaAquino* | *https://www.linkedin.com/in/avya-candido-598b5228a/* |
| <img src="https://github.com/gabrielbguimaraes.png" alt="Foto de Gabriel Guimarães" height="64" width="64"> | *Gabriel Guimarães* | *Developer* | *https://github.com/gabrielbguimaraes* | *https://www.linkedin.com/in/gabriel-g-854017138* |
| <img src="https://github.com/GalaxyBurst.png" alt="Foto de Pedro Prevides" height="64" width="64"> | *Pedro Prevides* | *Developer* | *https://github.com/GalaxyBurst* | *https://www.linkedin.com/in/pedro-prevides-87a0b71a8/* |
| <img src="https://github.com/Miojoguu.png" alt="Foto de Gustavo Lima" height="64" width="64"> | *Gustavo Lima* | *Developer* | *https://github.com/Miojoguu* | *https://www.linkedin.com/in/gustavo-lima-904623295/* |