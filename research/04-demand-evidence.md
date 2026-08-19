# Доказательная база по реальному спросу — Upwork, данные на 19.08.2026

## Методология и ограничения (читать перед выводами)

Аккаунт Yuliia Kruk (org_uid 1826266862556997861) помечен Upwork как **suspended**, connects_balance = 0. Несмотря на это, `find_jobs` (action=search и action=get) отработал и вернул полные данные объявлений, включая screening questions, preferred_qualifications и статистику ставок конкурентов (bid stats). Подать заявку (`can_apply`) система не даёт — это ожидаемо при suspended-статусе.

Инструмента поиска фрилансеров/конкурентов в доступном MCP-наборе Upwork **нет** (проверено через поиск по каталогу инструментов — есть только `find_jobs`, `find_saved_jobs`, `get_profile`, `get_messages`, `list_freelancer_proposals` и т.п., ни один не даёт поиск чужих профилей). Поэтому пункт про конкурентов ниже закрыт честно: сравнить профили-победители по этой методике нельзя, только по количеству откликов на конкретные вакансии.

Собрано и открыто полными карточками (`action=get`) 15 вакансий: 10 с бюджетом $5 000+ (fixed) в нишах SaaS/fintech/B2B/AI, 5 с бюджетом ≤ $500. Плюс ещё ~35 карточек просмотрены только в виде сниппетов поиска (`action=search`, поля title/skills/budget/proposal_count) — они использованы только для подсчёта частот по заголовкам и тегам навыков, не для цитат. Поиск по фразе "vibe coding Cursor v0 Lovable" (fixed, без ограничения бюджета) вернул **0 результатов** — зафиксировано как факт, не как вывод.

Выборка мала (15 карточек с полным текстом) — все частоты ниже даны как "N из 15" / "N из 10" / "N из 5", это не репрезентативная статистика по всему Upwork, а факт по просмотренной выборке.

---

## 1. Язык спроса — дословные цитаты

### Как формулируют задачу (высокий бюджет, $5k+)

1. "We're looking for a design partner to help us elevate our brand and Shopify store to the next level" — GOIMU, $20 000, ID 2089969734271586379, опубл. 19.08.2026
2. "No template work. We need a partner who can deeply understand our brand, our customers, and our growth goals — then design from that understanding. If your approach starts with 'pick a theme and customize it,' we're probably not a fit." — GOIMU, $20 000
3. "Conversion-first, not design for design's sake." — GOIMU, $20 000
4. "Fully custom design of the homepage and every site page — templates are explicitly disallowed." — UI/UX Designer for Web Projects (Ideate Creative), $5 000, ID 2085347603626015730
5. "Present at least 3 distinct design concepts/directions to the Center for selection and approval BEFORE full-screen design begins." — там же
6. "We need a UX/UI design master to build a consumer-facing app with a deep understanding of design, neuroscience, and AI-driven design." — UX/UI Designer for Telehealth App, $50 000, ID 2085216606965897238
7. "The ideal candidate should be detail-oriented, obsessed with perfection, and proficient in AI and agentic design." — там же
8. "This is NOT a general presentation design job. We specifically need someone who has worked on real investor/fundraising decks before." — UX/Visual Designer, $20 000, ID 2084203271295997302
9. "We are looking for an exceptional Senior UI/UX Designer to lead the complete design of a premium AI-powered SaaS platform from concept to final developer-ready designs." — Senior UI/UX Designer AI SaaS Platform, $8 500, ID 2072394812824177875
10. "We value quality over speed and are looking for a long-term design partner for future phases of the product." — там же
11. "You have demonstrated experience branding SaaS platforms or analytical dashboards — not e-commerce or lifestyle brands. We need someone who understands how to make a tech product feel trustworthy, modern, and conversion-ready." — SaaS Branding & UI/UX for AI Video Platform, $5 000, ID 2078191743011694091
12. "We are undertaking a comprehensive redesign of Cleanprogram.com… This is not a cosmetic refresh or template application. We need a strategic design partner who can audit our current design patterns, identify user friction points…" — Shopify DTC Redesign & Design System Audit, $6 500, ID 2081207523948181677
13. "Apply if you understand skincare or beauty e-commerce, or if you have worked on similar DTC brands." — там же
14. "This is not a prototype, disposable MVP, generic quoting tool or visual redesign of an existing application." — KINSTALL B2B SaaS (dev-роль, $35 000), ID 2088299779008397024
15. "Design Challenges… Structural Identity Separation… Privacy-First Design… Design for concealed notifications by default." — XBH Chat, $22 000, ID 2085819634211151158

### Как формулируют задачу (низкий бюджет, ≤ $500)

