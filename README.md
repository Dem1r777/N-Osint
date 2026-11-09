<div align="center">

```text
  _   _         ____   _____ _____ _   _ _______ 
 | \ | |       / __ \ / ____|_   _| \ | |__   __|
 |  \| |______| |  | | (___   | | |  \| |  | |   
 | . ` |______| |  | |\___ \  | | | . ` |  | |   
 | |\  |      | |__| |____) |_| |_| |\  |  | |   
 |_| \_|       \____/|_____/|_____|_| \_|  |_|   
                  Created by Dem1
```

# 🔍 N-OSINT — Global Username Reconnaissance & OSINT Scanner

[![Python](https://img.shields.io/badge/Python-3.9%2B-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Platforms](https://img.shields.io/badge/Platforms-195%2B-00F0FF?style=for-the-badge)](./n_osint/sites.py)
[![Categories](https://img.shields.io/badge/Categories-13-10B981?style=for-the-badge)](./n_osint/sites.py)
[![Languages](https://img.shields.io/badge/UI_Languages-EN_%7C_RU_%7C_TG-F59E0B?style=for-the-badge)](./n_osint/i18n.py)
[![Author](https://img.shields.io/badge/Created_by-Dem1-8B5CF6?style=for-the-badge)](#)

**High-speed terminal OSINT reconnaissance tool for hunting usernames across 195+ global social networks, messengers, gaming, developer, and regional platforms using strictly open sources (Public OSINT).**

[🇬🇧 **English Documentation**](#-english-documentation) • [🇷🇺 **Документация на русском**](#-документация-на-русском)

</div>

---

# 🇬🇧 English Documentation

## 📖 Overview

**N-OSINT** (created by **Dem1**) is a modern, asynchronous command-line & interactive Terminal UI (TUI) tool inspired by *Sherlock* and *Maigret*. It allows cybersecurity researchers, OSINT investigators, penetration testers, and enthusiasts to quickly discover a target's digital footprint across the internet by searching a single username (or automatic username variations) across **195+ websites worldwide**.

Unlike basic status-code checkers, **N-OSINT** uses multi-layered detection rules (HTTP status codes, HTML body signature analysis, redirect inspection, public API/syndication probing, and per-site regex validation) along with anti-false-positive WAF/Cloudflare filtering and automatic metadata extraction.

---

## ✨ Key Features

- 🌐 **195+ Global Platforms in 13 Categories**:
  Covers all major global ecosystems — **X (Twitter), Instagram, TikTok, Threads, Telegram, LinkedIn, Steam**, YouTube, GitHub, Reddit, Twitch, Discord, Roblox, Chess.com, VK, Habr, Bilibili/Gitee/Zhihu, Patreon, OpenSea, and many more.
- ⚡ **Blazing-Fast Asynchronous Engine**:
  Powered by `httpx` and `aiohttp` with configurable concurrency (up to 150 simultaneous requests). Includes a built-in fallback to Python's standard `urllib` + `ThreadPoolExecutor` so the script works out of the box even before installing third-party packages.
- 🖥️ **Interactive Terminal UI (Rich TUI)**:
  - Stylish cyber-themed ASCII banner (`Created by Dem1`).
  - Interactive numbered navigation menu with instant **`0 = Back`** support at every prompt and submenu.
  - Real-time progress bar with live hit notifications, response ping (`ms`), and extracted page titles/bios.
- 🌍 **Multi-Language Interface (3 Languages)**:
  - **English (`en`)** — Default startup language.
  - **Russian (`ru`)** — Full localization.
  - **Tajik (`tg` / Тоҷикӣ)** — Full localization.
  - Switch languages anytime from the main menu (`[7]`) or via CLI flag (`-l en|ru|tg`).
- 🔄 **Smart Username Variations Generator**:
  Automatically generates and scans common nickname permutations (`nick_`, `_nick`, `nick.official`, `real_nick`, `the_nick`, `nick1`, and `.` / `_` / `-` swaps).
- 🛡️ **Anti-False-Positive & WAF Detection**:
  Detects Cloudflare challenges, captchas, soft-404 pages, and login redirects so blocked requests are marked as `WAF` instead of false-positive hits.
- 📊 **Multi-Format Report Export**:
  Export your findings with one click into **`reports/`** as:
  - **HTML** — Standalone dark-mode interactive dashboard with clickable profile cards.
  - **JSON** — Full structured data for automation and pipelines.
  - **CSV** — Spreadsheet-ready table (UTF-8 BOM compatible with Excel).
  - **TXT** — Clean text summary for notes and reports.

---

## 🗂️ Supported Categories & Platforms (195+ Sites)

| # | Code | Category | Examples of Supported Platforms |
|:-:|:-----|:---------|:--------------------------------|
| 1 | `social` | **Social Networks** | X (Twitter), Instagram, TikTok, Threads, Facebook, Pinterest, Snapchat, Bluesky, Mastodon, Reddit, Tumblr, Truth Social, Gab, Minds, MeWe, Gettr, Clubhouse, Linktree, Carrd, About.me, Bento.me, Taplink, Beacons.ai, Solo.to, Bio.link, Gravatar, Ask.fm, Tellonym, NGL.link, SpaceHey |
| 2 | `messengers` | **Messengers** | Telegram, Discord (Invite/Vanity), Keybase, Matrix, ICQ / VK Teams, Kik |
| 3 | `video` | **Video & Streams** | YouTube, Twitch, Kick, Rumble, Vimeo, Dailymotion, Trovo, Coub, Likee, Bigo Live |
| 4 | `gaming` | **Gaming** | Steam (Custom ID & Groups), Roblox, Chess.com, Lichess, FACEIT, osu!, Minecraft (NameMC / Mojang), PSNProfiles (PlayStation), XboxGamertag, Speedrun.com, Itch.io, GameJolt, Newgrounds, Modrinth, CurseForge, NexusMods, Backloggd, GOG, TETR.IO |
| 5 | `dev` | **IT & Coding** | GitHub, GitLab, Bitbucket, Codeberg, Gitea, SourceForge, HuggingFace, Kaggle, LeetCode, Codeforces, Codewars, HackerRank, AtCoder, TopCoder, Dev.to, Hashnode, Replit, CodePen, JSFiddle, StackBlitz, Docker Hub, PyPI, npm, Crates.io, RubyGems, Packagist, NuGet, Launchpad, AUR, HackerNews, HackerOne, Bugcrowd, TryHackMe, Root-Me, WakaTime, Pastebin |
| 6 | `professional` | **Career & Business** | LinkedIn, ProductHunt, IndieHackers, Crunchbase, Wellfound (AngelList), Polywork, Read.cv, Peerlist, SlideShare, SpeakerDeck, ResearchGate, Academia.edu |
| 7 | `creative` | **Art & Design** | Behance, Dribbble, ArtStation, DeviantArt, Figma, Unsplash, Flickr, 500px, VSCO, EyeEm, Imgur, Giphy, Tenor, Sketchfab, Thingiverse, Printables, Cara.app, Pixiv |
| 8 | `music` | **Music & Audio** | SoundCloud, Spotify, Bandcamp, Last.fm, Genius, Mixcloud, Audiomack, ReverbNation, Discogs, RateYourMusic, Freesound, Musescore |
| 9 | `blogs` | **Blogs & Forums** | Medium, Substack, Quora, WordPress, Blogger, LiveJournal, Disqus, Wikipedia (EN / RU), Fandom, Slashdot, DailyKos, Wattpad, Archive of Our Own (AO3), Scribd, Issuu, 9GAG, iFunny |
| 10 | `cis` | **CIS Services** | VK (ВКонтакте), OK.ru, Habr, Habr Career, Pikabu, DTF, VC.ru, Boosty, Rutube, Dzen, TenChat, Drive2.ru, Shikimori, Ficbook, Author.Today, Kwork, FL.ru, Freelance.habr, Trashbox, CyberForum, Lolzteam, Sports.ru, StopGame, Playground.ru, IRecommend |
| 11 | `asia` | **Asian Platforms** | Gitee, Zhihu, CSDN, Velog, Note.com, Qiita, Zenn.dev, Hatena Blog, Weibo |
| 12 | `finance` | **Freelance & Crypto** | Patreon, BuyMeACoffee, Ko-fi, Gumroad, Fiverr, Freelancer.com, PeoplePerHour, Etsy, eBay, Poshmark, Depop, Redbubble, TeePublic, TradingView, CoinMarketCap, OpenSea, Rarible, Foundation.app, Liberapay, OpenCollective |
| 13 | `hobbies` | **Hobbies & Lifestyle** | Letterboxd, MyAnimeList, AniList, Kitsu, Goodreads, LibraryThing, Trakt.tv, Duolingo, Memrise, OpenStreetMap, Strava, Untappd, Geocaching, Instructables, Hackaday.io |

---

## 🚀 Installation & Quick Start

### Prerequisites
- **Python 3.9+** installed on your system (Windows, Linux, macOS, or Termux).

### 1. Clone the Repository
```bash
git clone https://github.com/Dem1/N-OSINT.git
cd N-OSINT
```

### 2. Install Dependencies
```bash
pip install -r requirements.txt
```
> 💡 **Windows Users:** You can simply double-click or run `start.bat`. It will automatically check your Python installation, install `httpx`, `rich`, and `aiohttp` if missing, and launch the interactive menu.

---

## 🖥️ Usage Guide

### 1. Interactive Terminal Menu (TUI Mode)
Run the script without arguments to open the interactive control panel (starts in **English** by default):
```bash
python n_osint.py
```

#### Main Menu Options:
```text
[1] Search all platforms
[2] Search by categories
[3] Search with username variations
[4] Search specific sites (X, Instagram, Steam...)
[5] Platform catalog (195+ sites)
[6] Settings (Threads: 45, Timeout: 10.0s, Proxy: None)
[7] Language / Язык / Забон (English)
[0] Exit
```
> 🔙 **Quick Back Navigation:** Inside any menu option, category selector, or input prompt, simply type **`0`** and press `Enter` to go one step back without restarting the script!

---

### 2. Command-Line Interface (CLI Mode)

You can also run **N-OSINT** directly from the terminal with CLI arguments (just like *Sherlock*):

```bash
# Search a username across all 195+ platforms worldwide:
python n_osint.py durov

# Search multiple usernames in a single run:
python n_osint.py durov torvalds

# Filter scan by specific categories (e.g. social networks, messengers, gaming):
python n_osint.py username -c social messengers gaming

# Filter scan by specific platform names:
python n_osint.py username -s X Instagram TikTok Threads Telegram LinkedIn Steam

# Enable automatic username variations and export all reports to reports/:
python n_osint.py username --variations -o reports/

# Customize concurrency (threads), timeout, and proxy:
python n_osint.py username -n 80 -t 8 --proxy http://127.0.0.1:8080

# Launch in Russian or Tajik directly from CLI:
python n_osint.py -l ru
python n_osint.py -l tg

# List all supported categories or platforms:
python n_osint.py --list-categories
python n_osint.py --list-sites
```

### Full CLI Flags Reference

| Flag | Long Flag | Description |
|:-----|:----------|:------------|
| `usernames` | — | One or more target usernames (omit to launch interactive TUI) |
| `-i` | `--interactive` | Force interactive TUI menu mode |
| `-l` | `--lang {en,ru,tg}` | Interface language: `en` (default), `ru` (Russian), `tg` (Tajik) |
| `-c` | `--category CAT ...` | Filter platforms by one or more category codes |
| `-s` | `--site SITE ...` | Filter platforms by site name substrings |
| `-v` | `--variations` | Automatically generate and test username variations |
| `-t` | `--timeout SEC` | HTTP timeout in seconds (default: `10.0`) |
| `-n` | `--concurrency NUM` | Number of concurrent async connections (default: `45`, max: `150`) |
| `-o` | `--output DIR` | Directory to save `.txt`, `.json`, `.csv`, and `.html` reports |
| — | `--proxy URL` | HTTP/SOCKS5 proxy URL (e.g. `http://127.0.0.1:8080`) |
| — | `--verbose` | Print `NOT_FOUND`, `WAF`, and connection errors in real time |
| — | `--no-SSL-check` | Disable SSL certificate verification |
| — | `--list-categories` | Print table of all platform categories and exit |
| — | `--list-sites` | Print catalog of all supported sites and exit |
| — | `--version` | Show version and platform count |

---

## 📂 Project Structure

```text
N-OSINT/
├── n_osint/
│   ├── __init__.py      # Package metadata & author (Dem1)
│   ├── sites.py         # Database of 195+ platforms, categories & variation generator
│   ├── scanner.py       # Async HTTP engine (httpx / aiohttp / urllib fallback) & metadata parser
│   ├── ui.py            # Rich TUI, ASCII banner, interactive menus & live progress bar
│   ├── i18n.py          # Multi-language localization dictionary (English, Russian, Tajik)
│   ├── exporter.py      # Report generators for TXT, JSON, CSV, and dark-mode HTML
│   └── cli.py           # CLI argument parser & runner
├── n_osint.py           # Main executable entry point
├── start.bat            # One-click Windows launcher & dependency installer
├── requirements.txt     # Python dependencies (httpx, rich, aiohttp)
└── README.md            # Bilingual project documentation (EN / RU)
```

---

## ⚠️ Legal & Ethical Disclaimer

**N-OSINT** is developed strictly for **educational purposes, authorized security assessments, and legitimate Open-Source Intelligence (OSINT) research**.
- The tool queries **exclusively publicly accessible web pages** and public endpoints.
- It does **not** bypass authentication, crack passwords, or access private data.
- The author (**Dem1**) is not responsible for any misuse or damage caused by this software. Always comply with local laws and platform Terms of Service.

---
---

# 🇷🇺 Документация на русском

## 📖 О проекте

**N-OSINT** (создатель — **Dem1**) — это высокоскоростной асинхронный терминальный OSINT-инструмент нового поколения (аналог *Sherlock* и *Maigret*) для поиска аккаунтов человека по никнейму исключительно по открытым источникам (**Public OSINT**).

Скрипт проверяет целевой никнейм сразу по **195+ соцсетям, мессенджерам, игровым сервисам, IT-платформам, форумам и локальным сайтам мира**, используя комбинированные методы проверки: HTTP-коды ответа, сигнатуры в HTML-коде страницы, отслеживание редиректов, публичные API-эндпоинты и проверку допустимого формата имени пользователя (`regex`).

---

## ✨ Основные возможности

- 🌍 **Глобальная база из 195+ сайтов в 13 категориях**:
  Поддерживаются **X (Twitter), Instagram, TikTok, Threads, Telegram, LinkedIn, Steam**, YouTube, GitHub, GitLab, Reddit, Twitch, Discord, Roblox, Chess.com, Lichess, VK (ВКонтакте), OK.ru, Хабр, Пикабу, DTF, VC.ru, Boosty, Kwork, Lolzteam, Patreon, OpenSea и десятки других площадок.
- ⚡ **Высокая скорость работы**:
  Асинхронный движок на базе `httpx` и `aiohttp` проверяет все платформы за считанные секунды (до 150 параллельных потоков). Если сторонние библиотеки ещё не установлены, автоматически включается резервный многопоточный режим на стандартной библиотеке `urllib`.
- 🖥️ **Красивый интерактивный интерфейс в терминале (Rich TUI)**:
  - Фирменный ASCII-баннер **N-OSINT** с подписью `Created by Dem1`.
  - Короткое и понятное меню с выбором режима поиска.
  - **Быстрый возврат назад (`0 = Назад`)**: в любом подменю и на любом шаге ввода достаточно нажать **`0`**, чтобы вернуться на предыдущий шаг без перезапуска программы.
  - Живой прогресс-бар с выводом найденных ссылок в реальном времени, временем отклика (`мс`) и автоматическим извлечением заголовка/информации профиля (`og:title` / JSON).
- 🗣️ **Поддержка 3 языков интерфейса**:
  - **English (`en`)** — язык по умолчанию при запуске.
  - **Русский (`ru`)** — полная русская локализация.
  - **Тоҷикӣ (`tg`)** — полная таджикская локализация.
  - Переключение языка доступно прямо в главном меню (пункт `[7]`) или через флаг запуска `-l ru` / `-l tg`.
- 🔄 **Авто-подбор вариаций никнейма**:
  Автоматическая генерация и проверка похожих никнеймов (`nick_`, `_nick`, `nick.official`, `real_nick`, `the_nick`, `nick1`, а также замена символов `.`, `_`, `-`).
- 🛡️ **Защита от ложных срабатываний (Anti-WAF)**:
  Распознаёт капчи, проверки Cloudflare и мягкие редиректы, помечая их как `WAF`, чтобы они не попадали в список найденных профилей.
- 📄 **Экспорт отчётов в 4 форматах**:
  Сохранение результатов в папку **`reports/`** в форматах:
  - **HTML** — стильный автономный веб-отчёт в тёмной теме с кликабельными карточками профилей.
  - **JSON** — структурированный отчёт со всей статистикой.
  - **CSV** — таблица для Excel / Google Таблиц.
  - **TXT** — чистый текстовый список найденных ссылок.

---

## 🗂️ Категории платформ (13 категорий / 195+ сайтов)

| № | Код | Категория | Примеры поддерживаемых сервисов |
|:-:|:----|:----------|:--------------------------------|
| 1 | `social` | **Соцсети** | X (Twitter), Instagram, TikTok, Threads, Facebook, Pinterest, Snapchat, Bluesky, Mastodon, Reddit, Tumblr, Truth Social, Minds, Linktree, Carrd, About.me, Bento.me, Taplink, Beacons.ai, Solo.to, Bio.link, Gravatar, Ask.fm, Tellonym, NGL.link, SpaceHey |
| 2 | `messengers` | **Мессенджеры** | Telegram, Discord, Keybase, Matrix, ICQ / VK Teams, Kik |
| 3 | `video` | **Видео и стримы** | YouTube, Twitch, Kick, Rumble, Vimeo, Dailymotion, Trovo, Coub, Likee, Bigo Live |
| 4 | `gaming` | **Игры** | Steam (ID и группы), Roblox, Chess.com, Lichess, FACEIT, osu!, Minecraft (NameMC), PSNProfiles (PlayStation), XboxGamertag, Speedrun.com, Itch.io, GameJolt, Newgrounds, Modrinth, CurseForge, NexusMods, Backloggd, GOG, TETR.IO |
| 5 | `dev` | **IT и кодинг** | GitHub, GitLab, Bitbucket, Codeberg, Gitea, SourceForge, HuggingFace, Kaggle, LeetCode, Codeforces, Codewars, HackerRank, AtCoder, TopCoder, Dev.to, Hashnode, Replit, CodePen, JSFiddle, StackBlitz, Docker Hub, PyPI, npm, Crates.io, RubyGems, Packagist, NuGet, Launchpad, AUR, HackerNews, HackerOne, Bugcrowd, TryHackMe, Root-Me, WakaTime, Pastebin |
| 6 | `professional` | **Карьера и бизнес** | LinkedIn, ProductHunt, IndieHackers, Crunchbase, Wellfound (AngelList), Polywork, Read.cv, Peerlist, SlideShare, SpeakerDeck, ResearchGate, Academia.edu |
| 7 | `creative` | **Арт и дизайн** | Behance, Dribbble, ArtStation, DeviantArt, Figma, Unsplash, Flickr, 500px, VSCO, EyeEm, Imgur, Giphy, Tenor, Sketchfab, Thingiverse, Printables, Cara.app, Pixiv |
| 8 | `music` | **Музыка** | SoundCloud, Spotify, Bandcamp, Last.fm, Genius, Mixcloud, Audiomack, ReverbNation, Discogs, RateYourMusic, Freesound, Musescore |
| 9 | `blogs` | **Блоги и форумы** | Medium, Substack, Quora, WordPress, Blogger, LiveJournal, Disqus, Wikipedia (EN / RU), Fandom, Slashdot, DailyKos, Wattpad, AO3, Scribd, Issuu, 9GAG, iFunny |
| 10 | `cis` | **Сервисы СНГ** | VK (ВКонтакте), OK.ru (Одноклассники), Хабр, Хабр Карьера, Пикабу, DTF, VC.ru, Boosty, Rutube, Дзен, TenChat, Drive2.ru, Shikimori, Ficbook, Author.Today, Kwork, FL.ru, Freelance.habr, Trashbox, CyberForum, Lolzteam, Sports.ru, StopGame, Playground.ru, IRecommend |
| 11 | `asia` | **Азия** | Gitee, Zhihu, CSDN, Velog, Note.com, Qiita, Zenn.dev, Hatena, Weibo |
| 12 | `finance` | **Фриланс и крипто** | Patreon, BuyMeACoffee, Ko-fi, Gumroad, Fiverr, Freelancer.com, PeoplePerHour, Etsy, eBay, Poshmark, Depop, Redbubble, TeePublic, TradingView, CoinMarketCap, OpenSea, Rarible, Foundation.app, Liberapay, OpenCollective |
| 13 | `hobbies` | **Хобби и развлечения** | Letterboxd, MyAnimeList, AniList, Kitsu, Goodreads, LibraryThing, Trakt.tv, Duolingo, Memrise, OpenStreetMap, Strava, Untappd, Geocaching, Instructables, Hackaday.io |

---

## 🚀 Установка и запуск

### Требования
- Установленный **Python 3.9+** (Windows, Linux, macOS или Termux на Android).

### 1. Клонирование репозитория
```bash
git clone https://github.com/Dem1/N-OSINT.git
cd N-OSINT
```

### 2. Установка зависимостей
```bash
pip install -r requirements.txt
```
> 💡 **Для пользователей Windows:** Вы можете просто запустить файл `start.bat` двойным кликом или из консоли — он сам проверит наличие библиотек `rich`, `httpx`, `aiohttp`, установит их при необходимости и запустит N-OSINT.

---

## 🖥️ Примеры использования

### 1. Интерактивный режим (TUI-меню)
Запустите скрипт без параметров, чтобы открыть интерактивное меню (по умолчанию запускается на английском языке, переключить язык можно нажатием `7`):
```bash
python n_osint.py
```
Или сразу запустите интерактивное меню на русском или таджикском языке:
```bash
python n_osint.py -l ru
python n_osint.py -l tg
```

#### Пункты главного меню (на русском):
```text
[1] Поиск по всем сайтам
[2] Поиск по категориям
[3] Поиск с вариациями ника
[4] Поиск по выбранным сайтам (X, Instagram, Steam...)
[5] Список всех сайтов (195)
[6] Настройки (Потоки: 45, Таймаут: 10.0с, Прокси: Нет)
[7] Язык / Language / Забон (Русский)
[0] Выход
```
> 🔙 **Удобная навигация назад:** Если вы зашли в любой пункт меню по ошибке или хотите сменить категорию — просто введите **`0`** и нажмите `Enter`, чтобы вернуться на шаг назад!

---

### 2. Быстрый запуск через командную строку (CLI)

```bash
# Поиск никнейма по всем 195+ сайтам мира:
python n_osint.py durov

# Поиск сразу нескольких никнеймов подряд:
python n_osint.py durov torvalds

# Поиск только в выбранных категориях (соцсети, мессенджеры и игры):
python n_osint.py username -c social messengers gaming -l ru

# Точечный поиск только по конкретным соцсетям:
python n_osint.py username -s X Instagram TikTok Threads Telegram LinkedIn Steam

# Поиск с генерацией вариаций никнейма и автосохранением всех отчётов в папку reports/:
python n_osint.py username --variations -o reports/

# Настройка количества потоков, таймаута и прокси:
python n_osint.py username -n 80 -t 8 --proxy http://127.0.0.1:8080

# Вывести таблицу всех категорий или полный каталог сайтов:
python n_osint.py --list-categories -l ru
python n_osint.py --list-sites -l ru
```

---

## ⚠️ Дисклеймер (Отказ от ответственности)

Инструмент **N-OSINT** создан исключительно в **образовательных, исследовательских целях и для проведения легальных OSINT-расследований и аудитов безопасности**.
- Программа обращается **только к общедоступным публичным веб-страницам**.
- Инструмент не осуществляет обход авторизации, подбор паролей или доступ к закрытым персональным данным.
- Автор (**Dem1**) не несёт ответственности за любое неправомерное использование данного программного обеспечения.

---

<div align="center">

**N-OSINT** • Created by **Dem1**

</div>
