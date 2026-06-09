# Reddy — Konsept Markalar / Концепты брендов для Турции

Набор **дизайн-концептов** локальных турецких бет-брендов. Каждый сайт — статичный HTML-шаблон: красивый, с анимациями и ховерами, **без бэкенд-функционала**. Анимации на [Motion](https://motion.dev) (через CDN). Лого пока текстовые (wordmark), позже заменятся на PNG.

## Бренды (8)

| Бренд | Концепция | Папка |
|---|---|---|
| **Ankabet** | Феникс / Анкара, премиум sport+casino | `public/brands/ankabet/` |
| **Meydan** | Арена/площадь, live-ставки, фан-комьюнити | `public/brands/meydan/` |
| **Risk Al** (Take A Risk) | Риск как осознанный выбор, монета, бирюза | `public/brands/takearisk/` |
| **Altın Günü** | «Золото объединяет Турцию», традиция | `public/brands/altingunu/` |
| **Dünyası** | «Türkiye'nin Spor Dünyası», спорт-медиа | `public/brands/dunyasi/` |
| **BetSepeti** | Маркетплейс/агрегатор БК и бонусов | `public/brands/betsepeti/` |
| **The Roman Bet** | Римско-византийская Анатолия, арена | `public/brands/romanbet/` |
| **The Big Fix** | Нео-нуар, джекпот, казино/слоты | `public/brands/bigfix/` |

## Как смотреть локально

Любой статический сервер из папки `public/`. Например:

```bash
# вариант 1 — встроенный в современный node (нужен npx)
npx serve public

# вариант 2 — питон, если есть
python -m http.server -d public 8080
```

Затем открыть `http://localhost:8080/` — это **хаб** (галерея), откуда открываются все концепты.

## Деплой — GitLab Pages

Пушится в `gitlab.com/teroser23/reddy-concepts`. Пайплайн `.gitlab-ci.yml` публикует `public/`.
Живой адрес: **https://teroser23.gitlab.io/reddy-concepts/**

## Структура

```
public/
├── index.html          # хаб-галерея
├── assets/             # стили/скрипты хаба
└── brands/<slug>/index.html   # автономный концепт каждого бренда
```

Все ссылки — относительные (Pages отдаёт по подпути `/reddy-concepts/`).
