# Salva Calouro - Sistema de Auxílio a Calouros

## Problema

No contexto acadêmico da universidade, observa-se que os alunos ingressantes (calouros) enfrentam grande dificuldade de adaptação nos primeiros semestres devido à sobrecarga de informações fragmentadas e à complexidade do espaço físico.

Como Sistema de Informação, o projeto visa mitigar as seguintes falhas do cenário atual:
* **Desorientação geográfica:** Dificuldade em campi extensos para a localização de salas e prédios.
* **Incompreensão burocrática:** Falta de clareza sobre as regras, o fluxo curricular e o funcionamento da matrícula.
* **Ausência de canal centralizado:** Falta de um meio confiável que conecte as dúvidas dos novos alunos à experiência prévia dos veteranos.

## Escopo

A plataforma propõe um sistema digital de orientação e integração, cruzando dados de localização física com o progresso acadêmico do estudante.

* **Foco de Ação:** Navegação espacial e planejamento acadêmico.
* **Mecanismo de Apoio:** Conexão colaborativa entre as dúvidas dos calouros e o conhecimento dos veteranos.

O sistema será documentado como um MVP (Produto Mínimo Viável) compreendendo:
* Documentação de Requisitos e Backlog.
* Modelagem Conceitual de Dados (MER/DER).
* Protótipo de Alta Fidelidade (Figma).

## Stakeholders (Interessados)

Para o desenvolvimento deste sistema de informação, identificamos os seguintes atores principais:
* **Calouros (Usuários Consumidores):** Buscam orientação espacial, acadêmica e informacional.
* **Veteranos (Usuários Contribuintes):** Fornecem respostas, atualizações sobre o campus e suporte, sendo recompensados pelo engajamento.
* **Administradores:** Responsáveis pela moderação do conteúdo, atualização do mapa e manutenção da base de dados.
* **Universidade (Ambiente):** Provedora das regras de negócio (grades, pré-requisitos) e do espaço físico mapeado.

## Requisitos Funcionais

* **Cadastro e Gestão de Perfil:** Diferenciação de perfis entre Calouros e Veteranos.
* **Mapa Interativo e Rotas:** Sistema de busca por localização de salas, laboratórios, prédios e serviços, com traçado de rotas dentro da universidade.
* **Controle de Fluxo Curricular:** Interface para acompanhamento do histórico escolar, visualização da grade, explicação de matérias e alertas de pré-requisitos.
* **Base de Conhecimento e FAQ:** Mecanismo de busca otimizado para dúvidas frequentes sobre processos universitários (matrícula, editais, etc.).
* **Calendário Acadêmico Inteligente:** Apresentação das datas críticas da instituição.
* **Sistema de Gamificação e Recompensas:** Atribuição de pontos ou conquistas para veteranos que auxiliam calouros ou cadastram informações úteis na plataforma.

## Requisitos Não Funcionais e Regras de Negócio (Complemento)

* **RNF1 (Usabilidade):** O sistema deve ser construído como uma aplicação web com design responsivo (Mobile-first), priorizando o uso em smartphones durante a locomoção pelo campus.
* **RNF2 (Personalização Institucional):** O sistema deve permitir a adaptação de conteúdo, fluxos e mapas de acordo com o curso selecionado pelo usuário.

## Exemplos de Uso (User Stories)

* "Como calouro, quero visualizar a rota mais rápida da entrada do campus até a minha sala de aula para não me atrasar na primeira semana."
* "Como calouro, quero marcar as disciplinas que já cursei para visualizar exatamente quais matérias estão liberadas para a minha próxima matrícula."
* "Como veterano, quero responder dúvidas de calouros no fórum da plataforma para acumular pontos no sistema de gamificação."

## Detalhes do Produto

* **Modelo de Orientação:** A plataforma atua em dois eixos principais: Espaço (onde o aluno deve estar fisicamente) e Tempo (em qual etapa do curso o aluno se encontra).

## Épicos do Projeto (Backlog)

* **Gestão de Usuários:** Perfis, autenticação e níveis de acesso.
* **Navegação Espacial:** Desenvolvimento do mapa interativo, marcações e rotas.
* **Jornada Acadêmica:** Lógica do controle de fluxo, grade e histórico.
* **Informação e Comunidade:** FAQ, base de conhecimento e fórum de dúvidas.
* **Engajamento:** Lógica do sistema de gamificação e pontuação de veteranos.

## Autores

* Caio Fernando Rocha de Albuquerque - 242034518
* Davi Bragança e Silva - 242001473
* Eric Wu Harris - 242001482
* Roberto Ribeiro Correa de Oliveira Neto - 242009936
* Victor Yan Martinez de Avila - 241032994
