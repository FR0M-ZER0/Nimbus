# Definition of Ready (DoR) - Definição de Pronto

A **Definition of Ready** é um acordo do time que estabelece os critérios mínimos para uma User Story ser considerada pronta para entrar em uma Sprint. O objetivo é garantir que o time de desenvolvimento possua todas as informações necessárias para trabalhar na história sem grandes impedimentos ou ambiguidades.

---

### Checklist de DoR

Para que uma história seja considerada **"Pronta" (Ready)**, ela deve atender aos seguintes critérios:

- [ ] **História Bem Definida (INVEST):** A história é Independente, Negociável, Valiosa, Estimável, Pequena (Sized appropriately) e Testável.

- [ ] **Critérios de Aceitação Claros:** As condições de sucesso e falha estão escritas de forma objetiva e são testáveis.

- [ ] **Valor de Negócio Explícito:** Todos no time entendem o "porquê" da história e qual benefício ela trará para o usuário ou para o negócio.

- [ ] **Dependências Identificadas:** Quaisquer dependências (técnicas, de outras equipes ou de negócio) foram mapeadas e, se possível, resolvidas.

- [ ] **Estimativa de Esforço Realizada:** O time de desenvolvimento discutiu a complexidade e atribuiu uma estimativa (Story Points).

- [ ] **Protótipos/Mockups Anexados:** Histórias com impacto na interface do usuário (UI/UX) possuem um guia visual (wireframe, mockup ou design final) anexado.

- [ ] **Compreendida pelo Time:** A história foi apresentada e discutida em uma sessão de refinamento, e o time confirma que entendeu o escopo do trabalho.

## Definition of Done (DoD) - Definição de Feito

A **Definition of Done** é o checklist compartilhado por todo o time que define quando um trabalho em um item do backlog está 100% completo. Ela garante um padrão de qualidade consistente e assegura que o incremento entregue ao final da Sprint está potencialmente pronto para ser colocado em produção.

---

### Checklist de DoD

Para que uma história seja considerada **"Feita" (Done)**, ela deve atender a todos os seguintes critérios:

- [ ] **Código Completo e Versionado:** O código foi implementado e submetido ao repositório principal (main/develop branch) via Pull Request.

- [ ] **Código Revisado (Peer Review):** Pelo menos um outro desenvolvedor revisou e aprovou o Pull Request, garantindo conformidade com os padrões de codificação do time.

- [ ] **Testes Unitários Escritos e Passando:** Foram criados testes unitários que cobrem a lógica de negócio implementada, e todos eles executam com sucesso no pipeline.

- [ ] **Testes de Integração Bem-sucedidos:** A nova funcionalidade foi testada em conjunto com as outras partes do sistema para garantir que não há efeitos colaterais indesejados.

- [ ] **Critérios de Aceitação Atendidos:** Todos os Critérios de Aceitação definidos na história foram verificados e validados em um ambiente de testes.

- [ ] **Pipeline de CI/CD Verde:** O processo de Integração Contínua (build, testes automatizados) e Entrega Contínua (deploy em ambiente de homologação) foi executado com sucesso.

- [ ] **Documentação Atualizada:** A documentação técnica, da API ou guias de usuário relevantes foram criados ou atualizados para refletir as mudanças.

- [ ] **Aprovado pelo Product Owner (PO):** A funcionalidade foi demonstrada ao PO (durante a Sprint ou na Sprint Review) e ele a aceitou como completa e alinhada às expectativas.