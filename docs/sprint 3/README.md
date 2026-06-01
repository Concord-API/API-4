# API - 4º Semestre BD

# Trivio – Gerenciamento de manutenções
<p align="center">
    <img src="/docs/img/trivio branco.svg" alt="Logo Trivio" width="300">
</p>

# Documentação - Sprint 3

## Desafio

Implementar uma plataforma para gerenciar manutenções de equipamentos distribuídos globalmente, vinculados a contratos de diferentes empresas. A solução permitirá registrar equipamentos, acompanhar horas de uso e planejar intervenções técnicas considerando fatores como localização, duração estimada e prioridade das manutenções.

## User Stories

| Rank | Prioridade | User Story | Estimativa | Sprint | Meta |
| --- | --- | --- | --- | --- | --- |
| 8 | Alta | **Como Técnico**, quero documentar a manutenção **para registrar o processo da manutenção**. | 8 | Sprint 3 | Sim |
| 9 | Alta |**Como Administrador**, quero acompanhar as manutenções feitas pelos Técnicos **para auxiliar o técnico caso necessário**.| 8 | Sprint 3 | Sim |
| 10 | Alta | **Como Administrador**, quero criar processos personalizados para contratos específicos **para ajudar na documentação e agir de acordo com a necessidade do cliente.** | 5 | Sprint 3 | Sim |
| 11 | Média | **Como usuário**, quero receber alertas na tela **para prevenção de erros.**. | 3 | Sprint 3 | Sim |
| 12 | Baixa | **Como Usuário**, quero adaptar o tema da minha conta **para se adequar ao meus gostos**. | 1 | Sprint 3 | Não |

---
## Resumo
| ID   | User Story | Prioridade | Status | Meta | DoR Atendido | DoD Atendido | Requisito Referenciado |
|------|------------|------------|--------|------------------|--------------|--------------|------------------------|
| Sprint3-1 | Como técnico, quero documentar a manutenção para registrar o processo da manutenção | Alta | Concluída | ✅ | ✅ | ✅ | [8] Documentação de manutenção |
| Sprint3-2 | Como Administrador, quero acompanhar as manutenções feitas pelos Técnicos para auxiliar o técnico caso necessário | Alta | Concluída | ✅ | ✅ | ✅ | [9] Compartilhamento de informações de manutenção |
| Sprint3-3 | Como Administrador, quero criar processos personalizados para contratos específicos para ajudar na documentação e agir de acordo com a necessidade do cliente | Alta | Concluída | ✅ | ✅ | ✅ | [10] Processos personalizados por contrato |
| Sprint3-4 | Como usuário, quero receber alertas na tela para prevenção de erros | Média | Concluída | ✅ | ✅ | ✅ | [11] Atualização na UX |
| Sprint3-5 | Como Usuário, quero adaptar o tema da minha conta para se adequar aos meus gostos | Baixa | Concluída | ❌ | ✅ | ✅ | [12] Personalização de tema da conta |
---

# Requisitos

<details open>
  <summary>Expandir/Recolher</summary>


## ✅ US: Como Técnico, quero documentar a manutenção para registrar o processo da manutenção

| ID | Critério                                                                                                                        |
| -- | ------------------------------------------------------------------------------------------------------------------------------- |
| 1  | O sistema deve permitir ao Técnico registrar informações sobre a execução da manutenção.|
| 2  | O Técnico deve conseguir inserir uma descrição das atividades realizadas.|
| 3  | O sistema deve validar os campos obrigatórios antes de concluir o registro.|
| 4  | Apenas usuários com perfil de Técnico ou Administrador podem visualizar a documentação da manutenção.                           |
| 5  | As informações documentadas devem ser armazenadas corretamente no banco de dados e permanecer disponíveis para consulta futura. |

---

## ✅ US: Como Administrador, quero acompanhar as manutenções feitas pelos Técnicos para auxiliar o técnico caso necessário

