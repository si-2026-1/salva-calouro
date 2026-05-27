| Data | Descrição | Autor |
| :--- | :--- | :--- |
| 27/05/2026 | Adição de diagramas | Eric Wu Harris |
| 18/05/2026 | Criação do documento | Eric Wu Harris |

# Salva Calouro: Sistema de Auxílio a Calouros

Plataforma digital de orientação e integração para novos alunos da Universidade de Brasília (UnB), cruzando dados de localização física com o progresso acadêmico do estudante.

## O Problema
No contexto acadêmico da universidade, observa-se que os alunos ingressantes (calouros) enfrentam grande dificuldade de adaptação nos primeiros semestres devido à sobrecarga de informações fragmentadas e à complexidade do espaço físico. De que forma a centralização de informações acadêmicas e a facilitação da orientação espacial podem mitigar as dificuldades de adaptação de alunos ingressantes nos primeiros semestres universitários?

> [Documento de Problema](problema/problema.md)

## A Solução
Um sistema colaborativo que une navegação espacial e planejamento acadêmico. O aplicativo atua como um guia interativo, conectando as dúvidas dos calouros à experiência dos veteranos. O objetivo principal é simplificar a geolocalização no campus e otimizar a gestão do fluxo curricular, transformando a adaptação universitária em uma jornada mais autônoma e fluida.

## Escopo do Projeto

> [Documento de Escopo](escopo/escopo.md)

**O que o sistema faz:**

* Disponibiliza um mapa interativo e sistema de rotas para localização de salas, laboratórios, prédios e serviços.
* Fornece uma interface para controle de fluxo curricular, acompanhamento do histórico escolar e alertas de pré-requisitos.
* Oferece uma Base de Conhecimento e FAQ para dúvidas sobre processos universitários (matrícula, editais, etc.).
* Possui um sistema de gamificação para recompensar veteranos que auxiliam calouros

**O que o sistema NÃO faz:**

* Não realiza a matrícula oficial em disciplinas (apenas auxilia no planejamento).
* Não substitui os sistemas acadêmicos oficiais da instituição.
* Não garante vagas nas turmas e disciplinas planejadas no fluxo.

## Principais Funcionalidades e Épicos

A arquitetura e as entregas do projeto estão divididas nos seguintes pilares centrais:

* **[Épico 1: Gestão de Usuários](epicos/01-gestao-de-usuarios.md):** Perfis, autenticação e diferenciação de níveis de acesso entre calouros e veteranos.
* **[Épico 2: Navegação Espacial](epicos/02-navegacao-espacial.md):** Desenvolvimento do mapa interativo, marcações e rotas.
* **[Épico 3: Jornada Acadêmica](epicos/03-jornada-academica.md):** Lógica do controle de fluxo, grade e histórico.
* **[Épico 4: Informação e Comunidade](epicos/04-informacao-comunidade.md):** FAQ, base de conhecimento e fórum de dúvidas.
* **[Épico 5: Engajamento](epicos/05-engajamento.md):** Lógica do sistema de gamificação e pontuação de veteranos.

## Requisitos Técnicos e Qualidade

A plataforma deve ser construída como uma aplicação web responsiva (Mobile-first), priorizando o uso em smartphones durante a locomoção pelo campus.

> * [Requisitos Funcionais (RF)](requisitos/req-funcionais.md)
> * [Requisitos Não Funcionais (RNF)](requisitos/req-nao-funcionais.md)

## Autores

* Caio Fernando Rocha de Albuquerque - 242034518
* Davi Bragança e Silva - 242001473
* Eric Wu Harris - 242001482
* Roberto Ribeiro Correa de Oliveira Neto - 242009936
* Victor Yan Martinez de Avila - 241032994