16. "We need a designer to turn an AI concept into a polished, production-ready UI for a mobile app." — $10, ID 2089807610715939797
17. "High-quality work is more important to me than the lowest price." — Figma + Webflow Landing Page Designer, бюджет указан как $10 (плейсхолдер), ID 2089805553293523459
18. "Start your proposal with 'WEBFLOW' so I know you read the brief." — там же
19. "Hi, I need a complete redesign of my existing site consist of 7 pages. Please include a fixed price for this other than my budget I mentioned, I want it to start asap." — Website Redesign, $200, ID 2089846935848620716
20. "A Website to use for markerting my beauty therapy business" (орфография заказчика сохранена) — $200, ID 2089688095722152917
21. "Need a web design for Landscaping services. Good domain" — $41, ID 2089751105923658692
22. "Homepage, browse/grid page (with a 'Featured' vs 'standard' listing split), individual profile pages… Multi-step profile creation wizard… We have a detailed written product spec ready to share" — Marketplace UI/UX Designer, $100, ID 2089960214068603441 (детальный бриф при мизерном бюджете)
23. "Must be familiar with FlutterFlow… Please share relevant examples of similar work, especially splash or intro screen animations" — $50, ID 2089936561269549872

### Как описывают требования к портфолио (буквально)

24. "Can you show me strong examples of your projects?" — screening question, XBH Chat, $22 000
25. "Please send 5 examples of your work. If you have experience in non-profit, that would be great." — screening question, $5 000 (Ideate Creative)
26. "Must have: Prior experience designing pitch decks / fundraising decks (please share 1–2 samples — no exceptions, we need to see actual deck work, not generic slide design)" — $20 000
27. "Applications without a portfolio will not be considered." — $8 500 AI SaaS
28. "A portfolio featuring premium SaaS products… Three projects that best demonstrate your UI/UX expertise." — $8 500 AI SaaS
29. "Strong portfolio is the #1 filter. We'll be reviewing the first applications as a team and shortlisting based on portfolio quality before scheduling any calls." — $5 000 SaaS Branding
30. "You must provide a direct link to your Figma portfolio (for example, figma.com/@yourname). This is not optional." — $6 500 Shopify DTC
31. "Template-based work or component libraries without real client context will not be considered." — там же
32. "Applications without a Figma link, without screening question answers, or with vague or templated responses will be rejected immediately." — там же
33. "Do not submit AI-generated or generic answers. We can tell, and we will not move forward." — там же (страх не перед AI-инструментами дизайна, а перед AI-сгенерированными ответами на скрининг)
34. "Links to your best 3 to 5 Webflow websites that are similar in quality and scope." — $5 000 B2B redesign
35. "Two or three relevant production SaaS examples; Your exact personal contribution—or each proposed contributor's exact contribution—to every example." — $35 000 KINSTALL (dev, но формулировка доказательной базы показательна)
36. "Generic proposals, undisclosed outsourcing, anonymous team allocation, unverified claims and portfolios without a clear explanation of personal contribution will not be shortlisted." — там же

Низкий бюджет — требования к портфолио заметно короче: "Please share relevant examples of similar work" (ID 2089936561269549872, $50) и "3 relevant Figma/Webflow landing pages you have designed and built" (ID 2089805553293523459, $10) — без слов "no exceptions", "will not be considered", без указания ниши.

---

## 2. Требования-фильтры и их частота (из 10 карточек с бюджетом $5k+, полный текст)

| Требование в тексте вакансии | Частота |
|---|---|
| Явный порог лет опыта (5+, 7+ и т.п.) | 2 из 10 (ID 2072394812824177875 — "5+ years"; ID 2078191743011694091 — "7+ years") |
| Требование именно нишевого портфолио (SaaS/фінтех/B2B, явный отказ от e-commerce/lifestyle) | 3 из 10 (2078191743011694091, 2081207523948181677, 2072394812824177875) |
| Жёсткая формулировка отказа без портфолио/ссылки ("will not be considered", "rejected immediately") | 3 из 10 (2072394812824177875, 2081207523948181677, отчасти 2084203271295997302 "no exceptions") |
| Требование готового кода / сборки, а не только Figma (двухфазный Figma→разработка обязателен) | 1 из 10 явно обязательный (2079965929643651204, Figma+Webflow); ещё 1 — опционально (2089969734271586379, GOIMU: "You don't need to cover all four areas") |
| Developer handoff как формат сдачи (не обязательно значит "designer сам кодит") | 3 из 10 (2072394812824177875, 2081207523948181677, 2089969734271586379) |
| Явный запрос "готовность работать с их разработчиками / командой продукта" | 2 из 10 (2085216606965897238 "working with a team", 2072394812824177875 "collaborating with developers and product teams") |
| Числовые фильтры Upwork (min Job Success Score) выставлены в самой вакансии | 2 из 10 (ID 2085819634211151158 — JSS 90; ID 2085347603626015730 — JSS 90 + rising_talent) |
| Явное требование к живым/отгруженным продуктам в портфолио ("live", "shipped", "production") | 2 из 10 (2081207523948181677 — "led a redesign of a live e-commerce store"; 2072394812824177875 — "premium SaaS products") |