| ID | Critério                                                                                           |
| -- | -------------------------------------------------------------------------------------------------- |
| 1  | O sistema deve permitir ao Administrador visualizar todas as manutenções cadastradas.              |
| 2  | O sistema deve exibir o Técnico responsável por cada manutenção.                                   |
| 3  | O Administrador deve conseguir visualizar o status atual de cada manutenção.                       |
| 4  | O sistema deve exibir informações relevantes da manutenção, como cliente, local e datas previstas. |
| 5  | O Administrador deve conseguir consultar a documentação registrada pelo Técnico.                   |
| 6  | Apenas usuários com perfil de Administrador podem acessar essa funcionalidade.                     |
| 7  | As informações apresentadas devem refletir os dados atualizados da manutenção.                     |

---

## ✅ US: Como Administrador, quero criar processos personalizados para contratos específicos para ajudar na documentação e agir de acordo com a necessidade do cliente

| ID | Critério                                                                                             |
| -- | ---------------------------------------------------------------------------------------------------- |
| 1  | O sistema deve permitir ao Administrador criar processos personalizados para contratos específicos.  |
| 2  | O processo deve possuir nome e descrição obrigatórios.                                               |
| 3  | O Administrador deve conseguir editar ou remover etapas do processo.                                 |
| 4  | O sistema deve associar corretamente o processo ao contrato selecionado.                             |
| 5  | O Administrador deve conseguir visualizar e editar processos já cadastrados.                         |
| 6  | O sistema deve validar os campos obrigatórios antes de salvar o processo.                            |
| 7  | Apenas usuários com perfil de Administrador podem criar, editar ou excluir processos personalizados. |
| 8  | Os processos personalizados devem ser armazenados corretamente no banco de dados.                    |

---

## ✅ US: Como usuário, quero receber alertas na tela para prevenção de erros

| ID | Critério                                                                                                       |
| -- | -------------------------------------------------------------------------------------------------------------- |
| 1  | O sistema deve exibir alertas quando o usuário realizar uma ação inválida ou preencher informações incorretas. |
| 2  | Os alertas devem apresentar mensagens claras e objetivas sobre o erro identificado.                            |
| 3  | O sistema deve exibir os alertas em tempo real sempre que possível.                                            |
| 4  | O usuário deve conseguir corrigir as informações após a exibição do alerta.                                    |
| 5  | O sistema deve impedir a continuidade da ação quando houver erro de validação.                                 |
| 6  | Os alertas devem seguir o padrão visual definido para o projeto.                                               |
| 7  | O sistema não deve apagar os dados já preenchidos após a exibição do alerta.                                   |
| 8  | O sistema deve exibir mensagens de confirmação quando uma ação for concluída com sucesso.                      |

---

## ✅ US: Como Usuário, quero adaptar o tema da minha conta para se adequar aos meus gostos

| ID | Critério                                                                                           |
| -- | -------------------------------------------------------------------------------------------------- |
| 1  | O sistema deve permitir ao Usuário alterar o tema da sua conta.                                    |
| 2  | O sistema deve disponibilizar, no mínimo, as opções de tema Claro e Escuro.                        |
| 3  | A alteração do tema deve ser aplicada imediatamente após a seleção.                                |
| 4  | O sistema deve salvar a preferência de tema do Usuário.                                            |
| 5  | O tema selecionado deve ser mantido em acessos futuros.                                            |
| 6  | O tema deve ser aplicado em todas as telas do sistema.                                             |
| 7  | O Usuário deve conseguir alterar o tema sempre que desejar.                                        |
| 8  | O sistema deve garantir a legibilidade e a usabilidade da interface em todos os temas disponíveis. |

</details>

---

# DoR - Definition of Ready

<details open>
  <summary>Expandir/Recolher</summary>

###  DoR — US: Acompanhar Manutenções dos Técnicos

|                Critério                | Descrição                                                                                                                        |
| :------------------------------------: | -------------------------------------------------------------------------------------------------------------------------------- |
|       Clareza e Valor de Negócio       | A User Story está claramente descrita e o objetivo de acompanhar e auxiliar os Técnicos durante as manutenções foi identificado. |
|    Critérios de Aceitação Definidos    | Os critérios para visualização, acompanhamento e consulta das manutenções foram definidos e compreendidos pelo time.             |
|     Priorização pelo Product Owner     | A User Story foi priorizada pelo Product Owner.                                                                                  |
|          Estimativa de Esforço         | A história possui estimativa de esforço validada pelo time de desenvolvimento.                                                   |
|       Dependências Identificadas       | Foram identificadas dependências relacionadas ao cadastro de manutenções, usuários e permissões de acesso.                       |
| Referências Visuais (quando aplicável) | Wireframes, dashboards ou modelos de tela foram feitos baseados em padrões de mercado de acordo com o tema do nosso projeto.                                             |

