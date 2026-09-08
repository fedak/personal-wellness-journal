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

Адреса реалізованого локального клієнта:

```text
http://localhost:8765/auth/oura/callback
```

Цю адресу перевірено з локальним клієнтом. Зареєстрована адреса має точно
збігатися з адресою в OAuth-запиті, включно з портом і шляхом.
Не використовуйте інформаційні сторінки GitHub Pages як callback.

## Дозволи

Для архіву всіх 19 підтримуваних типів даних клієнт використовує Daily,
Heartrate, SpO2, Stress, Heart Health, Workout, Tag, Personal, Session і
Ring Configuration. Останній дозвіл потрібен також для історії заряду кільця.
Email не потрібен. Сам список дозволів у порталі не замінює авторизацію власника:
після розширення списку потрібно повторно підтвердити доступ через локальну форму.

Після створення застосунку зберігайте Client Secret локально, поза публічним
репозиторієм. Для доступу до даних потрібен наступний крок OAuth2-авторизації.
