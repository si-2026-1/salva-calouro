## Histórico de Alterações

| Data       | Descrição                                         | Autor                               |
| :--------- | :------------------------------------------------ | :---------------------------------- |
| 18/05/2026 | Criação do documento com a estrutura inicial.     | Eric Wu Harris                      |
| 27/05/2026 | Revisão e refinamento das histórias de usuário.   | Caio Fernando Roccha de Albuquerque |
| 27/05/2026 | Alteração na formatação das histórias de usuário. | Caio Fernando Roccha de Albuquerque |

# Épico 4 — Informação e Comunidade

Responsável pela centralização de dados burocráticos e pela interação social. Reúne a base de conhecimento estática (FAQ), o calendário de prazos da instituição e o fórum colaborativo de perguntas e respostas.

**Requisitos Funcionais Associados:** RF13, RF14, RF15

---

## Histórias de Usuário (User Stories)

### US4.1 — Base de Conhecimento e FAQ Otimizado

- **Descrição:**
  Como calouro com dúvidas institucionais
  Quero consultar uma base de conhecimento (FAQ) com pesquisa otimizada
  Para entender rapidamente processos burocráticos da UnB, como matrícula, trancamento de disciplinas e ajustes de grade.
- **Critérios de Aceitação:**
  - O sistema deve disponibilizar um campo de busca textual no topo da página de FAQ.
  - Os tópicos de ajuda devem ser categorizados por temas (ex: Secretaria, Alimentação, Estágios, Matrícula).
  - O sistema deve carregar as respostas em sanfonas expansíveis (accordions) para facilitar a leitura visual.
  - A busca deve retornar artigos relevantes com base em palavras-chave inseridas pelo usuário.

### US4.2 — Fórum Colaborativo e Mentoria

- **Descrição:**
  Como veterano da comunidade universitária
  Quero criar tópicos de discussão e responder a postagens de dúvidas na plataforma
  Para compartilhar minha experiência acadêmica e auxiliar ativamente na integração dos novos alunos.
- **Critérios de Aceitação:**
  - Usuários autenticados com o perfil adequado devem possuir um botão para "Criar Nova Postagem".
  - Cada tópico do fórum deve permitir uma seção de respostas encadeadas (comentários).
  - O sistema deve disponibilizar um botão para curtir/votar positivamente nas melhores respostas (upvote).
  - Deve haver uma opção para denunciar conteúdos inadequados, sinalizando-os para a moderação.

### US4.3 — Calendário Acadêmico Integrado

- **Descrição:**
  Como usuário da plataforma
  Quero visualizar as datas críticas e os prazos importantes do calendário acadêmico da UnB
  Para não perder os períodos oficiais de modificação de matrícula, trancamento geral ou solicitações especiais.
- **Critérios de Aceitação:**
  - O sistema deve exibir um componente de calendário visual ou uma linha do tempo (timeline) com os eventos do semestre corrente.
  - Prazos urgentes (com vencimento na mesma semana) devem receber um destaque visual ou tag de alerta.
  - O usuário deve conseguir filtrar os eventos por tipo (ex: Prazos de Matrícula, Feriados, Eventos Acadêmicos).
  - Deve haver uma opção para exportar as datas ou sincronizá-las com calendários externos (como Google Calendar).
