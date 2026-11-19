# BarberFlow

Repositório oficial de **especificação, prototipação e validação** do projeto **BarberFlow** — uma solução web focada na jornada de agendamento de serviços e gestão operacional para barbearias.

---

## Objetivo do Repositório

Centralizar de forma organizada toda a documentação de engenharia de software, artefatos de negócio, diagramas, protótipos interativos de interface (UX/UI) e evidências de validação do produto.

---

## Estrutura de Pastas

```text
BarberFlow/
├── docs/
│   ├── documentos-originais/      # Documentos base do projeto (Pré-projeto em PDF e A3 em DOCX)
│   ├── modelo-de-negocio/         # Definição de proposta de valor e modelo de negócio
│   ├── requisitos/                # Especificação de requisitos funcionais e não funcionais
│   ├── regras-de-negocio/         # Regras de negócio e restrições do domínio
│   ├── diagramas/                 # Fluxogramas, organogramas e modelagens do sistema
│   ├── personas-e-storyboards/    # Personas, jornadas do usuário e storyboards
│   ├── planejamento/              # Cronogramas, escopo e planejamento das entregas
│   ├── metodologia/               # Processos e metodologias adotadas pelo squad
│   ├── gestao-de-riscos/          # Matriz de riscos e planos de mitigação
│   └── relatorio-final/           # Consolidação e relatório final do projeto
├── prototypes/
│   ├── html/                      # Protótipo web interativo (visao-geral.html e telas S1–S5)
│   ├── imagens/                   # Logotipo e capturas das telas do protótipo
│   └── mockups/                   # Mockups iniciais e rascunhos visuais de interface
├── tests/                         # Artefatos, roteiros e evidências de testes e validação
├── .gitignore                     # Regras de arquivos e pastas ignorados pelo Git
└── README.md                      # Documentação principal do repositório
```

---

## Como Abrir o Protótipo Interativo

O protótipo funcional pode ser visualizado diretamente no navegador, sem necessidade de servidor ou dependências externas:

1. Clone ou acesse a pasta local do repositório.
2. Navegue até `prototypes/html/`.
3. Abra o arquivo **[`prototypes/html/visao-geral.html`](prototypes/html/visao-geral.html)** em qualquer navegador moderno (Chrome, Edge, Firefox ou Safari).

> **Dica:** Na tela `visao-geral.html`, utilize as setas laterais ou os indicadores inferiores para navegar pelas 5 telas da jornada do usuário:
> - **S1:** Catálogo & Profissional (`tela1.html`)
> - **S2:** Agenda & Horários (`tela2.html`)
> - **S3:** Dados & Confirmação (`tela3.html`)
> - **S4:** Agendamento Confirmado (`tela4.html`)
> - **S5:** Painel do Barbeiro (`tela5.html`)

---

## Fluxo de Branches (Git)

- `main`: Branch principal estável, contendo a estrutura base e entregas consolidadas.
- `develop`: Branch de integração contínua para documentação e protótipos.
- `feature/*`: Branches temáticas integradas via merge na `develop` (ex.: `feature/documentacao`, `feature/prototipos`).
