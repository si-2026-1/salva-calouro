---
author: Caio Fernando Roccha de Albuquerque
date: 2026-05-27
changes: Revisão e refinamento das histórias de usuário
---

# Épico 3 — Jornada Acadêmica

Focado na gestão da vida acadêmica e no planejamento do curso. Contempla a interface visual do fluxo curricular, permitindo o acompanhamento do progresso, a validação de disciplinas cursadas e a previsão de matrículas futuras.

**Requisitos Funcionais Associados:** RF09, RF10, RF11, RF12

---

## Histórias de Usuário (User Stories)

### US3.1 — Visualização da Grade Curricular Interativa

- **Descrição:**
  Como estudante da Universidade de Brasília
  Quero visualizar a grade curricular do meu curso em um formato de fluxo visual interativo
  Para entender facilmente a distribuição das disciplinas obrigatórias e optativas ao longo dos semestres.
- **Critérios de Aceitação:**
  - O sistema deve renderizar o fluxo do curso dividindo as matérias por semestres recomendados.
  - Cada disciplina deve possuir um card visual indicando seu nome, código, quantidade de créditos e natureza (obrigatória/optativa).
  - O fluxo deve destacar visualmente as conexões de pré-requisitos entre as matérias (ex: ligando as caixas por linhas ou setas).

### US3.2 — Acompanhamento de Progresso e Histórico

- **Descrição:**
  Como aluno da UnB
  Quero marcar as disciplinas nas quais já fui aprovado
  Para manter meu histórico escolar atualizado na plataforma e visualizar meu percentual de conclusão de curso.
- **Critérios de Aceitação:**
  - O usuário deve conseguir alterar o status de uma disciplina para "Concluída" diretamente pelo fluxo visual.
  - O sistema deve calcular e exibir uma barra de progresso com a porcentagem de créditos obrigatórios e optativos integralizados.
  - O sistema deve permitir desmarcar uma disciplina caso o usuário tenha cometido um erro de preenchimento.

### US3.3 — Simulação e Previsão de Matrícula (Verificação de Pré-requisitos)

- **Descrição:**
  Como estudante planejando o próximo semestre letivo
  Quero que o sistema calcule e exiba automaticamente quais matérias estão liberadas para matrícula
  Para planejar minha grade de horários de forma assertiva e sem quebras de pré-requisito.
- **Critérios de Aceitação:**
  - O sistema deve bloquear a seleção de disciplinas cujos pré-requisitos não foram marcados como concluídos na US3.2.
  - As disciplinas com os pré-requisitos cumpridos devem receber um destaque visual de "Liberada para Matrícula".
  - O algoritmo deve validar cenários de co-requisitos (matérias que precisam ser feitas em conjunto).

### US3.4 — Consulta de Ementas e Detalhes de Disciplinas

- **Descrição:**
  Como calouro montando minha grade
  Quero consultar a explicação, ementa básica e departamento responsável por uma disciplina
  Para entender seu conteúdo programático e nível de dificuldade antes de efetivar a matrícula no SIGAA.
- **Critérios de Aceitação:**
  - Ao clicar no card de uma disciplina, um modal com o conteúdo detalhado da ementa deve ser aberto.
  - O detalhamento deve exibir o código oficial da UnB, departamento ofertante, ementa textual e bibliografia básica (se houver).
  - O sistema deve exibir uma lista de disciplinas que dependem diretamente da matéria consultada (pós-requisitos).
