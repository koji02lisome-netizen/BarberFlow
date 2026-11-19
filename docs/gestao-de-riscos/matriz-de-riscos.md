# Matriz de Gestão de Riscos — BarberFlow

Este documento apresenta os riscos técnicos, operacionais e de cronograma identificados no Documento A3 para o projeto **BarberFlow**, juntamente com sua justificativa, nível de impacto e plano de contingência (**Plano B**).

---

## Matriz de Riscos e Planos de Contingência

| ID | Risco Identificado | Por que foi identificado | Impacto | Plano B (Contingência) |
| :--- | :--- | :--- | :--- | :--- |
| **R01** | **Atraso no cronograma até 23/11** | Acúmulo de entregas acadêmicas simultâneas e logística de gravação do Pitch em grupo. | **Alto** | Priorizar o MVP (agendamento + painel do barbeiro) no quadro Kanban e gravar partes do Pitch remotamente. |
| **R02** | **Choque de horários simultâneos** | Possibilidade de dois clientes selecionarem e tentarem confirmar o mesmo slot ao mesmo tempo. | **Alto** | Aplicar transação atômica no banco de dados e exibir alerta imediato sugerindo novo horário disponível. |
| **R03** | **Baixa adesão de barbearias por complexidade** | Público-alvo habituado ao caderno físico e WhatsApp pode resistir a interfaces densas ou difíceis. | **Médio** | Simplificar a tela inicial em 3 passos objetivos e oferecer *onboarding* guiado com link direto. |
| **R04** | **Indisponibilidade ou perda de código** | Risco de falha em computador local de algum integrante antes dos marcos de entrega. | **Alto** | Manter commits diários obrigatórios no repositório Git remoto acompanhados de backup da documentação na nuvem. |
| **R05** | **Escopo excessivo (*Scope Creep*)** | Tentativa de incluir módulos fiscais complexos ou marketplace fora do prazo da disciplina. | **Médio** | Congelar o escopo nos 4 módulos centrais definidos e registrar funcionalidades extras apenas como melhorias futuras. |
