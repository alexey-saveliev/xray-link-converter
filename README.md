# Xray Outbound → Share Link Converter

Простая web-страница для конвертации **Xray/V2Ray outbound JSON** в share-ссылки:

- `vless://`
- `vmess://`
- `trojan://`
- `ss://` (Shadowsocks)

Работает **полностью в браузере (client-side)** — без отправки данных на сервер.

---

## 🚀 Демо

[https://alexey-saveliev.github.io/xray-link-converter/](https://alexey-saveliev.github.io/xray-link-converter/)

## ⚙️ Возможности

- Поддержка популярных протоколов:
  - VLESS (включая Reality)
  - VMess
  - Trojan
  - Shadowsocks
- Обработка transport:
  - TCP
  - WebSocket (WS)
  - gRPC
  - HTTPUpgrade / XHTTP
- Поддержка:
  - TLS
  - Reality (pbk, sid, fp и т.д.)
- Работа с:
  - одним outbound
  - массивом `outbounds`
- Генерация ссылки + копирование в буфер
- Примеры конфигураций прямо в UI

---

## 📦 Использование

1. Открой страницу
2. Вставь JSON конфигурации Xray (outbound или весь config)
3. Нажми **"Сконвертировать"**
4. Получи share-ссылку

---

## 📄 Пример входного JSON

### VLESS

```json
{
  "protocol": "vless",
  "settings": {
    "vnext": [
      {
        "address": "example.com",
        "port": 443,
        "users": [
          {
            "id": "UUID",
            "encryption": "none"
          }
        ]
      }
    ]
  }
}
````

## 🔒 Безопасность

* Все данные обрабатываются **локально в браузере**
* Нет отправки JSON на сервер
* Подходит для работы с чувствительными конфигурациями


## ⚠️ Ограничения

* Поддерживаются только основные outbound-протоколы
* Некоторые специфичные параметры Xray могут не учитываться
* Нет обратного преобразования (link → JSON)


## 🛠️ Планы развития

* [ ] Обратное преобразование (link → JSON)
* [ ] Импорт JSON-файла
* [ ] Drag & Drop
* [ ] Поддержка inbound → link
* [ ] Массовая конвертация
* [ ] Генерация QR-кодов

## 📄 Лицензия

MIT