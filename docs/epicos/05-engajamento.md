---
author: Caio Fernando Roccha de Albuquerque
date: 2026-05-27
changes: Revisão e refinamento das histórias de usuário
---

# Épico 5 — Engajamento

Engloba a camada de gamificação do sistema. É responsável por contabilizar as interações positivas dos veteranos, gerenciar o sistema de pontuação/conquistas e renderizar os painéis de reconhecimento da comunidade.

**Requisitos Funcionais Associados:** RF16, RF17

---

## Histórias de Usuário (User Stories)

### US5.1 — Sistema de Pontuação e Medalhas (Gamificação)

- **Descrição:**
  Como veterano engajado no Salva Calouro
  Quero acumular pontos de experiência e obter medalhas digitais (badges) ao interagir positivamente no fórum ou cadastrar informações úteis
  Para validar meu apoio à comunidade e ter meu esforço de mentoria reconhecido na plataforma.
- **Critérios de Aceitação:**
  - O sistema deve conceder pontos automaticamente com base em ações específicas (ex: +10 pontos por resposta criada, +5 por voto positivo recebido).
  - O sistema deve desbloquear medalhas no perfil do usuário ao atingir marcos predefinidos (ex: Medalha "Mentor Iniciante" após 5 respostas úteis).
  - O usuário deve conseguir visualizar sua pontuação total e sua coleção de medalhas diretamente na sua tela de perfil.

### US5.2 — Painel de Reconhecimento (Ranking da Comunidade)

- **Descrição:**
  Como usuário da plataforma
  Quero visualizar um ranking atualizado com os estudantes veteranos mais ativos do campus
  Para reconhecer, valorizar e identificar facilmente os membros que mais contribuem com o ecossistema da universidade.
- **Critérios de Aceitação:**
  - O sistema deve exibir uma tela de classificação geral (Leaderboard) ordenando os usuários de maior pontuação para menor.
  - O ranking deve exibir a foto de perfil, o nome, o curso e a medalha principal de cada veterano listado.
  - O sistema deve permitir filtrar a classificação por períodos de tempo (ex: Ranking Mensal, Semestral ou Geral do Curso).
  - Os dados do ranking devem ser atualizados de forma assíncrona para garantir a performance da página.
