---
title: Preços e cobrança
description: Como a assinatura da plataforma e o saldo das sessões do WhatsApp são pagos, cobrados e recarregados.
---

Na plataforma, você paga por duas coisas diferentes:

1. Assinatura da plataforma — paga pelo Stripe
2. Saldo das sessões de conversa do WhatsApp (WABA) — gerenciado separadamente da assinatura

> [!NOTE]
> A assinatura não é cobrada do saldo. O saldo é usado só para as cobranças das sessões de conversa do WhatsApp.

## Assinatura pelo Stripe

As assinaturas da plataforma são processadas pelo Stripe Billing.

Depois de assinar, você gerencia a assinatura no Stripe Customer Portal, que abre pela seção [Billing](https://platform.1msg.io/manage/billing) da plataforma.

No Customer Portal você pode:

* ver o plano atual
* trocar de plano
* cancelar a assinatura
* renovar ou reativar a assinatura
* atualizar o cartão
* alterar o endereço e os dados de cobrança
* ver faturas e recibos
* baixar faturas em PDF
* tentar de novo pagamentos que falharam

Tudo o que envolve a assinatura é feito direto no Stripe Customer Portal.

Mais sobre os planos em [Planos de assinatura](./subscription-plans.pt.md).

## Saldo das sessões de conversa do WhatsApp (WABA)

O saldo é usado exclusivamente para as cobranças das sessões de conversa do WhatsApp pela WABA.

A plataforma usa cobrança pós-paga: as sessões de conversa são cobradas depois do uso real.

Se o saldo ficar negativo, na próxima cobrança ou recarga bem-sucedida:

* a dívida é descontada primeiro
* depois o valor restante é creditado no saldo

Exemplo:

* se o saldo está em `-3 USD`
* e é feita uma cobrança automática ou recarga de `10 USD`

então:

* `3 USD` cobrem a dívida
* `10 USD` são creditados no saldo

## Como as cobranças são calculadas

Uma vez por hora, o sistema calcula quanto custaram as sessões de conversa e cobra esse valor.

O preço depende da categoria da conversa:

* Marketing
* Utility
* Authentication / Authorization

Os preços atuais estão em um documento separado.

* [Custo das mensagens](./messaging-costs.pt.md)

## Saldo negativo e bloqueio do canal

Se o saldo ficar negativo, o sistema tenta cobrar automaticamente o cartão vinculado.

Na cobrança automática:

* primeiro o saldo negativo é coberto
* depois são cobrados mais `10 USD` para o saldo voltar a ficar positivo

É feita só uma tentativa de cobrança automática.

* Se o pagamento passar, o saldo é restaurado automaticamente
* Se o pagamento falhar, o canal fica bloqueado até o saldo ser recarregado manualmente

Para o canal não parar, mantenha o saldo positivo ou ative a Recarga automática.

## Recarga automática

Para o saldo não ficar negativo, ative a Recarga automática (Auto Top-Up).

Ao configurar a Recarga automática, informe:

* o limite mínimo do saldo
* o valor da recarga

Quando o saldo fica abaixo do limite configurado, o sistema cobra o cartão automaticamente e recarrega o saldo.

### Quando a Recarga automática falha

Para cada recarga automática, o sistema faz até 3 tentativas de pagamento.

* Se uma das tentativas passar, o saldo é recarregado automaticamente
* Se as 3 tentativas falharem, a Recarga automática é desativada para o método de pagamento atual

Se depois disso o saldo ficar negativo, o canal pode ser suspenso até o saldo ser recarregado manualmente.

## Recarga manual do saldo

O saldo pode ser recarregado separadamente da assinatura da plataforma.

O dinheiro do saldo é usado só para as sessões de conversa do WhatsApp.

A assinatura da plataforma continua sendo cobrada separadamente, pelo Stripe Subscription Billing.
