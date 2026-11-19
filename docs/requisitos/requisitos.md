# Especificação de Requisitos — BarberFlow

Este documento consolida os **Requisitos Funcionais (RF)** e os **Requisitos Não Funcionais (RNF)** do **Sistema Web de Agendamento e Gestão para Barbearias Locais (BarberFlow)**, extraídos da documentação de Pré-Projeto, do Documento A3 (Squad 01 — UNISOCIESC, 2026) e validados contra o protótipo interativo (`S1` a `S5`).

---

## 1. Escopo: Prototipado vs. Módulos Futuros (A3)

Conforme diretriz acadêmica da disciplina de Garantia da Qualidade de Software, a prototipação inicial concentrou-se nas telas funcionais do fluxo principal de agendamento e operação diária (excluindo tela de login), enquanto os demais módulos especificados no A3 compõem o roadmap evolutivo da aplicação:

| Categoria | Telas / Módulos | Público-Alvo | Status no Repositório |
| :--- | :--- | :--- | :--- |
| **Escopo Prototipado (MVP)** | `S1` Catálogo & Profissional (`tela1.html`) | Cliente Final | Prototipado em HTML/CSS |
| **Escopo Prototipado (MVP)** | `S2` Agenda & Horários (`tela2.html`) | Cliente Final | Prototipado em HTML/CSS |
| **Escopo Prototipado (MVP)** | `S3` Dados & Confirmação (`tela3.html`) | Cliente Final | Prototipado em HTML/CSS |
| **Escopo Prototipado (MVP)** | `S4` Agendamento Confirmado (`tela4.html`) | Cliente Final | Prototipado em HTML/CSS |
| **Escopo Prototipado (MVP)** | `S5` Painel do Barbeiro (`tela5.html`) | Barbeiro / Equipe | Prototipado em HTML/CSS |
| **Módulo Futuro (A3)** | Ficha do Cliente e Histórico de Cortes (Tela 4 do A3) | Barbeiro / Gestor | Especificado (Planejado) |
| **Módulo Futuro (A3)** | Controle de Estoque e PDV (Tela 5 do A3) | Barbeiro / Gestor | Especificado (Planejado) |
| **Módulo Futuro (A3)** | Dashboard Gerencial e Financeiro (Tela 6 do A3) | Proprietário / Gestor | Especificado (Planejado) |

---

## 2. Requisitos Funcionais (RF)

### 2.1 Escopo Prototipado (Jornada `S1` a `S5`)

| ID | Requisito Funcional | Descrição | Origem / Tela |
| :--- | :--- | :--- | :--- |
| **RF01** | Seleção de profissional | O sistema deve permitir ao cliente visualizar o profissional selecionado (ex.: nome e cargo, como *Carlos Silva — Barbeiro Sênior*) e acionar a troca/alteração do barbeiro antes de escolher o horário. | `S1` (`tela1.html`) / A3 |
| **RF02** | Catálogo de serviços com preço e duração | O sistema deve exibir os serviços disponíveis com título, duração estimada em minutos e valor monetário (ex.: *Corte Social — 45 min — R$ 50*; *Barba Completa — 30 min — R$ 35*; *Corte + Barba — 75 min — R$ 80*), permitindo seleção única ou combinada. | `S1` (`tela1.html`) / A3 |
| **RF03** | Cálculo dinâmico do total estimado | O sistema deve calcular e exibir em tempo real o valor total estimado (e a duração total associada) conforme os serviços selecionados pelo cliente. | `S1` (`tela1.html`) / A3 |
| **RF04** | Seleção de data e grade de horários em tempo real | O sistema deve apresentar um seletor de datas e uma grade de horários segmentada por período (**Manhã**, **Tarde**, **Noite**), diferenciando visualmente horários disponíveis, selecionados, **Indisponíveis** e **Bloqueados**. | `S2` (`tela2.html`) / Fluxograma |
| **RF05** | Resumo contínuo da reserva antes da confirmação | O sistema deve exibir o resumo da seleção (data, hora, profissional, serviços e total) no rodapé de `S2` e em formato de recibo no topo de `S3` para conferência do cliente. | `S2` e `S3` (`tela2.html`, `tela3.html`) |
| **RF06** | Coleta de dados do cliente e observações | O sistema deve disponibilizar formulário para preenchimento obrigatório de **Nome Completo** e **WhatsApp (com DDD)**, além de campo opcional de **Observações** (ex.: preferência de pente/máquina). | `S3` (`tela3.html`) / A3 |
| **RF07** | Reserva temporária e validação de concorrência | Ao avançar para a confirmação, o sistema deve sinalizar reserva temporária de **10 minutos** para conclusão e validar em tempo real no servidor se o slot segue livre antes de gravar na agenda do profissional, exibindo alerta e solicitando novo horário em caso de indisponibilidade. | `S3` (`tela3.html`) / Fluxograma / A3 |
| **RF08** | Emissão de comprovante e protocolo da reserva | Após confirmação, o sistema deve gerar um código de protocolo único (ex.: `#BF-45G2`), exibir data, hora, profissional, endereço do estabelecimento e políticas de atraso/cancelamento, além de botões para **Adicionar ao Calendar** e iniciar **Novo Agendamento** (bem como opções de cancelamento/reagendamento previstas no A3). | `S4` (`tela4.html`) / A3 |
| **RF09** | Painel Diário do Barbeiro (Linha do tempo) | O sistema deve apresentar ao profissional uma timeline cronológica dos atendimentos do dia com horário, nome do cliente, serviços, valor e status (`Concluído`, `Em Atendimento`, `Agendado` e `Espaço Bloqueado`), permitindo iniciar o próximo atendimento e realizar bloqueio manual de horário/almoço. | `S5` (`tela5.html`) / A3 |