---

###  DoR — US: Documentar Manutenção

|                Critério                | Descrição                                                                                                                    |
| :------------------------------------: | ---------------------------------------------------------------------------------------------------------------------------- |
|       Clareza e Valor de Negócio       | A User Story está claramente descrita e o objetivo de registrar o processo da manutenção foi identificado.                   |
|    Critérios de Aceitação Definidos    | Os critérios de aceitação para registro, consulta e armazenamento da documentação foram definidos e compreendidos pelo time. |
|     Priorização pelo Product Owner     | A User Story foi priorizada pelo Product Owner.                                                                              |
|          Estimativa de Esforço         | A história possui estimativa de esforço validada pelo time de desenvolvimento.                                               |
|       Dependências Identificadas       | Foram identificadas as dependências relacionadas à manutenção, usuários e banco de dados para armazenamento das informações. |
| Referências Visuais (quando aplicável) | Wireframes, dashboards ou modelos de tela foram feitos baseados em padrões de mercado de acordo com o tema do nosso projeto                                               |

---

###  DoR — US: Criar Processos Personalizados para Contratos

|                Critério                | Descrição                                                                                                           |
| :------------------------------------: | ------------------------------------------------------------------------------------------------------------------- |
|       Clareza e Valor de Negócio       | A User Story está claramente descrita e o valor de adaptar processos às necessidades dos clientes foi identificado. |
|    Critérios de Aceitação Definidos    | Os critérios de criação, edição, associação e visualização dos processos foram definidos e compreendidos pelo time. |
|     Priorização pelo Product Owner     | A User Story foi priorizada pelo Product Owner.                                                                     |
|          Estimativa de Esforço         | A história possui estimativa de esforço validada pelo time de desenvolvimento.                                      |
|       Dependências Identificadas       | Foram identificadas dependências relacionadas ao cadastro de contratos e persistência dos processos personalizados. |
| Referências Visuais (quando aplicável) | Wireframes, dashboards ou modelos de tela foram feitos baseados em padrões de mercado de acordo com o tema do nosso projeto                                          |

---

###  DoR — US: Receber Alertas para Prevenção de Erros

|                Critério                | Descrição                                                                                                          |
| :------------------------------------: | ------------------------------------------------------------------------------------------------------------------ |
|       Clareza e Valor de Negócio       | A User Story está claramente descrita e o benefício de reduzir erros operacionais foi identificado.                |
|    Critérios de Aceitação Definidos    | Os critérios para exibição, conteúdo e comportamento dos alertas foram definidos e compreendidos pelo time.        |
|     Priorização pelo Product Owner     | A User Story foi priorizada pelo Product Owner.                                                                    |
|          Estimativa de Esforço         | A história possui estimativa de esforço validada pelo time de desenvolvimento.                                     |
|       Dependências Identificadas       | Foram identificadas dependências relacionadas às validações do sistema e aos fluxos de negócio que exigem alertas. |
| Referências Visuais (quando aplicável) | Esse tópico foi feito baseado em padrões UX de mercado de acordo com o tema do nosso projeto                                     |

---

###  DoR — US: Personalização de Tema da Conta

|                Critério                | Descrição                                                                                                            |
| :------------------------------------: | -------------------------------------------------------------------------------------------------------------------- |
|       Clareza e Valor de Negócio       | A User Story está claramente descrita e o benefício de personalização da experiência do usuário foi identificado.    |
|    Critérios de Aceitação Definidos    | Os critérios para seleção, aplicação e persistência do tema foram definidos e compreendidos pelo time.               |
|     Priorização pelo Product Owner     | A User Story foi priorizada pelo Product Owner.                                                                      |
|          Estimativa de Esforço         | A história possui estimativa de esforço validada pelo time de desenvolvimento.                                       |
|       Dependências Identificadas       | Foram identificadas dependências relacionadas à interface do sistema e ao armazenamento das preferências do usuário. |
| Referências Visuais (quando aplicável) | Mockups ou referências visuais dos temas disponíveis foram disponibilizados.|

