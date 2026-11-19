# Modelo de Negócio e Análise de Mercado — BarberFlow

## 1. Problema e Justificativa

O projeto **BarberFlow** (*Sistema Web de Agendamento e Gestão para Barbearias Locais*) é direcionado ao segmento de **micro e pequenas barbearias de bairro**. Em estabelecimentos de contato direto e recorrente com o cliente, falhas operacionais afetam imediatamente a percepção de qualidade e o faturamento.

No cenário manual atual, grande parte das barbearias locais realiza agendamentos por mensagens no **WhatsApp** ou anotações em **cadernos físicos**, gerando um efeito dominó de gargalos:

- **Atendimento disperso:** troca assíncrona de mensagens sem visibilidade imediata de horários livres.
- **Choque de agenda:** agendamentos duplicados e sobreposição de horários para o mesmo profissional.
- **Ausências frequentes:** esquecimentos de horários marcados por parte dos clientes.
- **Queda produtiva:** o barbeiro precisa interromper cortes para responder o celular durante o atendimento.

---

## 2. Proposta de Valor e Pilares da Solução

O sistema substitui o fluxo manual por uma **interface web leve, responsiva e acessível por link exclusivo da barbearia** (sem necessidade de download de aplicativo pelo cliente), estruturada em quatro pilares centrais:

1. **Agendamento de serviços em tempo real:** seleção de serviço, profissional e horário disponível, com trava atômica contra conflitos de agenda e histórico do cliente.
2. **Banco de conhecimento de cortes:** ficha técnica com registro das preferências de cada cliente (numeração de máquina/lâminas, estilo e observações).
3. **Controle de estoque e vendas (PDV):** cadastro de produtos (ex.: pomadas, bebidas), baixa automática no estoque, seleção de formas de pagamento (ex.: Pix, Cartão) e faturamento por item vendido.
4. **Catálogo de serviços e relatórios mensais:** organização dos cortes por categoria, valor, duração estimada e complexidade, além de indicadores consolidados de receita, ticket médio, frequência de retorno e taxa de retenção.

---

## 3. Visão do Modelo de Negócio (Síntese Canvas)

| Bloco | Definição no BarberFlow |
| :--- | :--- |
| **Segmento de Clientes** | Micro e pequenas barbearias locais (negócios de bairro, de 1 a poucas cadeiras) e seus clientes finais via celular. |
| **Proposta de Valor** | Agendamento web em ~30 segundos sem download de app, fim dos choques de horário e gestão integrada (agenda, ficha, PDV e relatórios) com identidade própria da barbearia. |
| **Canais** | Link direto e exclusivo da barbearia (compartilhável via WhatsApp, Instagram e Google) acessado em navegadores móveis e desktop. |
| **Relacionamento com Clientes** | Autoatendimento rápido para o cliente final, envio de comprovante/protocolo e lembretes pelo contato cadastrado. |
| **Atividades-Chave** | Gestão de disponibilidade em tempo real, validação de concorrência, painel diário do barbeiro, controle de estoque/PDV e geração de relatórios. |
| **Recursos-Chave** | Aplicação web responsiva, banco de dados transacional, catálogo de serviços e base técnica de cortes por cliente. |
| **Parcerias-Chave** | Barbeiros parceiros/autônomos atuando no estabelecimento. |
| **Estrutura de Custos** | Desenvolvimento, hospedagem web/banco de dados e manutenção evolutiva da plataforma. |
| **Fontes de Receita** | Modelo enxuto e acessível para barbearias locais (posicionamento contra mensalidades elevadas e taxas sobre transações de marketplaces). |

---

## 4. Análise Comparativa de Concorrentes

| Concorrente | Referência | Forças | Fraquezas no Nicho | Diferencial do BarberFlow | Escopo Não Contemplado |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **AppBarber** | `appbarber.com.br` | Sistema completo para barbearias; controle financeiro, comissões e gestão de estoque integrada. | Curva de aprendizado alta para pequenos estabelecimentos; custos de assinatura elevados; interface poluída para agendamentos rápidos. | Interface enxuta, focada exclusivamente na rapidez do agendamento e acesso web sem download de aplicativo pesado pelo cliente. | Módulo avançado de emissão fiscal e controle complexo de estoque de insumos. |
| **Booksy** | `booksy.com` | Grande rede de estabelecimentos e usuários; marketplace com busca por geolocalização e avaliações públicas. | Plataforma genérica (não especializada em barbearias); cobrança de taxas sobre transações e diluição da identidade visual do barbeiro. | Link de agendamento direto e personalizado para a barbearia, preservando a marca e eliminando a exposição de concorrentes na mesma tela. | Sistema de marketplace público unificado com busca global por geolocalização. |
