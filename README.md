# Salva Calouro

Plataforma digital de orientação e integração para novos alunos da Universidade de Brasília (UnB), cruzando dados de localização física com o progresso acadêmico do estudante.

## O Problema

No contexto acadêmico da universidade, observa-se que os alunos ingressantes (calouros) enfrentam grande dificuldade de adaptação nos primeiros semestres devido à sobrecarga de informações fragmentadas e à complexidade do espaço físico.

## A Solução

Um sistema colaborativo que une navegação espacial e planejamento acadêmico. O aplicativo atua como um guia interativo, conectando as dúvidas dos calouros à experiência dos veteranos. O objetivo principal é simplificar a geolocalização no campus e otimizar a gestão do fluxo curricular, transformando a adaptação universitária em uma jornada mais autônoma e fluida.

---

## Configuração do Ambiente

### Pré-requisitos

- **Python 3.8+** - Para execução do MkDocs
- **pip** - Gerenciador de pacotes Python
- **git** - Controle de versão

### Instalação

```bash
# Crie um ambiente virtual
python3 -m venv .venv

# Ative o ambiente virtual
source .venv/bin/activate  # Linux/Mac
# ou
.venv\Scripts\activate     # Windows

# Instale as dependências
pip install mkdocs mkdocs-material
```

---

## Estrutura do Projeto

```text
.
├── docs/                    # Documentação do projeto
│   ├── index.md            # Página inicial
│   ├── requisitos/         # Requisitos funcionais e não-funcionais
│   ├── epicos/             # Épicos do projeto
│   └── ...
├── overrides/              # Customizações do tema
│   └── partials/           # Componentes HTML personalizados
├── mkdocs.yml              # Configuração do MkDocs
└── README.md               # Este arquivo
```

- **docs/**: Todos os arquivos markdown da documentação
- **mkdocs.yml**: Configuração do site (tema, navegação, plugins)
- **overrides/**: Customizações visuais do tema Material

---

## Desenvolvimento

### Executar Localmente

```bash
# Ative o ambiente virtual (se ainda não ativado)
source .venv/bin/activate

# Inicie o servidor de desenvolvimento
mkdocs serve
```

O site estará disponível em `http://127.0.0.1:8000`

**Recursos do servidor de desenvolvimento:**
- Auto-reload: Alterações nos arquivos são refletidas automaticamente
- Live preview: Visualize mudanças em tempo real
- Ctrl+C para interromper

### Build para Produção

```bash
# Gera os arquivos estáticos na pasta site/
mkdocs build
```

---

## Comandos Úteis

```bash
# Servidor de desenvolvimento (com endereço específico)
mkdocs serve -a 0.0.0.0:8000

# Build limpo (remove cache anterior)
mkdocs build --clean

# Verificar configuração
mkdocs --verbose build

# Listar comandos disponíveis
mkdocs --help
```

## Links

[Prototipação](https://www.figma.com/design/OXKKcagHWRRzG0XCwU79pO/SI---Salva-Calouro?node-id=0-1&p=f&t=z1tKezGkALLh1RO3-0)