Из 5 карточек с бюджетом ≤ $500: ни одна не содержит порога лет опыта, нишевого требования к портфолио или JSS-фильтра. Требование "показать примеры" встречается в 3 из 5, но в общей формулировке ("share relevant examples", "3 relevant… pages") без слов "no exceptions" / "will not be considered".

---

## 3. Отличия: бюджет $5k+ vs ≤$500 (15 карточек, 10 vs 5)

Что встречается в высоком бюджете, но не встречается в низком (в этой выборке):
- Явный отказ от шаблонов как условие: "templates are explicitly disallowed" / "No template work" — 3 из 10 высоких, 0 из 5 низких.
- Требование нишевого портфолио (конкретно SaaS/фінтех/дашборды, с явным исключением e-commerce/lifestyle) — 3 из 10 vs 0 из 5.
- Жёсткие отказные формулировки к неполным заявкам ("rejected immediately", "will not be considered", "no exceptions") — 3 из 10 vs 0 из 5.
- Запрос обоснования решений/reasoning, а не просто визуала: "propose solutions backed by reasoning, not trends", "Why did you choose that direction over other possibilities?" — присутствует в $6 500 Shopify DTC; в низкобюджетных карточках такого запроса reasoning не встречено.
- Указание на долгосрочное партнёрство/будущие фазы: "long-term design partner for future phases" ($8 500), "There may be opportunities for additional Webflow/Figma work if this project goes well" — последнее фактически встретилось и в низкобюджетной карточке ($10, ID 2089805553293523459), так что этот пункт **не** является чистым различителем.

Что совпадает в обеих группах (не различитель, вопреки ожиданию):
- Запрос "показать примеры работ" есть и там, и там — разница в жёсткости формулировки, не в самом факте запроса.
- Требование "Figma + сборка сайта" (не только дизайн) встречается и в дешёвых карточках: "Figma + Webflow Landing Page Designer" за $10 (плейсхолдер) и "Figma to Squarespace Designer" за $10 — обе требуют и дизайн, и вёрстку. Тезис "дёшево — это только Figma, дорого — это ещё и код" в данной выборке **не подтверждается**: количество примеров одинаково мало (по 2) в обеих группах.
- Длина брифа не всегда коррелирует с бюджетом: маркетплейс за $100 (ID 2089960214068603441) имеет подробный бриф ("детальный product spec"), сопоставимый по детальности с $5 000-вакансиями.

---

## 4. Упоминания AI-инструментов и "vibe coding"

Прямой поиск по фразе "vibe coding designer Cursor v0 Lovable" (fixed, без ограничения бюджета) — **0 результатов** из выдачи Upwork search.

В 10 карточках с бюджетом $5k+ (полный текст):
- "Cursor", "Claude", "v0", "vibe coding" — **0 упоминаний**.
- "Lovable" — 1 упоминание, но как явно **запрещённый** инструмент для разработчика: "Low-code or no-code application foundations—including Bubble, FlutterFlow, Lovable or similar platforms—will not be accepted for the production application" (KINSTALL, $35 000). Это вакансия на full-stack разработку, не на дизайн.
- "AI-assisted development tools may be used responsibly, but the selected provider remains fully accountable for architecture, security, licensing, code quality, testing, documentation, correctness and maintainability" (там же) — AI как инструмент допускается, но ответственность остаётся на человеке, не как требуемый навык.
- "AI-driven design" / "proficient in AI and agentic design" — 1 упоминание (Telehealth, $50 000) — единственный случай, где AI прямо назван желаемым навыком дизайнера, без конкретики (без названия инструментов).
- "AI-powered" в 4 из 10 карточек, но во всех случаях это описание **продукта клиента** ("AI-powered SaaS platform", "AI Video Platform"), а не требование к инструментам дизайнера.

