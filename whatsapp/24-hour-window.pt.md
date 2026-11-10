---
title: Janela de 24 horas
description: Quando você pode enviar qualquer mensagem para um cliente no WhatsApp e quando só serve um template aprovado.
---

A janela de 24 horas é o período em que a empresa pode enviar qualquer mensagem para o cliente depois do último contato dele. Com a janela aberta, não é preciso usar templates pagos. Com ela fechada, só dá para escrever com um template pago aprovado.

É uma regra da Meta, não da 1MSG: funciona igual em todos os provedores da WhatsApp Business API.

## Como a janela funciona

1. **A janela abre** quando o cliente escreve para a empresa. Pode ser qualquer coisa: uma pergunta, um pedido ou só um “oi”.
2. A partir da **última** mensagem recebida, a empresa tem 24 horas para enviar mensagens. Nesse tempo dá para conversar normalmente: enviar qualquer mensagem dentro das políticas do WhatsApp, sem templates pagos.
3. **Depois de 24 horas** da última mensagem recebida, a janela fecha. A partir daí, não dá para enviar mensagens livres até o cliente escrever de novo.
4. **Com a janela fechada**, você só pode enviar templates pagos aprovados.
5. **Para reabrir a janela**, o cliente precisa mandar uma nova mensagem. Aí a contagem recomeça: mais 24 horas de conversa livre.

Exemplo: o cliente escreveu às 11:00, então até as 11:00 do dia seguinte você pode responder livremente.

As mensagens da própria empresa não abrem nem prolongam a janela.

As mensagens enviadas pelo app WhatsApp Business também não abrem nem prolongam a janela: ela existe só para mensagens pela Cloud API.

## O que dá para fazer com a janela aberta

Qualquer mensagem dentro das políticas do WhatsApp: texto, arquivos, imagens, botões, listas. Não é preciso template.

## O que fazer com a janela fechada

Envie um template aprovado. Escolha a categoria conforme a situação:

* **MARKETING** — iniciar uma conversa, anunciar uma promoção ou um produto novo, pedir feedback;
* **UTILITY** — mensagens sobre ações do cliente: confirmação de pedido ou pagamento, status da assinatura;
* **AUTHENTICATION** — códigos de uso único para cadastro, login ou recuperação de acesso.

Passo a passo:

1. A janela está fechada → envie um template.
2. O cliente responde → a janela está aberta.
3. Nas próximas 24 horas, converse livremente.

Mais sobre templates na seção sobre criar e enviar templates.

## Quanto custa

Janela aberta não quer dizer “grátis”. Desde 1º de julho de 2025, a Meta cobra por cada mensagem de template entregue, e não pela conversa. Na janela, mensagens livres dispensam template, mas templates de utilidade (UTILITY) e de marketing são sempre pagos, mesmo na janela.

Detalhes em [Custo das mensagens](../platform/billing/messaging-costs.pt.md).

## Próximos passos

* [Início rápido](../platform/quickstart.pt.md)
* Criar e enviar templates
* [Custo das mensagens](../platform/billing/messaging-costs.pt.md) — tarifas e categorias de templates
* [Referência da API](https://docs.1msg.io/) — métodos `/sendMessage` e `/sendTemplate`
