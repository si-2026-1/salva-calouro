---
changes: Criação do guia de design e prototipação do frontend
---

# Guia de Design e Prototipação — Salva Calouro

Documento de apoio para a prototipação do frontend no Figma. Consolida os
requisitos funcionais (RF), histórias de usuário (US) e o modelo de dados em
um **inventário de telas, fluxos, componentes e identidade visual**.

A plataforma é **web responsiva, Mobile-first** (RNF01): todas as telas são
projetadas primeiro para smartphone (375 px) e depois adaptadas para desktop.

---

## 1. Identidade Visual

### 1.1 Paleta de Cores

| Papel | Cor | HEX | Uso |
| :--- | :--- | :--- | :--- |
| **Primária (Azul UnB)** | 🔵 | `#113C75` | Cabeçalhos, botões primários, links, navegação ativa, marca |
| **Secundária (Verde)** | 🟢 | `#04843D` | Sucesso, "Concluído", "Liberada para matrícula", confirmações, badges |
| **Preto / Texto** | ⚫ | `#1A1A1A` | Texto principal (não usar preto puro `#000`) |
| **Branco / Fundo** | ⚪ | `#FFFFFF` | Fundo principal, cards |
| **Cinza 100 (Surface)** | | `#F4F6F9` | Fundo de seções, áreas secundárias |
| **Cinza 300 (Bordas)** | | `#D9DEE6` | Divisores, bordas de inputs, contornos de cards |
| **Cinza 500 (Texto suave)** | | `#6B7280` | Legendas, placeholders, metadados |

**Tons de apoio derivados** (para estados e destaques, mantendo a base azul/verde/neutra):

| Papel | HEX | Uso |
| :--- | :--- | :--- |
| Azul claro (hover/seleção) | `#E7EDF6` | Fundo de item selecionado, hover sutil |
| Verde claro | `#E3F1E9` | Fundo de tags/chips de sucesso, disciplina concluída |
| Alerta / urgente | `#C2410C` | Prazos vencendo, pré-requisito faltando (usar com parcimônia) |
| Alerta claro | `#FDEBE1` | Fundo de tags de alerta |

> Regra de contraste (RNF08 — Acessibilidade): texto sobre azul `#113C75` deve
> ser branco. Texto sobre verde `#04843D` deve ser branco. Garantir contraste
> mínimo AA (4.5:1) em todo texto de corpo.

### 1.2 Tipografia

Sugestão: **Inter** ou **Roboto** (sans-serif legível, boa em telas pequenas).

| Estilo | Tamanho / Peso | Uso |
| :--- | :--- | :--- |
| Display | 28 / Bold | Títulos de tela |
| H1 | 22 / Bold | Cabeçalhos de seção |
| H2 | 18 / SemiBold | Subtítulos, títulos de card |
| Body | 16 / Regular | Texto padrão |
| Body S | 14 / Regular | Texto secundário, descrições |
| Caption | 12 / Medium | Metadados, tags, labels de campo |

### 1.3 Grid, Espaçamento e Raios

- **Espaçamento base:** múltiplos de 4 px (4, 8, 12, 16, 24, 32).
- **Margem lateral mobile:** 16 px. **Desktop:** container central de 1140 px.
- **Raio de borda:** 12 px (cards), 8 px (botões/inputs), full (chips/avatares).
- **Sombra de card:** sutil, `0 2px 8px rgba(17,60,117,0.08)`.
- **Touch target mínimo:** 44 × 44 px (acessibilidade em locomoção).

---

## 2. Arquitetura de Informação

### 2.1 Mapa do Aplicativo (Sitemap)

```
Salva Calouro
├── Onboarding / Autenticação (público)
│   ├── Splash / Boas-vindas
│   ├── Login
│   ├── Cadastro (com seleção de curso)
│   └── Recuperar senha
│
├── App autenticado (navegação principal — bottom nav)
│   ├── 🗺️  Mapa            (Épico 2)
│   ├── 🎓  Meu Fluxo       (Épico 3)
│   ├── 💬  Comunidade      (Épico 4)
│   ├── 🏆  Ranking         (Épico 5)
│   └── 👤  Perfil          (Épicos 1 e 5)
│
└── Telas internas (acessadas a partir das principais)
    ├── Detalhe de Ponto de Interesse / Rota
    ├── Detalhe de Disciplina (ementa)
    ├── FAQ + Calendário Acadêmico
    ├── Tópico do Fórum + Respostas + Criar postagem
    └── Configurações de Perfil
```

### 2.2 Navegação Principal (Bottom Navigation — mobile)

Barra fixa inferior com 5 itens. Ícone + label. Item ativo em azul `#113C75`.

`[ Mapa ] [ Fluxo ] [ Comunidade ] [ Ranking ] [ Perfil ]`

No **desktop**, converter para barra lateral (sidebar) ou top nav horizontal com
os mesmos 5 destinos + logo à esquerda.

### 2.3 Diferenciação de Perfil (US1.3)

