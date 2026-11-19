# Metodologia de Desenvolvimento e Fluxo Git — BarberFlow

## 1. Transição Metodológica: Cascata → Ágil (Scrum + Kanban)

O projeto adotou uma estratégia híbrida evolutiva alinhada às demandas da disciplina e à construção incremental do produto:

### 1.1 Fase Inicial — Modelo em Cascata (*Waterfall*)
Na etapa inicial, aplicou-se o modelo sequencial para consolidar os fundamentos documentais exigidos antes da prototipação:
1. Entendimento do negócio e problema das barbearias locais.
2. Análise comparativa de concorrentes (*AppBarber* e *Booksy*).
3. Levantamento de requisitos, personas, storyboards, organograma e fluxograma.
4. Especificação estruturada das interfaces.

### 1.2 Evolução — Metodologia Ágil (*Scrum* e *Kanban*)
Para a prototipação, testes e desenvolvimento contínuo, o squad migrou para **Scrum** apoiado por um quadro **Kanban**, com base em quatro fatores práticos:

- **Entregas incrementais por Sprints:** alinhamento direto aos marcos parciais da disciplina no Wayhub (ex.: Sprint 1 em `21/10/2026` e entregas de novembro).
- **Adaptação rápida a feedbacks:** validações com barbeiros locais permitem repriorizar ajustes de usabilidade no *Product Backlog* sem paralisar o projeto.
- **Transparência entre os 4 integrantes:** uso de quadro Kanban com colunas **A Fazer**, **Em Progresso**, **Em Teste** e **Concluído**, evitando gargalos e sobrecarga individual.
- **Redução de riscos de prazo:** testes e validações acontecem a cada incremento funcional, prevenindo falhas graves às vésperas da entrega final.

---

## 2. Estratégia de Testes e Qualidade

Conforme o plano de Garantia da Qualidade do A3, os testes visam prevenir defeitos em cinco níveis complementares:

| Nível de Teste | Escopo | Alvo | Objetivo de Qualidade |
| :--- | :--- | :--- | :--- |
| **Unitários** | Cálculo de duração, valores e baixa de estoque | Camada de regras (`/src/services`) | Precisão financeira e de inventário antes da integração. |
| **Integração** | Comunicação API + Banco e trava de agenda | Endpoints de agendamento e PDV | Impedir duplicidade de horários sob concorrência. |
| **Funcionais (E2E)** | Jornada completa `S1` até exibição em `S5` | Homologação em navegador real | Validar requisitos do cliente ponta a ponta. |
| **Usabilidade** | Tempo de reserva e legibilidade móvel | Protótipo e interface em smartphones | Garantir uso autônomo por clientes sem baixar app. |
| **Concorrência e Segurança** | Inputs inválidos e acesso simultâneo ao slot | Validação e transações do banco | Evitar corrupção de dados, injeção e choque de agenda. |

---

## 3. Fluxo de Versionamento Git (Git Flow Simplificado)

O repositório (`https://github.com/koji02lisome-netizen/BarberFlow`) segue um modelo estruturado de branches:

- **`main`**: branch principal estável, contendo a estrutura consolidada e marcos prontos.
- **`develop`**: branch de integração contínua onde todas as entregas temáticas são validadas e integradas.
- **`feature/*`**: branches criadas a partir da `develop` para cada entrega isolada (ex.: `feature/documentacao`, `feature/prototipos`, `feature/organizacao-assets`, `feature/requisitos`, `feature/regras-de-negocio`, `feature/documentacao-complementar`), integradas de volta na `develop` via merge (`--no-ff`).