### 2.2 Módulos Futuros Previstos no A3 (Roadmap Evolutivo)

| ID | Requisito Funcional | Descrição | Módulo / Ator |
| :--- | :--- | :--- | :--- |
| **RF10** | Ficha do cliente e histórico técnico de cortes | O sistema deve manter um banco de conhecimento por cliente registrando cortes anteriores, numeração de máquina/lâminas utilizadas, produtos aplicados e observações técnicas para consulta pré-atendimento. | Ficha e Histórico (Barbeiro / Gestor) |
| **RF11** | Controle de estoque e PDV (Vendas de balcão) | O sistema deve permitir cadastrar produtos (ex.: pomadas, bebidas), registrar vendas de balcão com seleção da forma de pagamento (ex.: Pix, Cartão) e efetuar baixa automática no estoque no banco de dados. | Estoque e PDV (Barbeiro / Gestor) |
| **RF12** | Dashboard gerencial, financeiro e relatórios mensais | O sistema deve gerar indicadores exclusivos para o proprietário, incluindo faturamento consolidado (serviços + itens vendidos), ticket médio, produtividade por barbeiro, frequência de retorno e taxa de retenção mensal de clientes. | Dashboard Gerencial (Proprietário / Gestor) |
| **RF13** | Gestão de catálogo, preços e equipe | O sistema deve permitir ao Proprietário/Gestor configurar dados gerais da barbearia, cadastrar/editar serviços (categoria, valor, duração e complexidade) e gerenciar os perfis da equipe de barbeiros. | Administração (Proprietário / Gestor) |
| **RF14** | Lembretes automáticos via contato cadastrado | O sistema deve disparar lembretes de agendamento para o WhatsApp informado pelo cliente visando reduzir faltas e esquecimentos. | Notificações (Cliente Final) |

---

## 3. Requisitos Não Funcionais (RNF)

| ID | Categoria | Requisito Não Funcional | Critério / Justificativa |
| :--- | :--- | :--- | :--- |
| **RNF01** | **Usabilidade** | Acesso direto via navegador sem download de aplicativo | O cliente deve acessar o agendamento por link exclusivo da barbearia diretamente no navegador móvel, concluindo uma reserva em poucos passos (meta de ~30 segundos no fluxo principal). |
| **RNF02** | **Usabilidade** | Interface responsiva *mobile-first* e enxuta | O layout deve priorizar telas de smartphones com hierarquia visual clara, evitando poluição informacional para usuários leigos e barbeiros acostumados ao atendimento manual. |
| **RNF03** | **Acessibilidade** | Semântica HTML, contraste e navegação assistiva | As interfaces devem empregar elementos HTML semânticos (`header`, `main`, `section`, `footer`), atributos `aria-label` em botões icônicos (voltar, sair, iniciar atendimento), associação explícita `label`/`for` nos campos de formulário e contraste legível entre texto, fundo e estados desabilitados. |
| **RNF04** | **Desempenho** | Carregamento leve e resposta rápida de disponibilidade | As páginas públicas devem ser leves e a consulta/validação da grade de horários em tempo real deve responder rapidamente para evitar desistência durante o agendamento no celular. |
| **RNF05** | **Confiabilidade / Concorrência** | Transação atômica contra duplo agendamento | A confirmação de reserva e a baixa de estoque devem utilizar controle transacional no banco de dados para impedir choques de horário simultâneos ou inconsistência de inventário. |
| **RNF06** | **Segurança** | Validação e sanitização de entradas | Todos os formulários (nome, WhatsApp, observações) devem validar formato e sanitizar entradas no cliente e no servidor para prevenir corrupção de dados e injeção de código. |
| **RNF07** | **Segurança** | Controle de acesso por perfil (RBAC) | O sistema deve segregar permissões conforme o organograma: **Proprietário/Gestor** (acesso irrestrito e relatórios financeiros), **Barbeiro/Equipe** (agenda pessoal, bloqueios, ficha e PDV) e **Cliente Final** (apenas fluxo público de agendamento). |
| **RNF08** | **Manutenibilidade** | Padronização de código, versionamento e testes | O projeto deve seguir arquitetura separada por camadas (`/docs`, `/prototypes`, `/src`, `/tests`), fluxo Git (`main`, `develop`, `feature/*`) e cobertura planejada de testes unitários, de integração, E2E, usabilidade e segurança. |
| **RNF09** | **Identidade Visual** | Preservação da marca própria da barbearia | Diferentemente de marketplaces genéricos, o link exclusivo deve preservar a identidade visual e o logotipo da barbearia sem exibir concorrentes na mesma tela. |
| **RNF10** | **Portabilidade** | Compatibilidade multi-navegador | O sistema web e os protótipos devem funcionar corretamente nos principais navegadores modernos em dispositivos móveis (Android/iOS) e desktop. |
