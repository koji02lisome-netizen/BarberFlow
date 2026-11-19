# Matriz de Rastreabilidade de Testes — BarberFlow

Esta matriz estabelece o mapeamento bidirecional entre os **Requisitos Funcionais (`RF`)**, **Requisitos Não Funcionais (`RNF`)**, **Regras de Negócio (`RN`)**, as telas prototipadas (`S1`–`S5`) e os **Casos de Teste (`CT`)** definidos para validação do projeto **BarberFlow**.

---

## 1. Rastreabilidade: Escopo Prototipado (`S1` a `S5`)

| Requisito / Regra | Descrição Resumida | Tela / Artefato | Casos de Teste (`CT`) | Nível de Teste Planejado (A3) |
| :--- | :--- | :--- | :--- | :--- |
| **RF01** | Seleção e troca do profissional | `S1` (`tela1.html`) | `CT01` | Funcional (E2E) / Usabilidade |
| **RF02 / RN02** | Catálogo com preço e duração por serviço | `S1` (`tela1.html`) | `CT01`, `CT02` | Unitário / Funcional (E2E) |
| **RF03 / RN02** | Cálculo dinâmico do total estimado e seleção múltipla | `S1` (`tela1.html`) | `CT02` | Unitário / Funcional (E2E) |
| **RF04 / RN03** | Grade de horários por período vinculada à agenda do barbeiro | `S2` (`tela2.html`) | `CT03`, `CT04` | Integração / Funcional (E2E) |
| **RN04** | Exibição de horários bloqueados/almoço e indisponíveis | `S2` (`tela2.html`) / `S5` (`tela5.html`) | `CT04`, `CT10` | Integração / Funcional (E2E) |
| **RF05** | Resumo contínuo da reserva em `S2` e recibo em `S3` | `S2`, `S3` (`tela2.html`, `tela3.html`) | `CT03`, `CT05` | Funcional (E2E) / Usabilidade |
| **RF06 / RN05** | Preenchimento obrigatório de Nome e WhatsApp e opcional de Observações | `S3` (`tela3.html`) | `CT05`, `CT06` | Funcional (E2E) / Segurança |
| **RF07 / RN01 / RN06** | Reserva temporária de 10 min e trava contra reserva duplicada | `S3` (`tela3.html`) | `CT07`, `CT08` | Integração / Concorrência |
| **RF08 / RN07 / RN08** | Comprovante, protocolo, tolerância de 10 min e cancelamento grátis até 2h | `S4` (`tela4.html`) | `CT09` | Funcional (E2E) / Usabilidade |
| **RF09 / RN09 / RN04** | Painel Diário do Barbeiro, transição de status e bloqueio de horário/almoço | `S5` (`tela5.html`) | `CT10`, `CT11` | Funcional (E2E) / Integração |
| **RNF01 / RNF02 / RNF09** | Acesso via navegador, layout *mobile-first* e identidade visual própria | `visao-geral.html`, `S1`–`S5` | `CT12` | Usabilidade |
| **RNF03 / RNF10** | Semântica HTML, `aria-label`, `label`/`for`, contraste e renderização | `visao-geral.html`, `S1`–`S5` | `CT12`, `CT13` | Usabilidade / Acessibilidade |

---

## 2. Cobertura Planejada para Módulos Futuros (Escopo A3)

Os itens abaixo pertencem ao roadmap evolutivo especificado no Documento A3 e ainda não possuem telas implementadas em `prototypes/html/`:

| Requisito / Regra | Módulo Futuro (A3) | Estratégia de Teste Prevista (Tabela 5 do A3) |
| :--- | :--- | :--- |
| **RF10** | Ficha do Cliente e Histórico Técnico de Cortes | Testes de Integração (persistência) e Funcionais (consulta pré-atendimento). |
| **RF11 / RN10** | Controle de Estoque e PDV (baixa automática) | Testes Unitários (cálculo de estoque/pagamento) e Integração transacional. |
| **RF12** | Dashboard Gerencial e Relatórios Mensais | Testes Unitários (ticket médio/retenção) e Restrição de Acesso (RBAC `RNF07`). |
| **RF13** | Gestão de Catálogo, Preços e Equipe | Testes Funcionais e Controle de Acesso exclusivo do Proprietário/Gestor (`RNF07`). |
| **RF14** | Lembretes Automáticos via WhatsApp | Testes de Integração com serviço de mensageria e agendamento de disparos. |
