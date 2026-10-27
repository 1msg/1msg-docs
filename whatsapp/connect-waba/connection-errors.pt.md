---
title: Erros ao conectar a WABA
description: "Como resolver erros após conectar a WABA: o número não está vinculado à conta do WhatsApp ou o método de pagamento falha."
---

## The number is not linked to the WhatsApp account

O canal do WhatsApp foi bloqueado pela Meta.

Siga os dois passos abaixo, nesta ordem.

**1. Confirme o número de novo no WhatsApp Manager**

O número não está confirmado no momento, então este passo é obrigatório.

1. Abra o [WhatsApp Manager](https://business.facebook.com/wa/manage/home/) com o usuário do Facebook que administra a conta WhatsApp Business correspondente.
2. Abra a seção de números de telefone e selecione o número certo.
3. Peça um novo código de confirmação por SMS ou chamada de voz e digite-o. Você precisa conseguir receber o SMS ou a ligação nesse número.
4. Espere até o número aparecer como confirmado. Se o nome de exibição já estiver aprovado, não é preciso alterá-lo.

**2. Defina o PIN do WhatsApp na 1MSG**

1. Abra [platform.1msg.io](https://platform.1msg.io/) e entre na sua conta.
2. Abra o canal correspondente.
3. No topo da tela você verá o banner **Complete WhatsApp setup: PIN not set**. Clique em **Set PIN**.

   ![Banner Complete WhatsApp setup: PIN not set com o botão Set PIN](./assets/pin-not-set-banner.png)
4. Digite um PIN de 6 dígitos. Se o PIN já foi criado no WhatsApp Manager, use o mesmo. Se ainda não existir, os dígitos que você digitar passam a ser o seu PIN. Guarde-o. A 1MSG não armazena o PIN e não consegue mostrá-lo depois.
5. Confirme que o PIN foi salvo e clique em **Continue**.

Depois dos dois passos, atualize a página **Status** do canal. O status **External WABA channel** não deve mais aparecer como **blocked**.

Se algo não ficar claro ou surgir um problema, fale com [o suporte](../../platform/support.pt.md) e envie capturas de tela — vamos ajudar a resolver.

## There is an error with the payment method. This will block business-initiated conversations

A mensagem `There is an error with the payment method` significa que a Meta não consegue cobrar pelos envios de mensagens do WhatsApp. Os modelos de mensagem (templates) e a primeira mensagem para o cliente não serão enviados. As respostas em uma conversa já aberta ainda poderão ser enviadas.

É necessário cadastrar um cartão na Meta. A assinatura da 1MSG não cobre esses custos.

**Onde acessar**

Entre no Facebook com a conta que gerencia essa conta do WhatsApp.

1. Acesse o [Meta Business Suite](https://business.facebook.com/) → Settings (Configurações).
2. No canto superior esquerdo, selecione a empresa à qual essa conta do WhatsApp pertence.
3. Acesse Billing & payments → Accounts → selecione a conta desse canal → Add payment method.
4. Adicione um cartão Visa ou Mastercard e salve. Se a Meta solicitar os dados da empresa, preencha-os.

Outra opção: acesse WhatsApp Manager → Settings → WhatsApp accounts → selecione a conta → Payment settings → Add payment method.

Se já houver um cartão cadastrado na empresa, mas ele não estiver vinculado ao WhatsApp, acesse WhatsApp accounts → selecione a conta → Settings → Payment settings → selecione o cartão → Make primary.

É necessário ter permissão para gerenciar pagamentos. O proprietário da conta tem essa permissão.

**O que fazer na 1MSG**

Abra o canal em [platform.1msg.io](https://platform.1msg.io/). O banner desaparecerá assim que a Meta aceitar o cartão — geralmente em poucos minutos.

Se o banner continuar aparecendo após uma hora, entre em contato com o [suporte](../../platform/support.pt.md) e envie capturas de tela do banner e da tela de pagamento na Meta.
