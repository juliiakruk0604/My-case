# Dribbble — система: валидация тегов + продвижение + автоматизация

Не «постить наугад», а рабочая петля: валидированные теги → авто-разлёт → лог → итерация по данным.
Данные о тегах получены разведкой по самому Dribbble (поиск по tags-страницам), 20.08.2026.

---

## ЧЕСТНАЯ КАРТА: что автоматизируется, что нет

| Задача | Автоматизация | Где |
|---|---|---|
| Загрузка шота В Dribbble | ❌ нельзя (нет API/Zapier write) | руками, 2 мин |
| Разлёт ИЗ Dribbble по каналам | ✅ да | Zapier (триггер New Shot) |
| Лог шотов+тегов в таблицу | ✅ да | Zapier → Google Sheets |
| Валидация тегов (находимость) | ⚠️ частично | Dribbble-разведка сейчас + Semrush (нужны юниты) |
| Аналитика лайков/просмотров по шоту | ❌ Dribbble не отдаёт по API | копим в трекере вручную |
| LinkedIn-лента органически | ❌ ограничено | руками |

Semrush для объёмов поисковых запросов — сейчас без API-юнитов: https://www.semrush.com/mcp-access

---

## 1. ВАЛИДИРОВАННЫЕ ТЕГИ (проверено: у каждого есть живая tags-страница на Dribbble)

Правило: на каждый шот **8–12 тегов**, из них **≥4 нишевых** (у которых своя населённая
tags-страница — значит шот попадает в поток, который листают покупатели), остальное — общие.

**Нишевые, подтверждённые живыми страницами:**
`fintech` · `fintech-dashboard` · `fintech-dashboard-ui` · `financial-dashboard` ·
`saas-dashboard` · `saas-dashboard-ui` · `crypto-exchange-app` · `crypto-trading-dashboard` ·
`cryptocurrency-dashboard` · `dark-crypto` · `dashboard` · `design-system` · `data-visualization`

**Общие (добивка, не нести весь вес):** `product-design` · `ui` · `ux` · `web-app` · `dark-ui` · `saas`

**Убрать со старых шотов (тянут не тех):** `interior-design` · `music` · `nft` · `poster` ·
`festival` · `furniture` · `landing-page` (как основной).

### Готовые наборы под твои продуктовые шоты
- **Payout dashboard:** fintech, fintech-dashboard, saas-dashboard, financial-dashboard, dashboard, design-system, data-visualization, product-design, ux, web-app
- **Options builder (before/after):** fintech, fintech-dashboard-ui, crypto-trading-dashboard, dashboard, data-visualization, ux, product-design, dark-ui, web-app, saas
- **Empresex exchange:** fintech, crypto-exchange-app, cryptocurrency-dashboard, dark-crypto, dashboard, design-system, product-design, ui, dark-ui, web-app
- **Receipts (позиционный):** product-design, design-system, fintech, saas, dashboard, ux, ui, case-study, web-app, next-js

---

## 2. ПЕТЛЯ ВАЛИДАЦИИ (автоматическая, накапливает данные)

Dribbble не отдаёт аналитику по API — поэтому валидируем **накоплением**, а не одноразово:

**Zap A — «Shot Logger»**
- **Триггер:** Dribbble → New Shot (уже подключён).
- **Действие:** Google Sheets → Create Row. Колонки: `date, title, url, tags, tag_set_id, likes(ручное), views(ручное), source_channel`.
- Раз в неделю ты вписываешь likes/views (2 мин) → через 6–8 шотов видно, **какой tag_set_id
  реально тянет**. Это и есть валидация по данным, а не по вкусу.

Пометка: помечай наборы тегов id-шками (A/B/C), чтобы петля сравнивала именно наборы.

---

## 3. ПРОДВИЖЕНИЕ (авто-разлёт, «загрузил раз → везде»)

**Zap B — «Fan-out»**
- **Триггер:** Dribbble → New Shot.
- **Действия (ветки):**
  - X/Twitter → Create Tweet (title + ссылка на шот + 2–3 тега).
  - Threads/Telegram-канал → Post (картинка шота из `images__hidpi` + подпись).
  - Buffer/Facebook Page → Add to Queue.
  - (LinkedIn-лента органически — руками, отдельная кнопка.)
- Подпись берём из `DRIBBBLE-copy.md` (метод под числом).

**Zap C — «Cadence nudge» (необязательно)**
- **Триггер:** Schedule by Zapier (раз в 7–10 дней).
- **Действие:** напоминание тебе (email/Telegram) «пора шот» + ссылка на след. заготовку.

---

## 4. КАК ЭТО СОБРАТЬ (Zap'ы строятся в веб-Zapier, не отсюда)

Этот MCP выполняет разовые действия, но постоянные «всегда-включённые» Zap'ы настраиваются в
интерфейсе zapier.com. Порядок:
1. zapier.com → Create Zap → Trigger: **Dribbble → New Shot** → выбрать твой connected аккаунт.
2. Добавить Action: **Google Sheets → Create Spreadsheet Row** (Zap A) — подключить твой Google.
3. Второй Zap: тот же триггер → Action **Twitter/Telegram/Buffer** (Zap B) — подключить каналы.
4. Включить. Дальше: грузишь шот на Dribbble → лог и разлёт идут сами.

Что могу сделать я отсюда прямо сейчас (разовыми действиями MCP), если каналы подключены в Zapier:
- по факту нового шота — вручную прогнать кросс-пост в подключённый канал;
- завести и наполнить трекер-таблицу.

---

## Порядок под выгорание
1. Залить 4 продуктовых шота готовым пакетом (тексты + теги выше) — это уже валидированные теги.
2. Собрать Zap A (лог) и Zap B (разлёт) — один раз, ~30–40 мин в Zapier.
3. Дальше: 1 шот в 7–10 дней → система сама логирует и разносит. Ты жмёшь Publish и вписываешь 2 числа.

Приоритет прежний: это витрина в фоне. Деньги — Contra/Braintrust/Upwork.