A interface se adapta ao perfil:

- **Calouro** — foco em consumir: Mapa, Fluxo, FAQ, leitura do fórum. CTA de
  introdução/dicas em destaque.
- **Veterano** — tudo do calouro + ações de geração de conteúdo: botão "Criar
  postagem" no fórum, edição de POIs, visualização de pontuação/medalhas em
  destaque no perfil.

Use estados de componente no Figma (ex.: botão "Criar postagem" com variante
`visível/oculto`) para representar a diferença de permissão.

---

## 3. Inventário de Telas

Cada tela referencia o Épico, as US e os RF que atende.

### Grupo A — Autenticação e Perfil (Épico 1 · RF01–RF04)

| # | Tela | US | Elementos-chave |
| :-- | :-- | :-- | :-- |
| A1 | **Boas-vindas / Splash** | — | Logo, slogan, botões "Entrar" e "Criar conta" |
| A2 | **Login** | US1.2 | E-mail institucional, senha, "Manter-me conectado", erro genérico, link "Esqueci a senha" |
| A3 | **Cadastro** | US1.1 | Nome, e-mail institucional, senha, **dropdown de curso (cursos ativos da UnB)**, validação de e-mail, semestre de ingresso |
| A4 | **Perfil** | US1.4, US5.1 | Avatar, nome, curso, **pontuação total e medalhas** (veterano), atalhos, botão "Editar" e "Sair" |
| A5 | **Configurações de Perfil** | US1.4 | Editar nome, foto, curso; alterar e-mail/senha **exige confirmação de senha atual**; botão "Salvar Alterações" |

### Grupo B — Navegação Espacial (Épico 2 · RF05–RF08)

| # | Tela | US | Elementos-chave |
| :-- | :-- | :-- | :-- |
| B1 | **Mapa Interativo** | US2.1 | Mapa do campus com zoom/pan, camadas de prédios/blocos, "Ponto Azul" de geolocalização, barra de busca flutuante |
| B2 | **Busca de POI** | US2.2 | Campo com autocomplete, suporte a siglas (PJC, PAT, ICC), resultados **categorizados** (Auditórios, Banheiros, Secretarias, RU…) |
| B3 | **Detalhe do Local (modal/aba)** | US2.4 | Nome oficial, foto, horário de funcionamento, descrição, botão **"Traçar Rota"** |
| B4 | **Rota traçada** | US2.3 | Linha de rota sobre o mapa, tempo estimado de caminhada, origem/destino, **toggle "Rota acessível" (rampas/elevadores)** |

### Grupo C — Jornada Acadêmica (Épico 3 · RF09–RF12)

| # | Tela | US | Elementos-chave |
| :-- | :-- | :-- | :-- |
| C1 | **Meu Fluxo (Grade)** | US3.1, US3.2 | Colunas por semestre, **cards de disciplina** (nome, código, créditos, natureza), linhas de pré-requisito, barra de progresso (% obrigatórias / optativas) |
| C2 | **Disciplina — estados** | US3.2, US3.3 | Estados do card: *Concluída* (verde), *Liberada* (destaque), *Bloqueada* (cinza/cadeado), *Cursando* |
| C3 | **Detalhe da Disciplina (modal)** | US3.4 | Código oficial UnB, departamento, ementa textual, créditos, carga horária, bibliografia, **pré-requisitos e pós-requisitos** |

### Grupo D — Informação e Comunidade (Épico 4 · RF13–RF15)

| # | Tela | US | Elementos-chave |
| :-- | :-- | :-- | :-- |
| D1 | **FAQ / Base de Conhecimento** | US4.1 | Busca textual no topo, **categorias** (Secretaria, Alimentação, Estágios, Matrícula), respostas em **accordions** |
| D2 | **Fórum (lista de tópicos)** | US4.2 | Lista de tópicos com título/categoria/autor/votos, filtro, botão **"Criar Nova Postagem"** (veterano) |
| D3 | **Tópico + Respostas** | US4.2 | Conteúdo do tópico, respostas encadeadas, **upvote**, marcação de "melhor resposta", botão denunciar |
| D4 | **Criar Postagem** | US4.2 | Título, categoria, corpo do texto, publicar |
| D5 | **Calendário Acadêmico** | US4.3 | Timeline/calendário do semestre, **tags de alerta** para prazos da semana, filtro por tipo, exportar (Google Calendar) |

### Grupo E — Engajamento (Épico 5 · RF16–RF17)

| # | Tela | US | Elementos-chave |
| :-- | :-- | :-- | :-- |
| E1 | **Ranking (Leaderboard)** | US5.2 | Lista ordenada por pontuação: posição, avatar, nome, curso, medalha principal; **filtro temporal** (Mensal / Semestral / Geral) |
| E2 | **Medalhas / Conquistas** | US5.1 | Galeria de badges desbloqueadas/bloqueadas, pontos necessários, integrada ao Perfil (A4) |

---

