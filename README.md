# TelebotPaymentsExample

## Что это вообще?

Это набросок платежной системы для ботов-магазинов.
Здесь реализована оплата через QIWI API

## Быстрый старт

1) Открываем `sample-telegram-bot.py`
2) Вписываем все нужные данные:
```python
# Токен бота телеграмм можно взять у @BotFather
telegram_token = '********03:AAFtxJz1p0KHy**********************'

# Номер телефона
my_login = '7912*******' 

# https://qiwi.com/api
qiwi_token = '7c91ebd4************************'

qiwi_nick = 'sextest'
```
3) Запускаем `sample-telegram-bot.py`
4) Прописываем боту `/test` и получаем сообщение:

![image](https://user-images.githubusercontent.com/92515117/148224737-43fef9b8-924e-4781-8d69-b9690b6abb30.png)

В случае оплаты или истечении срока платежа бот оповестит вас

## Разная информация
### Есть база данных?

Нет, базы данных нет. Есть только временное хранение заказов в файле на случай непредвиденной остановки бота. По завершении заказа запись о нем удаляется

### Является ли комментарий обязательным?

Да, писать комментарий при оплате обязательно, так как по нему _(и стоимости)_ происходит проверка платежей

## Зависимости

- telebot - `pip install pyTelegramBotAPI`
- requests - `pip install requests`
- hashlib - `pip install hashlib`
