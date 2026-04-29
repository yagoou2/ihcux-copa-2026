# CopaNaMao 📱⚽
**App Oficial do Torcedor na Arena — Copa do Mundo 2026**

> Protótipo de Baixa Fidelidade | IHC & UX — Centro Universitário UNA

---

## 👤 Integrante

**Yago Soares Costa**
Professor: Daniel Henrique Matos de Paiva

---

## 🎯 Problema Focado

### Qual dor do torcedor priorizamos resolver?

A maior dor identificada é o **conflito entre sair para buscar comida e perder momentos do jogo**. O torcedor enfrenta:

- Filas de 15–30 minutos nos quiosques
- Risco de perder um gol enquanto está fora do assento
- Desorientação em arenas com 60.000+ pessoas (portões, banheiros, setor)
- Nenhuma forma de rever um lance polêmico na hora

O **CopaNaMao** resolve isso com pedido de comida sem sair do assento, notificação de retirada no momento certo, replay multicâmera imediato e mapa GPS da arena.

---

## 🏗 Justificativa de Design

**Por que as informações foram organizadas desta forma?**

| Decisão | Motivo |
|---|---|
| **Botões grandes (mín. 44px)** | Ambiente de estádio = movimento, frio, luvas, distrações. Facilita toque impreciso |
| **Placar no topo da Home** | É o principal motivo do torcedor estar ali — aparece antes de qualquer outra info |
| **4 atalhos rápidos na Home** | Cobrem 80% dos casos de uso em 1 toque, sem precisar navegar por menus |
| **Banner de notificação proativo** | Torcedor não precisa ficar abrindo o app — recebe aviso de pedido pronto automaticamente |
| **GPS com rota no Mapa** | Torcedor não precisa saber o layout do estádio; app guia passo a passo |
| **Replay multicâmera** | Mantém o torcedor engajado mesmo quando saiu do assento brevemente |
| **Mínimo de toques** | Pedido completo: 3 toques. Emergência: 2 toques. Reduz fricção em momento de stress |
| **Modo Emergência visível** | Botão 🚨 fixo na Home — nunca escondido em menus secundários |

---

## 📱 Descrição das Telas

### Tela 1 — Home / Dashboard
Ponto de entrada do app. Exibe o **placar ao vivo** como elemento principal (maior na tela), quatro atalhos grandes (Mapa, Pedir Lanche, Replay, Emergência), banner de notificação proativo e miniaturas dos últimos replays. A hierarquia privilegia o placar e a ação mais urgente do momento.

### Tela 2 — Mapa do Estádio
Mapa interativo com representação do campo e setores. Mostra a **posição GPS do usuário** em tempo real, pontos de interesse (banheiros, lanchonetes, portões, segurança) e botão de "Traçar Rota" para o assento ou portão de saída. Chips permitem filtrar o tipo de POI exibido.

### Tela 3 — Cardápio Digital
Lista de alimentos e bebidas disponíveis no setor do usuário. Toggle no topo alterna entre **Retirar no Balcão** ou **Receber no Assento**. Chips de categoria filtram o cardápio. Cada item tem foto (placeholder), nome, descrição e botão `+` grande para adicionar ao carrinho. Banner fixo no rodapé exibe o total e acessa o carrinho.

### Tela 4 — Carrinho / Pagamento
Resumo do pedido com controles de quantidade (+/-), escolha do tipo de entrega, breakdown de valores e seleção de forma de pagamento (PIX, Crédito, Débito, Vale-Refeição). O botão **CONFIRMAR PEDIDO** é o maior elemento da tela, com tempo estimado de preparo logo abaixo.

### Tela 5 — Central de Replays
Replay em destaque com player de vídeo (placeholder), chips de seleção de ângulo de câmera (Principal, Trave, VAR, Visão 360) e barra de progresso. Abaixo, lista de lances recentes com thumbnail, título e timestamp. Strip inferior acessa as Estatísticas ao Vivo.

### Tela 6 — Perfil / Ingresso
Avatar e dados do usuário, **QR Code do ingresso** em destaque (grande para fácil leitura pelos fiscais), informações do evento (setor, fila, assento, portão de entrada) e botão de traçar rota até o portão correto.

### Extra 1 — Modo Acessibilidade
Interface de alto contraste (branco sobre preto), fonte aumentada em 20%, botão de microfone central e proeminente, lista de **comandos de voz pré-definidos** ("onde fica o banheiro?", "pedir hot dog", "ver o gol de novo", "emergência"). Área de feedback auditivo/textual na base da tela.

### Extra 2 — Fluxo de Emergência
Acionado pelo botão 🚨 na Home. Exibe a **localização exata automaticamente** (Setor/Fila/Assento), mini-mapa de confirmação e dois botões grandes: "SIM — ENVIAR LOCALIZAÇÃO" e "Cancelar — Falso Alarme". Após envio: ETA do fiscal mais próximo. Fluxo completo em apenas 2 toques.

---

## 🗺 Fluxo do Usuário

### Pedindo um Lanche
```
1. Home  →  toca em "PEDIR LANCHE"
2. Cardápio  →  escolhe item, toca em "+"
3. Toca no banner "Ver Carrinho (2 itens)"
4. Carrinho  →  revisa pedido, escolhe "Retirar no Balcão B3"
5. Toca em "CONFIRMAR PEDIDO"
6. Notificação push: "🍔 Seu pedido está pronto! Retire no B3"
7. Torcedor retira sem perder o jogo ✅
```

### Vendo um Replay
```
1. Home  →  toca em "REPLAY" ou em thumbnail de lance
2. Central de Replays  →  replay inicia automaticamente
3. Escolhe ângulo de câmera (chips: Principal / Trave / VAR / 360)
4. Controla com barra de progresso, replay em câmera lenta
5. Opcional: acessa "Estatísticas ao Vivo" do jogador
6. Retorna ao Home ✅
```

### Situação de Emergência
```
1. Home  →  toca em "🚨 EMERGÊNCIA"
2. Tela Emergência  →  localização carregada automaticamente
3. Confirma: "SIM — ENVIAR LOCALIZAÇÃO"
4. Fiscal mais próximo notificado com Setor/Fila/Assento
5. Torcedor recebe ETA: "Fiscal chegará em ~3 min" ✅
```

---

## 📁 Estrutura do Repositório

```
ihcux-copa-2026/
├── /prototipo
│   ├── prototipo.pdf       ← Protótipo completo (8 telas)
│   └── prototipo.png       ← Exportação da tela principal
└── README.md
```

---

## 🛠 Ferramenta e Processo

- Wireframes criados seguindo o padrão **Low-Fidelity** (tons de cinza, sem elementos gráficos refinados)
- Foco em **usabilidade sob pressão**: botões grandes, leitura clara, mínimo de toques
- Fluxo de navegação indicado por setas tracejadas
- Hierarquia visual: elemento mais importante = maior e mais alto na tela

---

*IHC & UX — Atividade Prática: Prototipagem de Baixa Fidelidade | Copa do Mundo 2026*
