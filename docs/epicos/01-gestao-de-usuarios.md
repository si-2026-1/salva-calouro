---
author: Caio Fernando Roccha de Albuquerque
date: 2026-05-27
changes: Revisão e refinamento das histórias de usuário com foco em critérios testáveis e personas da UnB
---

# Épico 1 — Gestão de Usuários

Este épico abrange o fluxo de entrada, autenticação e controle de acesso dos usuários na plataforma, garantindo a diferenciação funcional e de permissões entre os perfis que consomem informação e os que a geram.

**Requisitos Funcionais Associados:** RF01, RF02, RF03, RF04

---

## Histórias de Usuário (User Stories)

### US1.1 — Cadastro por Curso

- Título: Cadastro por Curso
- Descrição:
  Como estudante da Universidade de Brasília
  Quero me cadastrar na plataforma informando o meu curso de graduação
  Para acessar as funcionalidades e conteúdos personalizados de acordo com a minha grade e fluxo acadêmico.
- Critérios de Aceitação:
  - O sistema deve apresentar uma lista de seleção com os cursos de graduação ativos da UnB.
  - O usuário deve preencher obrigatoriamente nome, e-mail institucional, senha e curso.
  - O sistema deve validar se o e-mail inserido possui formato válido antes de concluir o cadastro.
  - O sistema deve impedir a criação de mais de uma conta com o mesmo e-mail.

### US1.2 — Autenticação Segura

- Título: Autenticação Segura
- Descrição:
  Como usuário cadastrado no Salva Calouro
  Quero realizar o login de forma segura utilizando minhas credenciais
  Para acessar minhas preferências, histórico de fluxo e dados salvos na plataforma.
- Critérios de Aceitação:
  - O sistema deve autenticar o usuário mediante a validação correta do e-mail e senha cadastrados.
  - O sistema deve exibir uma mensagem de erro clara em caso de credenciais inválidas, sem especificar qual dos campos está incorreto por motivos de segurança.
  - A senha deve ser criptografada no banco de dados através de um algoritmo de hash seguro.
  - O sistema deve oferecer uma opção "Manter-me conectado" para persistir a sessão do usuário de forma segura.

### US1.3 — Diferenciação de Perfis (Calouro/Veterano)

- Título: Diferenciação de Perfis (Calouro/Veterano)
- Descrição:
  Como estudante da UnB autenticado no sistema
  Quero que a plataforma identifique automaticamente se sou calouro ou veterano
  Para que a interface exiba as ferramentas de navegação e níveis de permissão adequados ao meu perfil.
- Critérios de Aceitação:
  - O sistema deve classificação o perfil com base no semestre de ingresso ou fluxo inserido pelo usuário.
  - Perfil **Calouro** deve visualizar prioritariamente guias de introdução, mapas de salas e dicas de ambientação.
  - Perfil **Veterano** deve ter acesso liberado às ferramentas de geração de conteúdo e fóruns de mentoria (conforme regras de permissão).
  - O sistema deve restringir o acesso a páginas administrativas ou de moderação para perfis que não possuam essas permissões específicas.

### US1.4 — Edição de Perfil

- Título: Edição de Perfil
- Descrição:
  Como usuário ativo do Salva Calouro
  Quero poder editar as informações do meu perfil a qualquer momento
  Para manter meus dados acadêmicos, foto de exibição e contatos devidamente atualizados.
- Critérios de Aceitação:
  - O sistema deve disponibilizar uma tela exclusiva de "Configurações de Perfil" acessível após o login.
  - O usuário deve poder alterar o nome de exibição, a foto de perfil e o curso atual.
  - O sistema deve exigir a confirmação da senha atual caso o usuário solicite a alteração do e-mail ou da senha de acesso.
  - O sistema deve salvar e refletir as alterações imediatamente em toda a plataforma após o clique no botão "Salvar Alterações".

---
