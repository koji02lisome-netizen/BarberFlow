# Resumo Executivo — BarberFlow

## 1. Visão Geral do Projeto

O **BarberFlow** (*Sistema Web de Agendamento e Gestão para Barbearias Locais*) foi concebido na Unidade Curricular de **Garantia da Qualidade de Software** (UNISOCIESC — Joinville/SC, 2026) pelo Squad 01, composto por **Pablo Guerra Prado**, **Claufer Hudson Ferreira**, **Miguel Soares** e **Anderson Kauan Júlio**, sob orientação dos professores **Anderson** e **Diego**.

A iniciativa atende micro e pequenas barbearias de bairro que sofrem com agendamentos manuais via WhatsApp e caderno físico, eliminando choques de horário, reduzindo faltas por esquecimento e evitando interrupções do barbeiro durante os atendimentos.

---

## 2. Escopo da Solução

- **Diferencial competitivo:** ao contrário de plataformas densas e caras (*AppBarber*) ou marketplaces genéricos que cobram taxas e expõem concorrentes (*Booksy*), o BarberFlow entrega um **link web exclusivo da barbearia**, leve e sem necessidade de instalação de aplicativo.
- **MVP Prototipado (`S1` a `S5`):**
  - `S1`: Catálogo de serviços (valores e durações) e seleção de profissional.
  - `S2`: Seletor de data e grade de horários em tempo real (`Manhã`, `Tarde`, `Noite`) com estados livre, indisponível e bloqueado.
  - `S3`: Formulário enxuto (Nome, WhatsApp e observações) com aviso de reserva temporária de 10 minutos.
  - `S4`: Comprovante com código de protocolo (`#BF-45G2`), regras de tolerância (10 min) e cancelamento gratuito (até 2h antes), além de integração com calendário.
  - `S5`: Painel Diário do Barbeiro com timeline de status (`Concluído`, `Em Atendimento`, `Agendado`, `Espaço Bloqueado`) e ação rápida de bloqueio de horário/almoço.
- **Roadmap de Módulos Futuros (A3):**
  - Ficha do Cliente e Histórico Técnico de Cortes (banco de conhecimento).
  - Controle de Estoque e PDV (baixa automática e formas de pagamento).
  - Dashboard Gerencial e Financeiro (ticket médio, faturamento e retenção mensal).

---

## 3. Garantia da Qualidade, Metodologia e Entregas

- **Metodologia:** transição planejada de **Cascata** (consolidação documental inicial) para **Scrum + Kanban** (entregas incrementais alinhadas às Sprints, testes contínuos e controle de fluxo entre os 4 integrantes).
- **Estratégia de Qualidade:** matriz cobrindo testes **Unitários**, de **Integração**, **Funcionais (E2E)**, de **Usabilidade** e de **Concorrência/Segurança**, apoiada por matriz de riscos com planos de contingência.
- **Estratégia de Apresentação:**
  - **Pitch em Vídeo (90s — Wayhub, 18/11 a 23/11/2026):** dividido em 4 blocos (Pablo: problema; Claufer: proposta de valor/diferenciais; Miguel: agendamento e painel; Anderson: estoque, relatórios e encerramento).
  - **Pôster Acadêmico (Jornada Acadêmica UNISOCIESC, 30/11 a 05/12/2026):** síntese visual de negócio, fluxograma/organograma, protótipos, testes e metodologia.

---

## 4. Conclusão

A integração entre levantamento estruturado de requisitos, prototipação focada em simplicidade *mobile-first*, versionamento disciplinado em Git e estratégia de testes em cinco níveis estabelece uma base sólida para entregar um sistema confiável, enxuto e aderente à realidade operacional das barbearias locais.