## 4. Biblioteca de Componentes (para Figma)

Crie como **componentes com variantes** para reuso e consistência.

**Globais**
- **Botão**: variantes `Primário` (azul preenchido), `Secundário` (contorno azul),
  `Sucesso` (verde), `Texto/link`, `Desabilitado`; tamanhos `M`/`L`.
- **Campo de texto**: estados `default`, `foco`, `erro`, `preenchido`; com label e helper.
- **Dropdown / Select** (curso, categoria, filtros).
- **Chip / Tag**: `categoria`, `sucesso` (verde), `alerta` (laranja), `neutro`.
- **App Bar** (topo): título + ação contextual.
- **Bottom Navigation**: 5 itens, estado ativo/inativo.
- **Avatar**: tamanhos `S`/`M`/`L`, com placeholder.
- **Modal / Bottom Sheet**: para detalhes (POI, disciplina).
- **Card** (base reutilizável).
- **Barra de progresso** (fluxo curricular).
- **Estado vazio** e **Skeleton/loading** (RNF03 — feedback em até 3 s).
- **Toast / mensagem de erro** (login, validações).

**Específicos**
- **Card de Disciplina** (variantes de estado: Concluída / Liberada / Bloqueada / Cursando / Optativa).
- **Card de Resultado de Busca de POI** (com categoria).
- **Card de Detalhe de Local** (foto, horário, "Traçar rota").
- **Item de Ranking** (posição, avatar, nome, curso, medalha).
- **Badge / Medalha** (desbloqueada / bloqueada).
- **Item de FAQ (accordion)**.
- **Card de Tópico do Fórum** (com upvote e contagem de respostas).
- **Item de Calendário/Timeline** (com tag de urgência).

---

## 5. Referência do Modelo de Dados (origem dos campos)

Resumo do diagrama físico para alimentar os textos/placeholders do protótipo
com dados coerentes.

### Usuário-exemplo padrão (persona dos mockups)

Para manter consistência em todas as telas, os dados de exemplo do usuário
logado usam sempre a mesma persona fictícia:

- **Nome:** João Rossi  ·  **Iniciais (avatar):** JR
- **E-mail:** joao.rossi@aluno.unb.br
- **Curso:** Engenharia de Software · 3º semestre  ·  **Perfil:** Veterano

- **USUARIO**: nome, email, matricula, curso → base dos perfis.
  - **CALOURO**: semestre_ingresso.
  - **VETERANO**: pontuacao_total, semestre_atual.
- **CURSO**: codigo, nome, grau, turno, departamento.
- **DISCIPLINA**: codigo, nome, ementa, carga_horaria, creditos.
  - **PERTENCE** (curso↔disciplina): semestre_sugerido, tipo (obrig./optativa).
  - **PRE_REQUISITO**: disciplina_requer ↔ disciplina_prereq.
  - **CURSOU** (usuário↔disciplina): status, mencao, periodo, ano.
- **PONTO_INTERESSE**: nome, tipo, latitude, longitude, descricao, horario_funcionamento.
  - **ROTA**: distancia_m, tempo_estimado_min, ponto_origem/destino.
- **EVENTO_CALENDARIO**: titulo, descricao, tipo, data_inicio, data_fim (relacionado a CURSO via ABRANGE).
- **ARTIGO_FAQ**: titulo, conteudo, categoria, palavras_chave, data_publicacao.
- **TOPICO_FORUM**: titulo, conteudo, categoria, status, data_criacao.
  - **RESPOSTA**: conteudo, melhor_resposta (bool).
- **CONQUISTA**: nome, descricao, icone, pontos_necessarios.
  - **CONQUISTOU** (veterano↔conquista): data_conquista.

---

## 6. Fluxos Principais (para protótipo navegável)

1. **Onboarding:** A1 → A3 (cadastro com curso) → B1 (Mapa, home padrão).
2. **Encontrar uma sala:** B1 → B2 (busca "ICC") → B3 (detalhe) → B4 (rota acessível).
3. **Planejar matrícula:** C1 (fluxo) → marcar concluídas → ver "liberadas" → C3 (ementa).
4. **Tirar dúvida:** D1 (FAQ busca) → sem resposta → D2 (fórum) → D3 (tópico) → upvote.
5. **Engajamento veterano:** D4 (criar postagem) → +pontos → E2 (medalha) → E1 (ranking).

---

## 7. Checklist de Qualidade (RNF)

- [ ] **Mobile-first** (RNF01): toda tela validada em 375 px antes do desktop.
- [ ] **Personalização por curso** (RNF02): fluxo, mapa e FAQ refletem o curso do usuário.
- [ ] **Feedback ≤ 3 s** (RNF03): skeletons/loaders em mapa, rota e fluxo.
- [ ] **Erros seguros** (RNF05): login não revela qual campo está incorreto (US1.2).
- [ ] **Acessibilidade** (RNF08): contraste AA, touch targets 44 px, foco visível,
      toggle de rota acessível (US2.3).
