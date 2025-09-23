
# Fluxo de Trabalho e Checklists da Sprint

Este documento descreve os rituais e os checklists que guiam o trabalho dentro de cada Sprint, garantindo alinhamento, qualidade e melhoria contínua.

---

## 1. Checklist do Processo da Sprint

Estas são as etapas e verificações essenciais em toda Sprint.

### Sprint Planning (Planejamento)
O objetivo é definir o que pode ser entregue na Sprint e como esse trabalho será realizado.

- [ ] **Meta da Sprint Definida:** Uma meta clara e concisa foi estabelecida e acordada por todo o time.
- [ ] **Itens Selecionados Atendem à DoR:** Todas as User Stories puxadas para a Sprint Backlog cumprem 100% da nossa [Definition of Ready (DoR)](./DEFINITION_OF_READY.md).
- [ ] **Capacidade do Time Considerada:** O volume de trabalho é compatível com a capacidade histórica do time.
- [ ] **Plano de Trabalho Criado:** As histórias são quebradas em tarefas menores (sub-tasks) para facilitar a execução e o acompanhamento.
- [ ] **Time se Compromete com a Meta:** A equipe expressa confiança de que a meta da Sprint pode ser alcançada.

### Sprint Review (Revisão)
O objetivo é inspecionar o incremento do produto e adaptar o Product Backlog.

- [ ] **Incremento "Done" Demonstrado:** Apenas o trabalho que atende 100% à nossa [Definition of Done (DoD)](./DEFINITION_OF_DONE.md) é apresentado.
- [ ] **Feedback dos Stakeholders Coletado:** O PO e outras partes interessadas fornecem feedback sobre o que foi entregue.
- [ ] **Product Backlog Atualizado:** O feedback é usado pelo PO para revisar e repriorizar o Product Backlog para as próximas Sprints.

### Sprint Retrospective (Retrospectiva)
O objetivo é que o time inspecione a si mesmo e crie um plano de melhorias para a próxima Sprint.

- [ ] **Discussão Aberta:** O time discute o que funcionou bem, o que não funcionou e o que pode ser melhorado no processo, nas ferramentas ou na colaboração.
- [ ] **Causa Raiz Identificada:** Para os problemas levantados, o time busca entender as causas fundamentais.
- [ ] **Plano de Ação Criado:** Pelo menos uma ação de melhoria concreta e mensurável é definida para ser implementada na próxima Sprint.

---

## 2. Evolução da Definition of Done (DoD) por Sprint

Nosso DoD não é estático. À medida que o produto e nossas ferramentas amadurecem, podemos adicionar novos critérios de qualidade. Com base no nosso backlog, esta é uma possível evolução:

### Adições ao DoD na Sprint 1
*(Foco em estabelecer a base do sistema)*

Além de todos os itens do DoD geral, uma história na Sprint 1 só está "Done" se:
- [ ] **Infraestrutura Essencial Provisionada:** Para histórias como a US #1 (Banco de Dados) e US #2 (API de Recepção), a infraestrutura correspondente foi configurada, testada e está operacional no ambiente de desenvolvimento.
- [ ] **Regras de Negócio Documentadas:** Para as US #4 (Alertas) e #6 (Acesso), as regras implementadas estão documentadas no código ou em uma wiki para referência futura.

### Adições ao DoD na Sprint 2
*(Foco em automação e na primeira entrega de valor visível ao usuário)*

Além de todos os itens do DoD geral e da Sprint 1, uma história na Sprint 2 só está "Done" se:
- [ ] **Passou pelo Pipeline de CI/CD:** O código foi integrado e implantado no ambiente de testes/desenvolvimento de forma 100% automatizada pelos pipelines criados nas US #8 e #9. **Este item se torna obrigatório para todas as Sprints futuras.**
- [ ] **Testado com Dados do Datalogger:** Funcionalidades que consomem dados, como a US #10 (Dashboard), foram validadas usando dados reais ou simulados enviados pelo Datalogger (US #7).

### Adições ao DoD na Sprint 3
*(Foco em escalabilidade e integrações externas)*

Além de todos os itens do DoD geral e das Sprints anteriores, uma história na Sprint 3 só está "Done" se:
- [ ] **Teste de Performance Realizado:** Para a US #11 (Dashboard Interativo), foi realizado um teste de carga simples para garantir que os filtros e gráficos respondem rapidamente com um volume de dados histórico considerável.
- [ ] **Documentação da API Revisada por Terceiros:** A documentação da API (US #13) foi revisada por alguém de fora do time de desenvolvimento (ou outro desenvolvedor) para garantir clareza e facilidade de uso.