</details>

---

# DoD - Definition of Done

<details open>
  <summary>Expandir/Recolher</summary>

## ✅ DoD — US: Documentar Manutenção

|             Critério             | Descrição                                                                                                               |
| :------------------------------: | ----------------------------------------------------------------------------------------------------------------------- |
|    Funcionalidade Implementada   | O Técnico consegue registrar e consultar a documentação de uma manutenção vinculada corretamente à ordem de manutenção. |
| Critérios de Aceitação Atendidos | Todos os critérios de aceitação da User Story foram implementados e validados.                                          |
|         Revisão de Código        | O código desenvolvido foi revisado por pelo menos um membro da equipe.                                                  |
|         Testes Realizados        | Os testes unitários e funcionais relacionados ao registro e consulta da documentação foram executados e aprovados.      |
|       Integração Concluída       | A funcionalidade foi integrada ao repositório principal sem conflitos.                                                  |
|      Documentação Atualizada     | A documentação do sistema foi atualizada com o fluxo de documentação de manutenção.                                     |
|      Padrão Visual Atendido      | A interface segue o padrão visual definido para o projeto.                                                              |
|    Validação do Product Owner    | A funcionalidade foi demonstrada e aprovada pelo Product Owner durante a review da sprint.                              |

---

## ✅ DoD — US: Acompanhar Manutenções dos Técnicos

|             Critério             | Descrição                                                                                                               |
| :------------------------------: | ----------------------------------------------------------------------------------------------------------------------- |
|    Funcionalidade Implementada   | O Administrador consegue visualizar e acompanhar as manutenções realizadas pelos Técnicos.                              |
| Critérios de Aceitação Atendidos | Todos os critérios de aceitação da User Story foram implementados e validados.                                          |
|         Revisão de Código        | O código desenvolvido foi revisado por pelo menos um membro da equipe.                                                  |
|         Testes Realizados        | Os testes unitários e funcionais relacionados à consulta e acompanhamento das manutenções foram executados e aprovados. |
|       Integração Concluída       | A funcionalidade foi integrada ao repositório principal sem conflitos.                                                  |
|      Documentação Atualizada     | A documentação do sistema foi atualizada com as instruções de acompanhamento das manutenções.                           |
|      Padrão Visual Atendido      | A interface segue o padrão visual definido para o projeto.                                                              |
|    Validação do Product Owner    | A funcionalidade foi demonstrada e aprovada pelo Product Owner durante a review da sprint.                              |

---

## ✅ DoD — US: Criar Processos Personalizados para Contratos

|             Critério             | Descrição                                                                                                        |
| :------------------------------: | ---------------------------------------------------------------------------------------------------------------- |
|    Funcionalidade Implementada   | O Administrador consegue criar, editar e associar processos personalizados a contratos específicos.              |
| Critérios de Aceitação Atendidos | Todos os critérios de aceitação da User Story foram implementados e validados.                                   |
|         Revisão de Código        | O código desenvolvido foi revisado por pelo menos um membro da equipe.                                           |
|         Testes Realizados        | Os testes unitários e funcionais relacionados à criação e manutenção dos processos foram executados e aprovados. |
|       Integração Concluída       | A funcionalidade foi integrada ao repositório principal sem conflitos.                                           |
|      Documentação Atualizada     | A documentação do sistema foi atualizada com as regras de configuração dos processos personalizados.             |
|      Padrão Visual Atendido      | A interface segue o padrão visual definido para o projeto.                                                       |
|    Validação do Product Owner    | A funcionalidade foi demonstrada e aprovada pelo Product Owner durante a review da sprint.                       |

---

## ✅ DoD — US: Receber Alertas para Prevenção de Erros

