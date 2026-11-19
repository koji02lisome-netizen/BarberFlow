# BarberFlow

Repositório oficial de **especificação, prototipação e validação** do projeto **BarberFlow** — *Sistema Web de Agendamento e Gestão para Barbearias Locais* (Squad 01 — Unidade Curricular de Garantia da Qualidade de Software, UNISOCIESC, 2026).

---

## Objetivo do Repositório

Centralizar de forma versionada e rastreável toda a documentação de engenharia de software, análise de negócio, requisitos, regras de domínio, diagramas, protótipos interativos de interface (UX/UI) e artefatos de validação do produto.

---

## Estrutura Completa do Repositório

```text
BarberFlow/
├── docs/
│   ├── documentos-originais/
│   │   ├── A3 Squad 01 - App Barbearias (2).docx
│   │   ├── Sistema Web para Barbearias - Cockpit.pdf
│   │   ├── pre-projeto-squad1official.pdf
│   │   └── roteiro_gravacao_cockpit_barbearia.pdf
│   ├── modelo-de-negocio/
│   │   └── modelo-de-negocio.md
│   ├── requisitos/
│   │   └── requisitos.md
│   ├── regras-de-negocio/
│   │   └── regras-de-negocio.md
│   ├── diagramas/
│   │   ├── diagramas.md
│   │   └── fluxograma-operacional.png
│   ├── personas-e-storyboards/
│   │   └── personas-e-storyboards.md
│   ├── planejamento/
│   │   ├── organograma.png
│   │   └── planejamento.md
│   ├── metodologia/
│   │   └── metodologia.md
│   ├── gestao-de-riscos/
│   │   └── matriz-de-riscos.md
│   └── relatorio-final/
│       └── resumo-executivo.md
├── prototypes/
│   ├── html/
│   │   ├── visao-geral.html
│   │   ├── BarberFlow-visao-geral-unico.html
│   │   ├── tela1.html
│   │   ├── tela2.html
│   │   ├── tela3.html
│   │   ├── tela4.html
│   │   └── tela5.html
│   ├── imagens/
│   │   ├── logo.png
│   │   ├── prototipoofficialtela1.png
│   │   ├── prototipoofficialtela2.png
│   │   ├── prototipoofficialtela3.png
│   │   ├── PROTOTIPOOFFICIALTELA4.png
│   │   └── prototipoofficialtela5.png
│   └── mockups/
│       ├── primeiro-prototipo-mockup.jpeg
│       └── video-demonstracao.mp4
├── tests/
│   ├── matriz-de-testes.md
│   ├── casos-de-teste.md
│   ├── criterios-de-aceitacao.md
│   └── resultados-da-validacao.md
├── .gitignore
└── README.md
```

---

## Documentação e Diagramas

| Área | Documento / Artefato | Descrição |
| :--- | :--- | :--- |
| **Modelo de Negócio** | [docs/modelo-de-negocio/modelo-de-negocio.md](docs/modelo-de-negocio/modelo-de-negocio.md) | Problema, proposta de valor, síntese Canvas e comparativo (AppBarber e Booksy). |
| **Requisitos** | [docs/requisitos/requisitos.md](docs/requisitos/requisitos.md) | Requisitos Funcionais (`RF01`–`RF14`) e Não Funcionais (`RNF01`–`RNF10`), diferenciando escopo `S1`–`S5` e módulos futuros. |
| **Regras de Negócio** | [docs/regras-de-negocio/regras-de-negocio.md](docs/regras-de-negocio/regras-de-negocio.md) | Regras de agenda, concorrência, preços/duração, bloqueios, prazos e políticas (`RN01`–`RN10`). |
| **Diagramas** | [docs/diagramas/diagramas.md](docs/diagramas/diagramas.md) · [fluxograma-operacional.png](docs/diagramas/fluxograma-operacional.png) | Fluxo operacional de agendamento e sequência em 5 fases. |
| **Personas e Storyboards** | [docs/personas-e-storyboards/personas-e-storyboards.md](docs/personas-e-storyboards/personas-e-storyboards.md) | Personas (Ricardo, Lucas e Thiago) e cenários *Antes vs. Com o Sistema*. |
| **Planejamento e Equipe** | [docs/planejamento/planejamento.md](docs/planejamento/planejamento.md) · [organograma.png](docs/planejamento/organograma.png) | Squad 01, níveis de acesso e cronograma de marcos (2026). |
| **Metodologia** | [docs/metodologia/metodologia.md](docs/metodologia/metodologia.md) | Transição Cascata → Scrum/Kanban, níveis de teste e fluxo Git. |
| **Gestão de Riscos** | [docs/gestao-de-riscos/matriz-de-riscos.md](docs/gestao-de-riscos/matriz-de-riscos.md) | Riscos mapeados (`R01`–`R05`), impacto e Plano B de contingência. |
| **Resumo Executivo** | [docs/relatorio-final/resumo-executivo.md](docs/relatorio-final/resumo-executivo.md) | Consolidação executiva, escopo, qualidade e estratégia de apresentação. |
| **Validação e Testes** | [matriz-de-testes.md](tests/matriz-de-testes.md) · [casos-de-teste.md](tests/casos-de-teste.md) · [criterios-de-aceitacao.md](tests/criterios-de-aceitacao.md) · [resultados-da-validacao.md](tests/resultados-da-validacao.md) | Rastreabilidade, casos de teste (`CT01`–`CT13`), cenários BDD e relatório de aprovação. |

---

## Como Abrir o Protótipo Interativo

Os protótipos funcionais podem ser abertos diretamente no navegador, sem necessidade de servidor ou instalação:

- **Apresentação modular (com `iframe` das telas `S1`–`S5`):**
  [`prototypes/html/visao-geral.html`](prototypes/html/visao-geral.html)
- **Apresentação em arquivo único autocontido (ideal para compartilhamento offline):**
  [`prototypes/html/BarberFlow-visao-geral-unico.html`](prototypes/html/BarberFlow-visao-geral-unico.html)

### Telas da Jornada (`S1` a `S5`)

| Tela | Arquivo | Descrição |
| :--- | :--- | :--- |
| **S1** | [`prototypes/html/tela1.html`](prototypes/html/tela1.html) | Catálogo de Serviços & Seleção de Profissional |
| **S2** | [`prototypes/html/tela2.html`](prototypes/html/tela2.html) | Seleção de Data & Grade de Horários em Tempo Real |
| **S3** | [`prototypes/html/tela3.html`](prototypes/html/tela3.html) | Dados do Cliente, Recibo & Reserva Temporária (10 min) |
| **S4** | [`prototypes/html/tela4.html`](prototypes/html/tela4.html) | Agendamento Confirmado, Protocolo & Políticas |
| **S5** | [`prototypes/html/tela5.html`](prototypes/html/tela5.html) | Painel Diário do Barbeiro & Bloqueio de Horário/Almoço |

---

## Fluxo de Branches (Git)

- `main`: Branch principal estável com a entrega final consolidada.
- `develop`: Branch de integração contínua.
- `feature/*`: Branches temáticas (`feature/documentacao`, `feature/prototipos`, `feature/organizacao-assets`, `feature/requisitos`, `feature/regras-de-negocio`, `feature/documentacao-complementar`, `feature/validacao`).
