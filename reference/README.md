# API reference

OpenAPI 3.0 specs of the 1MSG APIs. The site renders them as the API reference:

| File | API | Page on the site |
| --- | --- | --- |
| `inbox.json` | Inbox API | [1msg.io/docs/reference/inbox](https://1msg.io/docs/reference/inbox) |
| `whatsapp.json` | WhatsApp Business API, English | [1msg.io/docs/reference/whatsapp](https://1msg.io/docs/reference/whatsapp) |
| `whatsapp.ru.json` | WhatsApp Business API, Russian | [1msg.io/ru/docs/reference/whatsapp](https://1msg.io/ru/docs/reference/whatsapp) |

The site reads the specs from `main` and picks up a merged change within about an hour. Where a spec has no translation, the site shows the English one.

## Do not rename or move the files

The site fetches each spec by its raw URL, such as `https://raw.githubusercontent.com/1msg/1msg-docs/main/reference/inbox.json` (see `src/lib/docs/openapi.ts` in `1msg/1msg-website`). A renamed or moved file drops its reference from the site, so change the URL on the site first.

## Where the specs come from

- `whatsapp.json` and `whatsapp.ru.json` mirror `swagger.waba.json` and `swagger.waba.ru.json` in the private `1msg/1msg-front` repo, which Alibek Seksenali (@alibek-seksenali) maintains. That copy builds docs.1msg.io, which my.1msg.io also shows as its API docs. Make every change in both repos, and keep the English and Russian specs in step.
- `inbox.json` is exported from the Inbox API, which generates the spec from its own code (private `1msg/1msg-developers`). Fix a description there and export the spec again: a hand edit here is lost on the next export.

This folder holds no articles: the site does not turn the `.md` files under `reference/` into pages, so this README stays on GitHub.