В карточках с бюджетом ≤$500:
- "We need a designer to turn an AI concept into a polished, production-ready UI" ($10) — клиент уже сгенерировал AI-концепт и ищет человека, чтобы довести до продакшена. Аналогичная формулировка встретилась и в отдельно просмотренной карточке $5 000 (health supplement ads): "I use AI tools to concept and generate static image ads, and I need a skilled graphic designer to take my AI-generated comps and bring them to production-ready quality" — то есть сценарий "AI сделал набросок, нужен человек для доводки" встречается в обеих ценовых группах, не только в дешёвой.

Честный вывод по частоте (без интерпретации, только счёт): в просмотренной выборке заказчики почти никогда не называют конкретные AI-кодинг-инструменты (Cursor/Claude/v0/Lovable) как желаемый навык дизайнера; единственное упоминание Lovable — как отвергаемый инструмент для продакшен-разработки. "AI" как слово фигурирует часто, но в основном как характеристика продукта клиента, а не как требование к процессу дизайнера.

---

## 5. Конкуренты

Инструмента поиска профилей фрилансеров в доступном наборе Upwork MCP нет — проверено явным запросом по каталогу инструментов, найдены только `find_jobs`, `find_saved_jobs`, `get_profile` (только свой профиль или по known profile_key), `get_messages`, `list_freelancer_proposals`. Сравнить заголовки/портфолио/ставки выигрывающих фрилансеров напрямую нельзя.

Косвенные данные, которые доступны через `action=get` по каждой вакансии (bid stats конкурентов):
- XBH Chat ($22 000, 14 заявок): диапазон ставок в заявках $9 500–$22 000, средняя $21 107.
- Telehealth ($50 000, 99 заявок): диапазон $5–$51 000, средняя $42 222 — разброс аномально широкий (вероятно, часть ставок — почасовые контракты, ошибочно попавшие в fixed-статистику, либо намеренно заниженные "разведочные" заявки).
- KINSTALL ($35 000, 23 заявки): диапазон $1 000–$75 000, средняя $30 358.
- UX/Visual Designer, pitch deck ($20 000, 14 заявок): диапазон $1 200–$20 000, средняя $15 953.
- Marketplace UI/UX ($100, 8 заявок): все ставки ровно $100 — на низком бюджете разброс ставок отсутствует, конкуренты просто соглашаются на заявленную цену.
- Figma+Webflow Landing ($10 плейсхолдер, 14 заявок, 1 нанят): диапазон $10–$1 000, средняя $174 — здесь виден "плейсхолдер-бюджет" эффект: реальные заявки сильно выше заявленной цифры.

Дальше этого фактов нет — кто именно выигрывает и что у них в заголовке/портфолио, из доступных инструментов не установить.

---

## 6. Барьер новичка (нулевая история на платформе)

Из preferred_qualifications 10 карточек $5k+: `has_portfolio` везде стоит `false` (это служебное поле, не требование клиента), `min_hours_worked` везде `0`. `min_job_success_score` выставлен и ненулевой только в 2 из 10 карточек (ID 2085819634211151158 — 90; ID 2085347603626015730 — 90, плюс `rising_talent: true` и `min_earnings: "$100+"`). В остальных 8 из 10 этот платформенный фильтр равен 0 — то есть формального отсева по истории Upwork через системные настройки вакансии в 80% просмотренных дорогих карточек нет.

Из 5 карточек ≤$500: во всех `min_job_success_score` = 0, `has_portfolio` = false, `min_hours_worked` = 0 — платформенных фильтров нет вообще ни в одной.

Явных текстовых упоминаний "Top Rated", "must have X completed jobs on Upwork", "0 reviews will be rejected" в текстах 15 просмотренных карточек — **0**. Барьер, который реально виден в тексте, — не платформенная статистика, а требование доказательств (портфолио, конкретные ссылки, "your exact personal contribution", ответы на скрининг без признаков AI-генерации) — то есть отсекается не по цифрам профиля, а по содержанию заявки.

---

## Итог по фактам (без выводов и рекомендаций)

15 карточек с полным текстом (10 дорогих, 5 дешёвых) — вот что зафиксировано:
- Платформенный фильтр по Job Success Score стоит в 2 из 10 дорогих вакансий и в 0 из 5 дешёвых.
- Нишевое требование к портфолио (конкретно SaaS/дашборд/фінтех, с явным исключением других категорий) — в 3 из 10 дорогих, в 0 из 5 дешёвых.
- Жёсткие отказные формулировки к неполной заявке — в 3 из 10 дорогих, в 0 из 5 дешёвых.
- Требование "и Figma, и код" встречается в обеих группах (1 явное и 1 опциональное из 10 дорогих; 2 из 5 дешёвых) — не является чистым различителем в этой выборке.
- Прямые упоминания Cursor/Claude/v0/vibe coding — 0 из 15 карточек и 0 в отдельном целевом поиске.
