## Estrutura de Branches

  - **main**: Branch principal e estável do projeto. Recebe merges apenas ao final de cada sprint, após revisão e aprovação.  
  - **sprintX** (ex: sprint1, sprint2, sprint3): Cada sprint possui sua própria branch base, onde são integradas todas as funcionalidades desenvolvidas durante aquele ciclo.  
  - **task-número/nome-da-task-com-traço-se-tiver-espaco**: Para cada nova funcionalidade ou correção, é criada uma branch específica a partir da branch da sprint em andamento. Essa Branch é criada a partir do Jira.
  Exemplo: `API-35-0.1-Implementar-documentação-API`

  Após a conclusão e revisão da funcionalidade, é feito um *Pull Request (PR)* para a branch da sprint correspondente.  
  Quando o merge é aprovado, a branch da funcionalidade é deletada para manter o repositório limpo.  
  Ao final da sprint, a branch sprintX é integrada à main através de um *Pull Request* final.  
  A branch da sprint é mantida como histórico do desenvolvimento daquela iteração.