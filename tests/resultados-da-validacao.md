# Relatório de Validação Funcional e Visual dos Protótipos — BarberFlow

**Data da Validação:** 18/11/2026  
**Branch de Validação:** `feature/validacao`  
**Artefatos Inspecionados:** `prototypes/html/visao-geral.html`, `prototypes/html/BarberFlow-visao-geral-unico.html` e `prototypes/html/tela1.html` a `tela5.html`.

---

## 1. Resumo Executivo da Validação

Foi realizada a inspeção técnica do código-fonte HTML/CSS/JS e da estrutura visual dos protótipos interativos (`S1` a `S5`), confrontando cada tela com os requisitos (`RF`/`RNF`) e regras de negócio (`RN`) extraídos do Pré-Projeto e do Documento A3.

- **Resultado Geral:** **Aprovado** para o escopo de prototipação e demonstração do fluxo principal (`S1`–`S5`).
- **Integridade de Assets:** Todas as referências de logotipo nos arquivos `tela1.html`, `tela2.html`, `tela3.html` e `visao-geral.html` apontam corretamente para `../imagens/logo.png` (e `BarberFlow-visao-geral-unico.html` possui imagem embutida em Base64).

---

## 2. Resultado Detalhado por Tela (`S1` a `S5`)

| Tela | Arquivo | Verificações Funcionais e Visuais Executadas | Status | Observações Técnicas |
| :--- | :--- | :--- | :---: | :--- |
| **Apresentação / Carrossel** | `visao-geral.html` | Carregamento dos 5 `iframe` (`tela1.html`–`tela5.html`), botões `prevBtn`/`nextBtn`, indicadores de paginação e atualização do título dinâmico via JavaScript. | **Aprovado** | Navegação linear funcional entre as 5 etapas da jornada. |
| **S1 — Catálogo & Profissional** | `tela1.html` | Exibição de profissional (*Carlos Silva — Barbeiro Sênior*), checkboxes de serviços (*Corte Social*, *Barba Completa*, *Corte + Barba*) com duração e preço, rodapé com total estimado e botão **Avançar**. | **Aprovado** | Seleção visual de múltiplos checkboxes funcional via CSS `:checked`; cálculo dinâmico do total e troca de barbeiro previstos para a camada JS/API em `/src`. |
| **S2 — Agenda & Horários** | `tela2.html` | Seletor de datas (`radio`), agrupamento por períodos (`Manhã`, `Tarde`, `Noite`), estados `Selecionado`, `Indisponível` (`disabled`) e `Bloqueado` (`disabled`), botão voltar (`aria-label="Voltar"`) e rodapé resumo. | **Aprovado** | Slots ocupados/bloqueados corretamente desabilitados no DOM (`disabled`), atendendo visualmente às regras `RN03` e `RN04`. |
| **S3 — Dados & Confirmação** | `tela3.html` | Cartão resumo tipo recibo, campos `#nome`, `#whatsapp` e `#obs` com `label`/`for`, alerta de reserva temporária por 10 minutos e botão **Confirmar Agendamento**. | **Aprovado** | Atributos `required`, máscara de telefone e trava atômica no servidor (`RN01`/`RN05`/`RN06`) serão implementados na fase de backend/JS. |
| **S4 — Agendamento Confirmado** | `tela4.html` | Ícone de confirmação, protocolo `#BF-45G2`, resumo de data/hora/profissional, endereço, tags de regras (`Tolerância de atraso: 10 minutos`, `Cancelamento grátis até 2h antes`) e botões de ação. | **Aprovado** | Layout alinhado às regras `RN07` e `RN08`; integração real com calendário e reagendamento/cancelamento previstas para `/src`. |
| **S5 — Painel do Barbeiro** | `tela5.html` | Cabeçalho com data/profissional e botão `Sair` (`aria-label="Sair"`), timeline com estados (`Concluído`, `Em Atendimento`, `Agendado`, `Espaço Bloqueado`), botão iniciar (`aria-label="Iniciar Atendimento"`) e botão **Bloquear Horário / Almoço**. | **Aprovado** | Fluxo visual completo e sem sobrecarga; ações persistentes conectadas ao banco de dados previstas para a etapa de implementação. |

---

## 3. Observações de Escopo Futuro (Roadmap Pós-Protótipo)

Durante a validação documental, confirmou-se que os módulos listados abaixo constam no Documento A3 como evolução do produto e permanecem **fora do escopo desta entrega de protótipos estáticos/visuais**:

1. **Autenticação e Controle de Acesso (RBAC):** tela de login excluída por definição da disciplina; perfis de acesso (*Proprietário/Gestor*, *Barbeiro* e *Cliente Final*) deverão ser aplicados na camada de API/sessão.
2. **Ficha do Cliente e Histórico Técnico de Cortes (Tela 4 do A3):** banco de conhecimento com numeração de lâminas, produtos e observações recorrentes por cliente.
3. **Módulo de Estoque e PDV (Tela 5 do A3):** venda de produtos de balcão (pomadas, bebidas), escolha de pagamento (Pix/Cartão) e baixa automática no estoque (`RN10`).
4. **Dashboard Gerencial e Financeiro (Tela 6 do A3):** gráficos de faturamento consolidado, ticket médio e taxa de retenção mensal exclusivos do proprietário.
5. **Persistência e Concorrência Real:** implementação em `/src` de validação de entrada (`RNF06`), transações atômicas contra duplo agendamento (`RN01`/`RNF05`) e cronômetro de reserva temporária de 10 minutos (`RN06`).
