# API reference

OpenAPI 3.0 specs of the 1MSG APIs. The site renders them as the API reference:

| File | API | Page on the site |
| --- | --- | --- |
| `whatsapp.json` | WhatsApp Business API, English | [1msg.io/docs/reference/whatsapp](https://1msg.io/docs/reference/whatsapp) |
| `whatsapp.ru.json` | WhatsApp Business API, Russian | [1msg.io/ru/docs/reference/whatsapp](https://1msg.io/ru/docs/reference/whatsapp) |
| `campaigns.json` | Campaigns API | [1msg.io/docs/reference/campaigns](https://1msg.io/docs/reference/campaigns) |
| `inbox.json` | Inbox API | [1msg.io/docs/reference/inbox](https://1msg.io/docs/reference/inbox) |

The site picks up a change merged into `main` within about five minutes, the same way as the articles. A new spec needs no change on the site either.

## How the site reads the specs

- **One file, one API.** `reference/<id>.json` becomes the reference at `/docs/reference/<id>`, so the file name is part of the URL. Renaming a file moves its pages to new URLs.
- **Translations.** `reference/<id>.<lang>.json` is that API in another language: `ru` or `pt`, the languages the docs have. The site pairs its methods with the English ones by method and path, so the URLs stay the same. A method the translation lacks is shown in English. A translation without its English file is ignored.
- **Name.** The section takes its name from `info.title`. The one exception is `whatsapp`, which the site always calls "WhatsApp Business API".
- **Method pages.** Each operation gets its own page. The page is named after the `operationId` when it is the public method name (`sendMessage` → `send-message`). Generated ids with an underscore (`InboxController_listChannels`) give way to the `summary` (`List channels visible to this key` → `list-channels-visible-to-this-key`). So a changed `summary` or `operationId` changes that method's URL.
- **Sidebar.** With two tags or more, methods are grouped under their tags in the spec's order. Otherwise they are listed in the spec's order. WhatsApp comes first under Reference, the other APIs follow by file name.
- **Errors.** A spec the site cannot load or read hides only its own section; the rest of the docs stay up.

Anything else in `reference/` (this README, subfolders) is not shown on the site.

## Where the specs come from

- `whatsapp.json` and `whatsapp.ru.json` mirror `swagger.waba.json` and `swagger.waba.ru.json` in the private `1msg/1msg-front` repo, which Alibek Seksenali (@alibek-seksenali) maintains. That copy builds docs.1msg.io, which my.1msg.io also shows as its API docs. Make every change in both repos, and keep the English and Russian specs in step.
- `inbox.json` and `campaigns.json` are exported from the API, which generates them from its own code (private `1msg/1msg-developers`): `https://api.stage.1msg.io/api/docs/inbox-json` and `https://api.stage.1msg.io/api/docs/campaigns-json`. Fix a description there and export the spec again: a hand edit here is lost on the next export.
