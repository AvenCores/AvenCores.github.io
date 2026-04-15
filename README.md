<div align="center">
    <a href="https://www.youtube.com/@avencores/" target="_blank">
      <img src="https://github.com/user-attachments/assets/338bcd74-e3c3-4700-87ab-7985058bd17e" alt="YouTube" height="40">
    </a>
    <a href="https://t.me/avencoresyt" target="_blank">
      <img src="https://github.com/user-attachments/assets/939f8beb-a49a-48cf-89b9-d610ee5c4b26" alt="Telegram" height="40">
    </a>
    <a href="https://vk.ru/avencoresreuploads" target="_blank">
      <img src="https://github.com/user-attachments/assets/dc109dda-9045-4a06-95a5-3399f0e21dc4" alt="VK" height="40">
    </a>
    <a href="https://dzen.ru/avencores" target="_blank">
      <img src="https://github.com/user-attachments/assets/bd55f5cf-963c-4eb8-9029-7b80c8c11411" alt="Dzen" height="40">
    </a>
</div>

# 🌐 AvenCores.github.io

[![GPL-3.0 License](https://img.shields.io/badge/License-GPL--3.0-blue?style=for-the-badge)](./LICENSE)
[![Website](https://img.shields.io/badge/Website-Goida%20VPN-207e5c?style=for-the-badge&logo=firefox)](https://avencores.github.io/goida-vpn-site/)
[![GitHub stars](https://img.shields.io/github/stars/AvenCores/AvenCores.github.io?style=for-the-badge)](https://github.com/AvenCores/goida-vpn-site/stargazers)
![GitHub forks](https://img.shields.io/github/forks/AvenCores/AvenCores.github.io?style=for-the-badge)
[![GitHub pull requests](https://img.shields.io/github/issues-pr/AvenCores/AvenCores.github.io?style=for-the-badge)](https://github.com/AvenCores/goida-vpn-site/pulls)
[![GitHub issues](https://img.shields.io/github/issues/AvenCores/AvenCores.github.io?style=for-the-badge)](https://github.com/AvenCores/goida-vpn-site/issues)

<img alt="chrome_XBv3J3lpo1" src="https://github.com/user-attachments/assets/946b9a0f-ed88-4463-8e44-cbe4d4f3fa58" />

Статический GitHub Pages-репозиторий с одностраничной страницей-перенаправлением для `Goida VPN Configs`.

Сейчас сайт открывает стильный экран ожидания, показывает 3-секундный таймер и автоматически переводит пользователя на основной адрес:

`https://avencores.github.io/goida-vpn-site/`

## 📁 Что находится в проекте

- `index.html` — вся логика сайта в одном файле: HTML-разметка, CSS-оформление, анимации, таймер, прогресс-бар и JavaScript-редирект.
- `robots.txt` — правила для поисковых роботов, включая отдельные директивы для Yandex.
- `favicon.png` — иконка сайта.
- `LICENSE` — лицензия GNU GPL v3.

## ⚙️ Как работает страница

- В `<meta http-equiv="refresh">` настроен автоматический переход через 3 секунды.
- В JavaScript дублируется редирект через `window.location.replace(...)`.
- На странице есть ручная кнопка `Перейти сейчас`.
- Если у пользователя отключён JavaScript, переход всё равно выполняется через meta refresh.
- Поддерживается переключение светлой и тёмной темы на основе `localStorage` и системных предпочтений.
- Добавлены защитные meta-заголовки: CSP, `X-Content-Type-Options` и `Referrer-Policy`.

## 🚀 Как запустить локально

Так как это полностью статический сайт без сборки, достаточно открыть `index.html` в браузере.

Если нужен локальный сервер, можно использовать, например:

```powershell
python -m http.server 8000
```

После этого откройте `http://localhost:8000`.

## 🛠️ Что менять при обновлении

Если нужно перенаправлять на другой адрес, обновите в `index.html` все связанные места:

- `canonical`
- `preload`
- `meta refresh`
- текст с адресом на странице
- значение `REDIRECT_URL` в нижнем скрипте

Если нужно изменить задержку редиректа, скорректируйте:

- `content="3; url=..."`
- `TOTAL_SECONDS = 3`
- стартовое значение счётчика в элементе `#count`

## 🔎 Замечания по SEO и индексации

- Страница помечена как `noindex, nofollow`, то есть не предназначена для индексации.
- `robots.txt` ссылается на `sitemap.xml` и `Host` для пути `goida-vpn-site`, поэтому при смене структуры сайта эти настройки стоит проверить отдельно.

## 📜 Лицензия
Данный проект распространяется под лицензией GPL-3.0 — подробности см. в файле [LICENSE](LICENSE).

---
# 💰 Поддержать автора
+ **SBER**: `2202 2050 1464 4675`
