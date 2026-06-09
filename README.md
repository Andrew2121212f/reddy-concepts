# Reddy — Konsept Markalar / Концепты брендов для Турции

Набор **дизайн-концептов** локальных турецких бет-брендов. Каждый сайт — статичный HTML-шаблон: красивый, с анимациями и ховерами, **без бэкенд-функционала**. Анимации на [Motion](https://motion.dev) (через CDN). Логотипы — реальные (из брендбука Reddy), в SVG.

## Бренды (8)

| Бренд | Концепция | Папка | Лого |
|---|---|---|---|
| **Ankabet** | Феникс-тюльпан / Анкара, премиум sport+casino | `public/brands/ankabet/` | ✓ |
| **Meydan** | Арена/площадь, live-ставки, фан-комьюнити | `public/brands/meydan/` | ✓ |
| **Risk Al** (Take A Risk) | Риск как осознанный выбор, монета, бирюза | `public/brands/takearisk/` | ✓ |
| **Altın Günü** | «Золото объединяет Турцию», традиция | `public/brands/altingunu/` | ✓ |
| **Dünyası** | «Türkiye'nin Spor Dünyası», спорт-медиа | `public/brands/dunyasi/` | ✓ |
| **SporSepeti** | Маркетплейс/агрегатор БК и бонусов | `public/brands/betsepeti/` | ✓ |
| **The Roman Bet** | Римско-византийская Анатолия, арена (концепт) | `public/brands/romanbet/` | wordmark |
| **The Big Fix** | Нео-нуар, джекпот, казино/слоты (концепт) | `public/brands/bigfix/` | wordmark |

> The Roman Bet и The Big Fix — оригинальные концепты (брифа/лого не было), пока с текстовым wordmark.
> SporSepeti — бюро дало нейминг Spor/Maç/Taraftar Sepeti (не «BetSepeti»); стоит лого SporSepeti.

## Как смотреть локально

Любой статический сервер из папки `public/`:

```bash
npx serve public
# или: python -m http.server -d public 8080
```

Открыть `http://localhost:8080/` — это **хаб** (галерея), откуда открываются все концепты.

## Деплой — GitHub Pages

Пушится в `github.com/Andrew2121212f/reddy-concepts`. Workflow `.github/workflows/deploy.yml` публикует `public/` через GitHub Actions.

Живой адрес: **https://andrew2121212f.github.io/reddy-concepts/**

> Если Pages не включились автоматически: Settings → Pages → Source = **GitHub Actions**, затем перезапустить workflow.

## Структура

```
public/
├── index.html                 # хаб-галерея
└── brands/<slug>/
    ├── index.html             # автономный концепт бренда
    ├── logo.svg               # реальный логотип (где есть)
    └── logo.png
```

Все ссылки — относительные (Pages отдаёт по подпути `/reddy-concepts/`).
