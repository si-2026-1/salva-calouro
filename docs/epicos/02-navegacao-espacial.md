## Histórico de Alterações

| Data       | Descrição                                         | Autor                               |
| :--------- | :------------------------------------------------ | :---------------------------------- |
| 18/05/2026 | Criação do documento com a estrutura inicial.     | Eric Wu Harris                      |
| 27/05/2026 | Revisão e refinamento das histórias de usuário.   | Caio Fernando Roccha de Albuquerque |
| 27/05/2026 | Alteração na formatação das histórias de usuário. | Caio Fernando Roccha de Albuquerque |

# Épico 2 — Navegação Espacial

Trata da parte geoespacial e visual da aplicação. Engloba a renderização do mapa do campus, os mecanismos de busca por pontos de interesse e o algoritmo de traçado de rotas internas para guiar os estudantes.

**Requisitos Funcionais Associados:** RF05, RF06, RF07, RF08

---

## Histórias de Usuário (User Stories)

### US2.1 — Visualização de Mapa Interativo

- **Descrição:**
  Como estudante da Universidade de Brasília
  Quero visualizar um mapa interativo e responsivo do campus
  Para entender a disposição geográfica dos prédios, blocos e salas de forma intuitiva.
- **Critérios de Aceitação:**
  - O mapa deve carregar corretamente em dispositivos móveis e desktop (responsividade).
  - O usuário deve conseguir realizar ações de zoom (in/out) e pan (arrastar) no mapa.
  - Os prédios e blocos devem ter camadas visuais distintas para fácil identificação.
  - O mapa deve integrar uma API de geolocalização para exibir o "Ponto Azul" da posição atual do usuário.

### US2.2 — Busca por Pontos de Interesse (POI)

- **Descrição:**
  Como estudante da UnB
  Quero pesquisar por uma sala de aula, laboratório ou serviço específico (como o RU) através de uma barra de busca
  Para descobrir sua localização exata sem precisar navegar manualmente pelo mapa.
- **Critérios de Aceitação:**
  - A barra de busca deve oferecer sugestões de preenchimento automático (autocomplete).
  - O sistema deve retornar resultados mesmo para siglas comuns na UnB (ex: "PJC", "PAT", "ICC").
  - Ao selecionar um resultado, o mapa deve centralizar automaticamente no local correspondente com um marcador visual.
  - A busca deve categorizar os resultados (ex: Auditórios, Banheiros, Secretarias).

### US2.3 — Traçado de Rotas Internas

- **Descrição:**
  Como calouro desorientado no campus
  Quero traçar a rota ideal do meu ponto atual até o meu destino final
  Para evitar atrasos e encontrar o caminho mais curto entre blocos e pavilhões.
- **Critérios de Aceitação:**
  - O sistema deve calcular o trajeto utilizando algoritmos de busca em grafos (considerando caminhos transitáveis).
  - A rota deve ser exibida visualmente sobreposta ao mapa com uma linha de destaque.
  - O sistema deve estimar o tempo de caminhada entre o ponto de origem e o destino.
  - Deve ser possível alternar entre rotas acessíveis (rampas/elevadores) e rotas padrão.

### US2.4 — Detalhes do Local (Modais Informativos)

- **Descrição:**
  Como usuário da plataforma
  Quero clicar em um ponto de interesse para visualizar informações detalhadas
  Para conhecer horários de funcionamento, fotos de referência ou avisos importantes do local.
- **Critérios de Aceitação:**
  - Ao clicar em um marcador ou prédio, deve abrir um modal ou aba lateral de detalhes.
  - O detalhamento deve incluir: Nome oficial, foto do local, horário de funcionamento e descrição breve.
  - Deve haver um botão de "Traçar Rota" diretamente dentro do card de detalhes do local.
  - As informações exibidas devem ser consumidas dinamicamente do banco de dados de infraestrutura do campus.
