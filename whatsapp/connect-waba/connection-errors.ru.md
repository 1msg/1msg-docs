---
title: Ошибки при подключении WABA
description: Что делать, если после подключения WABA номер не привязан к аккаунту WhatsApp или не проходит оплата.
---

## The number is not linked to the WhatsApp account

Канал WhatsApp заблокирован со стороны Meta.

Необходимо выполнить два шага в указанном порядке.

**1. Повторно подтвердить номер в WhatsApp Manager**

Номер в данный момент не подтверждён, поэтому этот шаг обязателен.

1. Откройте [WhatsApp Manager](https://business.facebook.com/wa/manage/home/) под пользователем Facebook, который управляет соответствующим WhatsApp Business-аккаунтом.
2. Откройте раздел с номерами телефонов и выберите нужный номер.
3. Запросите новый код подтверждения по SMS или голосовому вызову и введите его. Необходимо, чтобы у вас была возможность получить SMS или звонок на этот номер.
4. Дождитесь, пока номер отобразится как подтверждённый. Если отображаемое имя уже одобрено, изменять его не требуется.

**2. Установить PIN-код WhatsApp в 1MSG**

1. Откройте [platform.1msg.io](https://platform.1msg.io/) и войдите в аккаунт.
2. Откройте нужный канал.
3. В верхней части экрана увидите баннер **Complete WhatsApp setup: PIN not set** и нажмите **Set PIN**.

   ![Баннер Complete WhatsApp setup: PIN not set с кнопкой Set PIN](./assets/pin-not-set-banner.png)
4. Введите 6-значный PIN-код. Если PIN уже был создан в WhatsApp Manager, укажите тот же PIN. Если PIN ещё не создавался, введённые цифры станут вашим PIN-кодом. Сохраните его. 1MSG не хранит PIN-код и не может показать его позже.
5. Подтвердите, что PIN сохранён, и нажмите **Continue**.

После выполнения обоих шагов обновите страницу **Status** канала. Статус **External WABA channel** больше не должен отображаться как **blocked**.

Если что-то непонятно или возникли проблемы, [обратитесь в поддержку](../../platform/support.ru.md) и приложите скриншоты — мы поможем разобраться.

## There is an error with the payment method. This will block business initiated conversations.

`There is an error with the payment method` значит, что Meta не может списать оплату сообщений WhatsApp. Шаблоны и первое сообщение клиенту не уходят. Ответы в уже открытом диалоге могут уходить.

Карта должна стоять в Meta. Подписка 1MSG эту оплату не покрывает.

**Куда зайти**

Войдите в Facebook пользователем, который управляет этим WhatsApp-аккаунтом.

1. Откройте [Meta Business Suite](https://business.facebook.com/) → Settings.
2. Слева вверху выберите бизнес, которому принадлежит этот WhatsApp-аккаунт.
3. Billing & payments → Accounts → аккаунт этого канала → Add payment method.
4. Добавьте Visa или Mastercard и сохраните. Если Meta спросит данные компании — заполните их.

Иной путь: WhatsApp Manager → Settings → WhatsApp accounts → Выберите аккаунт → Payment settings → Add payment method.

Карта уже есть в бизнесе, но не привязана к WhatsApp: WhatsApp accounts → аккаунт → Settings → Payment settings → выберите карту → Make primary.

Нужны права на оплату. У владельца аккаунта они есть.

**Что сделать в 1MSG**

Откройте канал на [platform.1msg.io](https://platform.1msg.io/). Баннер пропадает, когда Meta примет карту — обычно за несколько минут.

Если через час баннер на месте, напишите в поддержку и приложите скрин баннера и экрана оплаты в Meta.
