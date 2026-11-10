---
title: Custo das mensagens
description: Como funciona a cobrança das mensagens de template na WhatsApp Business API (WABA).
---

## Resumo rápido

* A **janela de atendimento de 24 horas** abre quando o usuário envia uma mensagem para você.
* Dentro dessa janela, você pode responder com **mensagens livres**.
* Fora da janela de 24 horas, você só pode enviar **mensagens de template**.
* **Templates de marketing são sempre pagos**, mesmo dentro da janela de 24 horas.
* **Templates de utilidade são sempre pagos**, mesmo dentro da janela de 24 horas.
* **Templates de autenticação** (OTP, códigos de verificação) são cobrados separadamente pela Meta.
* Aplicamos os preços oficiais da Meta com um **acréscimo de só 5%**, enquanto a maioria dos provedores cobra cerca de **15%**.

## O que é a janela de 24 horas

Quando o usuário envia qualquer mensagem para você, o WhatsApp abre uma janela de atendimento de 24 horas.

Exemplo: o cliente mandou uma mensagem às 11:00

`"Olá, cadê o meu pedido?"`

Até as 11:00 do dia seguinte, a empresa pode:

* enviar mensagens livres;
* responder sem templates;
* conversar livremente dentro da sessão.

## Tipos de mensagens de template

| Categoria | Para que serve |
| --- | --- |
| Marketing | Promoções, descontos, campanhas |
| Utility | Atualizações de pedido, recibos, notificações |
| Authentication | OTP, códigos de login, 2FA |

### Preços

[Custo por mensagem em USD na WhatsApp Business Platform, a partir de 1º de outubro de 2026 (XLSX)](./assets/whatsapp-rates-2026-10-01.xlsx)

### 1. Templates de marketing

Templates de marketing são **SEMPRE** pagos. Mesmo que o usuário tenha escrito para você há um minuto.

### 2. Templates de utilidade

Templates de utilidade também são **SEMPRE** pagos. Mesmo que o usuário tenha escrito para você há um minuto.

### 3. Templates de autenticação

* podem ser enviados fora da janela de 24 horas;
* são sempre cobrados;
* costumam ser mais baratos que os de marketing;
* têm casos de uso bem restritos.

## Quanto custa cada mensagem

| Tipo de mensagem | Dentro da janela de 24 h | Fora da janela de 24 h |
| --- | --- | --- |
| Mensagem livre | As primeiras 1.000 mensagens recebidas são grátis; as demais são cobradas. | Não permitido |
| Template de marketing | Pago | Pago |
| Template de utilidade | Pago | Pago |
| Template de autenticação | Pago (tarifa da Meta) | Pago (tarifa da Meta) |

## Regra importante

Mensagens livres:

* só podem ser enviadas dentro da janela de 24 horas;
* não podem ser enviadas fora da janela.

Depois que a janela fecha, **os templates são obrigatórios**.

## Modelo de preços na nossa plataforma

Usamos os preços oficiais da Meta. Por cima deles, a plataforma aplica um **acréscimo de só 5%**, bem abaixo da média do mercado (\~15%).
