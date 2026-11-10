---
title: Channel ID + JWT
description: Onde encontrar o ID e o token JWT do canal, como enviá-los numa requisição à API e o que significam os erros de autorização.
---

Toda requisição à API leva duas coisas: o **Channel ID**, que diz de qual número você envia, e o **token JWT**, que prova que a requisição é sua. Os dois ficam na página do canal.

A seguir: onde encontrá-los, como colocá-los na requisição, como testar e o que fazer em caso de erro.

## Passo 1. Abra a página do canal

Entre em [**platform.1msg.io**](https://platform.1msg.io/) e abra o canal pelo qual você vai enviar. Se houver vários números conectados, cada um é um canal separado, com seu próprio token.

Se você ainda não tem conta, comece pelo [Início rápido](../platform/quickstart.pt.md): dá para ativar um canal de teste e enviar a primeira mensagem sem esperar a aprovação da Meta.

## Passo 2. Copie o Channel ID e o token

Na página do canal você encontra:

* **Channel ID** — um identificador curto, que entra na URL da requisição;
* **JWT Token** — uma string que deve ser enviada em toda requisição.

O token é uma senha. Quem tiver o token pode enviar mensagens em nome da sua empresa. Guarde-o em variáveis de ambiente no servidor. Não coloque o token no frontend, em repositório público nem em capturas de tela.

## Passo 3. Coloque-os na requisição

As requisições vão para [**api.1msg.io**](https://api.1msg.io/). O Channel ID entra na URL logo depois do host:

```
https://api.1msg.io/{channelId}/sendMessage
```

Você pode enviar o token de duas formas. Elas são equivalentes: a API procura o token primeiro no corpo da requisição, depois na query string e depois no cabeçalho.

**No cabeçalho — recomendado:**

```bash
curl -X POST "https://api.1msg.io/{channelId}/sendMessage" \
  -H "Authorization: Bearer {token}" \
  -H "Content-Type: application/json" \
  -d '{"phone": "79001234567", "body": "Hello 1msg"}'
```

Um token no cabeçalho não vai parar nos logs de acesso do servidor nem no histórico do navegador, por isso é o preferido em produção.

**Na query string:**

```bash
curl -X POST "https://api.1msg.io/{channelId}/sendMessage?token={token}" \
  -H "Content-Type: application/json" \
  -d '{"phone": "79001234567", "body": "Hello 1msg"}'
```

Prático para um teste rápido, mas o token vai aparecer nos logs de acesso e nos proxies. Não use em produção.

## Passo 4. Verifique se funciona

Abra o [Playground](https://platform.1msg.io/dashboard/playground) no painel. Ele preenche o Channel ID e o token para você e mostra o JSON da requisição pronto, a resposta da API e o que chega no webhook. Se a mensagem foi entregue, o Channel ID e o token estão certos, e você pode levar o mesmo JSON para o seu código.

## Se a requisição falhar

**`token is required`, código 401.** O token não chegou à API. Confira se ele está em pelo menos um lugar: no corpo ou no cabeçalho.

**`access denied`, código 403.** O erro mais comum. Significa uma de duas coisas: o token está errado (erro de digitação, cortado ao copiar) ou pertence a um canal diferente do que está na URL. Copie de novo o ID e o token da mesma página do canal.

**`Invalid API KEY`, código 401.** O token chegou ao WhatsApp, mas foi recusado lá. Normalmente o canal não está mais conectado. Confira o status dele no painel.

**`Instance not found`, código 404.** O Channel ID na URL está errado. Confira se ele foi copiado inteiro e sem espaços.

## Um canal, um token

Cada canal tem seu próprio token. Se a empresa tem vários números de WhatsApp, ela também tem vários canais e vários tokens. O token de um canal não serve para enviar por outro.

## Próximos passos

* [Início rápido](../platform/quickstart.pt.md) — da primeira mensagem à produção
* [Conexão da WABA](./connect-waba/README.pt.md) — conecte seu próprio número
* [Referência da API](https://docs.1msg.io/) — todos os métodos
