# Реєстрація застосунку в Oura

Для перевірки застосунку використовуйте повні англомовні версії сторінок.
На кожній сторінці є перемикач УКР / EN, який відкриває той самий документ іншою мовою.

| Поле | Значення |
| --- | --- |
| Display Name | Personal Wellness Journal |
| Description | Personal, non-commercial application to access and analyze my own sleep, activity, and recovery data and generate reports in Ukrainian. Currently in development. |
| Contact Email | Власна дійсна контактна адреса власника; у цей публічний файл її не додаємо. |
| Website | https://fedak.github.io/personal-wellness-journal/en/ |
| Privacy Policy | https://fedak.github.io/personal-wellness-journal/en/privacy.html |
| Terms of Service | https://fedak.github.io/personal-wellness-journal/en/terms.html |

## Redirect URI — окреме налаштування

Попередньо запропонована адреса локального клієнта:

```text
http://localhost:8000/auth/oura/callback
```

Цей клієнт ще не реалізований. Прийнятність HTTP localhost потрібно перевірити
у формі нового порталу; якщо адреса відхиляється, потрібен контрольований
HTTPS callback. Зареєстрована адреса має точно збігатися з адресою в OAuth-запиті.
Не використовуйте інформаційні сторінки GitHub Pages як callback.

## Дозволи

Виберіть категорії даних, які використовуватимуться в першій версії.
Для запланованих звітів: Daily, Heartrate, SpO2, Stress, Heart Health, Workout,
Tag. Personal і Session додаються за потреби. Email і Ring Configuration
поки не потрібні. Сам список дозволів у порталі не замінює авторизацію власника.

Після створення застосунку зберігайте Client Secret локально, поза публічним
репозиторієм. Для доступу до даних потрібен наступний крок OAuth2-авторизації.