|             Critério             | Descrição                                                                                            |
| :------------------------------: | ---------------------------------------------------------------------------------------------------- |
|    Funcionalidade Implementada   | O sistema exibe alertas e mensagens de validação para prevenir erros de operação dos usuários.       |
| Critérios de Aceitação Atendidos | Todos os critérios de aceitação da User Story foram implementados e validados.                       |
|         Revisão de Código        | O código desenvolvido foi revisado por pelo menos um membro da equipe.                               |
|         Testes Realizados        | Os testes unitários e funcionais relacionados aos alertas e validações foram executados e aprovados. |
|       Integração Concluída       | A funcionalidade foi integrada ao repositório principal sem conflitos.                               |
|      Documentação Atualizada     | A documentação do sistema foi atualizada com as regras de exibição dos alertas.                      |
|      Padrão Visual Atendido      | As mensagens seguem o padrão visual definido para o projeto.                                         |
|    Validação do Product Owner    | A funcionalidade foi demonstrada e aprovada pelo Product Owner durante a review da sprint.           |

---

## ✅ DoD — US: Personalização de Tema da Conta

|             Critério             | Descrição                                                                                                      |
| :------------------------------: | -------------------------------------------------------------------------------------------------------------- |
|    Funcionalidade Implementada   | O Usuário consegue alterar e salvar suas preferências de tema na plataforma.                                   |
| Critérios de Aceitação Atendidos | Todos os critérios de aceitação da User Story foram implementados e validados.                                 |
|         Revisão de Código        | O código desenvolvido foi revisado por pelo menos um membro da equipe.                                         |
|         Testes Realizados        | Os testes unitários e funcionais relacionados à alteração e persistência do tema foram executados e aprovados. |
|       Integração Concluída       | A funcionalidade foi integrada ao repositório principal sem conflitos.                                         |
|      Documentação Atualizada     | A documentação do sistema foi atualizada com as opções de personalização disponíveis.                          |
|      Padrão Visual Atendido      | Todos os temas seguem o padrão visual e os requisitos de usabilidade definidos para o projeto.                 |
|    Validação do Product Owner    | A funcionalidade foi demonstrada e aprovada pelo Product Owner durante a review da sprint.                     |

</details>

---

## Equipe

<div align="center">
  <table>
    <thead>
      <tr>
        <th align="center">Integrante</th>
        <th align="center">Função</th>
        <th align="center">GitHub</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td align="center">Luís Antônio de S. Cardoso</td>
        <td align="center">Product Owner</td>
        <td align="center"><a href="https://github.com/LuisSCardoso"><img src="https://cdn.simpleicons.org/github/181717" alt="GitHub" width="22" /></a></td>
      </tr>
      <tr>
        <td align="center">João Vitor Andrade</td>
        <td align="center">Scrum Master</td>
        <td align="center"><a href="https://github.com/joaoandrade17"><img src="https://cdn.simpleicons.org/github/181717" alt="GitHub" width="22" /></a></td>
      </tr>
      <tr>
        <td align="center">João Vitor Baranov</td>
        <td align="center">Developer</td>
        <td align="center"><a href="https://github.com/JoaoBaranov"><img src="https://cdn.simpleicons.org/github/181717" alt="GitHub" width="22" /></a></td>
      </tr>
      <tr>
        <td align="center">Victor Nogueira</td>
        <td align="center">Developer</td>
        <td align="center"><a href="https://github.com/victorgsnogueira"><img src="https://cdn.simpleicons.org/github/181717" alt="GitHub" width="22" /></a></td>
      </tr>
      <tr>
        <td align="center">Richard Leonardo Cordeiro</td>
        <td align="center">Developer</td>
        <td align="center"><a href="https://github.com/RichardCordeiro"><img src="https://cdn.simpleicons.org/github/181717" alt="GitHub" width="22" /></a></td>
      </tr>
      <tr>
        <td align="center">Isaac Oliveira</td>
        <td align="center">Developer</td>
        <td align="center"><a href="https://github.com/IsaacOliveiraSouza"><img src="https://cdn.simpleicons.org/github/181717" alt="GitHub" width="22" /></a></td>
      </tr>
      <tr>
        <td align="center">Vinicius P. de Pádua</td>
        <td align="center">Developer</td>
        <td align="center"><a href="https://github.com/orgs/vp-p"><img src="https://cdn.simpleicons.org/github/181717" alt="GitHub" width="22" /></a></td>
      </tr>
    </tbody>
  </table>
</div>
