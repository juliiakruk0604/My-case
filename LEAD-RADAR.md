# Лид-радар — автономная машина захвата клиентов

Цель: 24/7 ловит преквалифицированных лидов (застрявшие vibe-кодеры + fintech/SaaS design-build),
Claude их оценивает и пишет персональный оффер, ты получаешь готовое «нажать отправить».
Крутится, пока ты в выгорании. Метрики — маркетинговые (reply/booking/close), не лайки.

---

## АРХИТЕКТУРА (цепочка)

```
[Источники: RSS/вебхуки] → [Фильтр по ключам] → [Claude: скоринг + оффер]
   → [Фильтр: score ≥ 60] → [Airtable: строка-лид] → [Telegram/email: пинг с черновиком]
```

Один Zap на источник (или мульти-фид). Всё native + Claude (уже подключён).

---

## 1. ИСТОЧНИКИ (breadth) — как достать RSS каждого

Поправка: у **Upwork и Wellfound своего RSS НЕТ** (Upwork убрал ~2019). Часть — нативный RSS,
часть — через Google Alerts / генератор.

**A. Готовые нативные RSS (вставить в Zapier как есть):**
- RemoteOK: `https://remoteok.com/remote-design-jobs.rss`
- RemoteOK: `https://remoteok.com/remote-react-jobs.rss`
- RemoteOK: `https://remoteok.com/remote-frontend-jobs.rss`
- We Work Remotely: `https://weworkremotely.com/categories/remote-design-jobs.rss`
- We Work Remotely: `https://weworkremotely.com/categories/remote-front-end-programming-jobs.rss`
- Remotive: `https://remotive.com/remote-jobs/feed/design`

**B. Google Alerts → RSS (гибкий, бесплатный; тащит и то, у чего фида нет):**
1. google.com/alerts → запрос → Show options → **Deliver to: RSS feed** → Create.
2. Клик по иконке RSS у алерта → копируй URL фида → в Zapier.
Запросы: `"built with Lovable"` · `"vibe coded" (help OR stuck OR production)` ·
`"Bolt.new" OR "v0.dev" MVP` · `site:upwork.com fintech designer "Next.js"` (Upwork через индекс Google).

**C. Сайты без RSS (Wellfound, Contra, Upwork-поиск) — генератор RSS.app / Fetchrss:**
- rss.app → вставить URL поиска (напр. `wellfound.com/role/r/product-designer`) → получить RSS-ссылку → в Zapier.

**D. Upwork — лучше не через RSS-костыль, а через MCP/агента** (прогон точнее, без ToS-серости).

**E. Витрины AI-билдеров (фаза 2):** Lovable/Bolt/v0 showcase → Webhooks by Zapier + скрейпер
(или Schedule → raw request). Публичные приложения их юзеров = преквалифицированный ICP.

Подключение: RSS by Zapier → Trigger «New Item in Feed» → URL фида → один Zap на фид.

---

## 2. КЛЮЧЕВЫЕ СЛОВА (для фильтра)

**Ловим (rescue):** Lovable, Bolt.new, v0, Replit, Base44, "vibe coded", "vibe-coding",
"AI built", "MVP to production", "production ready", "finish my app", "no-code to code".

**Ловим (product/fintech):** fintech dashboard, SaaS dashboard, "Next.js" designer,
"design and build", admin panel, B2B SaaS UI, design system.

**Отсекаем (negative):** WordPress, Shopify, Wix, ecommerce, "logo only", "$5", "$10", crypto shill.

---

## 3. ШАГ CLAUDE — скоринг + оффер (готовый промпт для действия «Send Message»)

Вставляешь текст лида в `{{lead_text}}`, `{{lead_url}}`. Claude возвращает JSON:

```
You are a growth-marketing SDR for Yuliia Kruk — a SaaS/fintech product designer who ALSO
ships production Next.js and turns broken AI-built (Lovable/Bolt/v0) apps into shipped
products in days. Read this lead and return ONLY JSON.

LEAD: {{lead_text}}
URL: {{lead_url}}

Return:
{
 "fit_score": 0-100,           // fit for her rescue/product niche
 "segment": "rescue" | "product" | "design" | "skip",
 "why": "one line",
 "budget_signal": "low|mid|high|unknown",
 "hook": "one specific observation about THEIR product/need, not generic",
 "draft_outreach": "<=110 words, her voice, no 'I'm excited', lead with the hook,
                    one proof number (4-day build / ships Next.js), soft CTA to a quick call"
}
Score low and segment 'skip' for e-commerce, WordPress, logo-only, sub-$500.
```

---

## 4. AIRTABLE — база лидов (она же дашборд)

Таблица `Leads`, колонки:
`date · source · title · url · fit_score · segment · budget_signal · hook · draft ·
status(NEW→SENT→REPLIED→CALL→PAID) · sent_at · replied(y/n) · $value · notes`

Rollups сами считают: лидов/день по источнику, средний score, конверсию по воронке.

---

## 5. ПИНГ ТЕБЕ

Telegram/email: только лиды со `score ≥ 60`.
Формат: `[score] segment — title\nhook\n— draft —\n<кнопка: открыть в Airtable>`
Тебе остаётся: прочитать, при желании отправить (1 действие).

---

## 6. МЕТРИКИ (оценка результата — маркетинговая)

Из статусов Airtable считаются автоматически:
- **Lead volume/day** по источнику → какой источник кормит.
- **Reply rate** = REPLIED / SENT → качество оффера/хука.
- **Booking rate** = CALL / REPLIED.
- **Close rate** = PAID / CALL.
- **Payback** = $ / (твоё время). CAC здесь = минуты, не деньги.

Недельный дайджест: Schedule → читает Airtable → Claude сводит «лучший источник/сегмент/хук +
что менять» → email. Решение недели: какой источник и хук масштабировать, какой убить.

---

## 7. ЧТО ПОДКЛЮЧИТЬ / ЧТО НУЖНО ОТ ТЕБЯ

Подключить в Zapier (5–10 мин): **RSS by Zapier**, **Airtable** (или Google Sheets), **Telegram**
(или Gmail). Claude — уже есть.

От тебя — 3 вещи:
1. Твой **cal.com/Contra линк** (в CTA черновиков).
2. С какого **источника стартуем** (Upwork saved-search / RemoteOK / Google Alerts).
3. Куда слать пинги (**Telegram** или email).

Дальше сборка: 1 Zap = Источник → Фильтр → Claude → Фильтр → Airtable → Пинг. ~30–40 мин.
Фаза 2 — витрины Lovable/Bolt (программный аутрич по идеальному ICP).

---

## Приоритет
Это машина №1: делает деньги напрямую и автономна. Dribbble/соцсети — догоняющий слой.
Старт с 1 источника (быстрая победа), потом добавляем фиды и витрины.
