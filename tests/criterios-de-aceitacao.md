# Critérios de Aceitação (BDD) — BarberFlow

Os critérios de aceitação abaixo seguem a sintaxe **BDD (`Dado / Quando / Então`)** para cada uma das cinco telas prototipadas (**`S1` a `S5`**), garantindo alinhamento entre os requisitos (`RF`/`RNF`), as regras de negócio (`RN`) e os protótipos HTML.

---

## Tela `S1` — Catálogo & Profissional (`tela1.html`)

### Cenário 1.1: Seleção de serviço e cálculo do total estimado
- **Dado** que o cliente acessou o link direto da barbearia na tela `S1` com o profissional selecionado (*Carlos Silva*),
- **Quando** o cliente seleciona um ou mais serviços do catálogo (ex.: *Corte Social* de 45 min por R$ 50,00 e *Barba Completa* de 30 min por R$ 35,00),
- **Então** o sistema deve destacar visualmente os cards escolhidos, atualizar o **Total Estimado** com a soma dos valores e considerar a duração acumulada ao avançar para a agenda (`RF01`, `RF02`, `RF03`, `RN02`).

### Cenário 1.2: Identidade própria sem download de aplicativo
- **Dado** que o cliente está utilizando um navegador móvel sem aplicativo instalado,
- **Quando** a página inicial `S1` é carregada,
- **Então** o sistema deve exibir o logotipo e a identidade visual da barbearia (`BarberFlow`) com layout responsivo e legível, sem exibir estabelecimentos concorrentes (`RNF01`, `RNF02`, `RNF09`).

---

## Tela `S2` — Agenda & Horários (`tela2.html`)

### Cenário 2.1: Seleção de data e horário livre
- **Dado** que o cliente avançou para a tela `S2` após selecionar profissional e serviços,
- **Quando** o cliente escolhe uma data (ex.: `16 Nov — Qua`) e clica em um horário disponível (ex.: `15:15` na grade da **Tarde**),
- **Então** o slot deve assumir o estado **Selecionado**, o resumo no rodapé deve exibir data, hora, profissional, serviços e valor total, e o botão **Continuar** deve encaminhar para `S3` (`RF04`, `RF05`, `RN03`).

### Cenário 2.2: Bloqueio de horários indisponíveis ou em pausa/almoço
- **Dado** que a grade de `S2` apresenta horários já reservados (`Indisponível`) e bloqueios manuais do barbeiro (`Bloqueado`),
- **Quando** o cliente tenta interagir com um horário marcado como `Indisponível` ou `Bloqueado`,
- **Então** o controle deve permanecer desabilitado (`disabled`), impedindo a seleção ou o avanço com aquele slot (`RF04`, `RN03`, `RN04`).

---

## Tela `S3` — Dados & Confirmação (`tela3.html`)

### Cenário 3.1: Confirmação com dados obrigatórios preenchidos dentro do prazo
- **Dado** que o cliente está na tela `S3` visualizando o recibo do agendamento e o aviso de **reserva temporária de 10 minutos**,
- **Quando** o cliente preenche corretamente **Nome Completo** e **WhatsApp (com DDD)**, opcionalmente inclui **Observações**, e aciona **Confirmar Agendamento** com o slot ainda disponível,
- **Então** o sistema deve validar a disponibilidade em transação atômica, gravar o agendamento na agenda do barbeiro e exibir a tela de confirmação `S4` (`RF05`, `RF06`, `RF07`, `RN01`, `RN05`, `RN06`).

### Cenário 3.2: Impedimento por ausência de dados obrigatórios ou conflito de horário
- **Dado** que o cliente está na tela `S3`,
- **Quando** o cliente tenta confirmar sem informar Nome ou WhatsApp válidos, **ou** quando o horário foi ocupado simultaneamente por outro cliente,
- **Então** o sistema deve bloquear a confirmação, exibir aviso claro do erro (campo obrigatório ou choque de horário) e manter o cliente na etapa para correção ou escolha de novo slot (`RF06`, `RF07`, `RN01`, `RN05`, `RNF06`).

---

## Tela `S4` — Agendamento Confirmado (`tela4.html`)

### Cenário 4.1: Exibição de comprovante, protocolo e regras da reserva
- **Dado** que o agendamento foi validado e gravado com sucesso,
- **Quando** a tela `S4` é apresentada ao cliente,
- **Então** o sistema deve exibir o protocolo único (ex.: `#BF-45G2`), a data/hora, o nome do barbeiro, o endereço da barbearia, os avisos de **Tolerância de atraso: 10 minutos** e **Cancelamento grátis até 2h antes**, além dos botões **Adicionar ao Calendar** e **Novo Agendamento** (`RF08`, `RN07`, `RN08`).

---

## Tela `S5` — Painel do Barbeiro (`tela5.html`)

### Cenário 5.1: Acompanhamento da linha do tempo e atualização de status
- **Dado** que o barbeiro acessou o **Painel do Barbeiro** (`S5`) com sua agenda diária carregada,
- **Quando** o profissional visualiza os atendimentos em ordem cronológica e aciona iniciar atendimento em um item `Agendado`,
- **Então** o painel deve refletir os estados `Concluído`, `Em Atendimento`, `Agendado` e `Espaço Bloqueado`, permitindo evoluir o atendimento atual sem choques manuais (`RF09`, `RN09`).

### Cenário 5.2: Registro de bloqueio de horário / almoço
- **Dado** que o barbeiro precisa reservar uma pausa ou horário de almoço na sua agenda,
- **Quando** ele aciona o botão **Bloquear Horário / Almoço** no rodapé do painel `S5`,
- **Então** o intervalo selecionado deve constar como **Espaço Bloqueado** no painel interno e passar a ser exibido como **Bloqueado** (desabilitado) na grade pública `S2` (`RF09`, `RN04`).
