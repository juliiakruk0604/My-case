# Доработка профиля — конкретные замены

Каждое изменение обосновано цитатой из реальной вакансии (см. research/04-demand-evidence.md).
Формат: что меняем → кого это приводит → доказательство.

---

## 1. ЗАГОЛОВОК

**Сейчас:**
`Product & Web Designer | SaaS, Fintech & Agency Sites`

**Заменить на:**
`SaaS & Fintech Product Design + Next.js Build | Dashboards, Design Systems`

**Что меняется и зачем:**

| Убрали | Почему |
|---|---|
| `Web Designer` | Ключевое слово дешёвого сегмента. По нему тебя находят заказчики сайтов за $200–500 («A Website to use for markerting my beauty therapy business», $200) |
| `Agency Sites` | То же самое: агентские и маркетинговые сайты — это сегмент, где заявки подают по $100 без разброса |

| Добавили | Почему |
|---|---|
| `Dashboards` | 3 из 10 дорогих вакансий требуют портфолио именно с дашбордами/SaaS и прямо исключают остальных: «demonstrated experience branding SaaS platforms or analytical dashboards — **not** e-commerce or lifestyle brands» ($5 000) |
| `Design Systems` | Твой реальный актив — 64-компонентная система. Это слово ищут продуктовые команды, а не владельцы лендингов |
| `Next.js Build` | Редкая комбинация с дизайном. Не поднимает цену сама по себе (проверено: «Figma + сборка» есть и в вакансиях за $10), но снимает у продуктовой команды вопрос «кто это соберёт» |

---

## 2. ПЕРВАЯ СТРОКА ОВЕРВЬЮ

В превью профиля видна только первая строка. Сейчас в ней стоит `agency marketing sites` —
то есть первое, что видит дорогой заказчик, это слово из дешёвого сегмента.

**Заменить первый абзац на:**

```
I design SaaS and fintech product interfaces — dashboards, admin panels, B2B flows —
and build them myself in Next.js with a CMS your team can edit without me.

Not e-commerce. Not lifestyle brands. Tech products, where a confusing screen turns
into support tickets and churn you can count.
```

Явный отказ от чужих отраслей — не потеря аудитории, а прохождение фильтра.
Дорогие заказчики отсекают по нише сами и пишут это прямым текстом.

---

## 3. ЧИСЛА: ПРИСТЕГНУТЬ МЕТОД

**Сейчас:** `Support tickets about payout status down 38% in month one.`

Число без базы, без n, без срока, без инструмента. Дорогой заказчик такие цифры не проверяет —
он обесценивает их целиком, вместе с соседними честными.

Доказательство, что это фильтр:
- «unverified claims … will not be shortlisted» ($35 000)
- «propose solutions backed by reasoning, not trends» ($6 500)
- «Why did you choose that direction over other possibilities?» ($6 500)

**Заменить на шаблон (заполнить своими фактами):**

```
Support tickets tagged "payout status" fell 38% — from [X] to [Y] per 1,000 sessions.
Measured in [инструмент] over [N] weeks before vs [N] weeks after launch, n = [сколько].
Method and raw counts are in the case.
```

Правило: каждое число несёт метод. Если метода нет — число надо убрать, а не смягчить.
Убранное число не вредит. Голое число вредит.

---

## 4. ЛИЧНЫЙ ВКЛАД — ОТДЕЛЬНОЙ СТРОКОЙ

Этого в профиле нет вообще. При этом заказчики требуют это прямым текстом:

- «Your **exact personal contribution** — or each proposed contributor's exact contribution — to every example» ($35 000)
- «Generic proposals, undisclosed outsourcing, anonymous team allocation … will not be shortlisted» ($35 000)

**Добавить в каждый кейс и в овервью:**

```
Sole designer and front-end developer on this project. Research, IA, UI, design system,
and the Next.js build. No agency, no subcontractors.
```

Ты действительно работаешь одна — это твоё преимущество, но пока оно нигде не заявлено.

---

## 5. ССЫЛКА НА ПОРТФОЛИО — ПРЯМАЯ И ЖИВАЯ

- «You must provide a direct link to your Figma portfolio. **This is not optional.**» ($6 500)
- «Applications without a portfolio will not be considered.» ($8 500)
- «Template-based work or component libraries **without real client context** will not be considered.» ($6 500)
- «led a **live** e-commerce store redesign» ($6 500)

**Действие:** прямая ссылка на живой продукт и на Figma в каждом кейсе.
Картинки в портфолио Upwork недостаточно — просят именно ссылку.

---

## 6. ЦЕНОВОЙ ЯКОРЬ

**Сейчас:** `Fixed projects from $5,500` и ставка `$38/hr`. Цель — €10 000 (≈ $10 800).

Заявленный минимум вдвое ниже цели. Первая цифра в тексте — это якорь; заказчик
не предложит больше, чем ты назвала.

Данные по ставкам конкурентов в дорогих вакансиях:

| Вакансия | Бюджет | Заявок | Средняя ставка в заявках |
|---|---|---|---|
| XBH Chat | $22 000 | 14 | $21 107 |
| Pitch deck design | $20 000 | 14 | $15 953 |
| KINSTALL (dev) | $35 000 | 23 | $30 358 |
| Marketplace UI | $100 | 8 | $100 (все одинаково) |

В дорогом сегменте подают близко к бюджету, и заявок там мало — 14 на $22 000.

**Замена [ОЦЕНКА, не замер]:** `Fixed projects from $9,000 · 4–6 weeks`, часовая ставка $65–85.
Обоснование: чтобы получать €10k, нижняя граница должна быть под целью, а не вдвое ниже.

---

## 7. ЧТО НЕ ДОБАВЛЯТЬ

**Не добавляй теги и упоминания vibecoding, Cursor, Claude, v0, Lovable.**

Данные: 0 упоминаний этих инструментов как желаемого навыка дизайнера в 15 карточках
с полным текстом; целевой поиск по фразе «vibe coding Cursor v0 Lovable» вернул 0 вакансий.
Единственное упоминание Lovable — в списке **запрещённых** инструментов ($35 000):
«Low-code or no-code application foundations — including Bubble, FlutterFlow, Lovable
or similar platforms — will not be accepted for the production application».

Слово «AI» в вакансиях описывает продукт заказчика («AI-powered SaaS platform»),
а не инструмент дизайнера. AI-скорость — твой внутренний метод, а не то, что продаётся
в заголовке. Продавать надо результат, который эта скорость даёт.

---

## 8. ЧТО СОХРАНИТЬ БЕЗ ИЗМЕНЕНИЙ

Это уже работает и сильнее, чем у большинства:

- Диагностика вместо самопрезентации: «the offer is real, but the page makes the founder
  explain it on a call» — говорит о боли покупателя, а не о твоих умениях.
- Финальный CTA: «Send your URL. I'll reply with one specific observation — not a pitch.»
  Снимает барьер входа и обещает конкретику, а не продажу.
- Порядок работы «positioning and sitemap before mockups» — прямо отвечает на запрос
  «propose solutions backed by reasoning, not trends».

---

## Порядок действий

0. Снять ограничение аккаунта. API отдаёт `suspended: true`, connects = 0, отклики
   отправить невозможно. До этого пункты ниже не дают эффекта.
1. Заголовок (п.1) — минута работы, меняет, кто тебя находит.
2. Первая строка овервью (п.2) — меняет, кто открывает профиль.
3. Личный вклад и метод у чисел (п.3, п.4) — проходят фильтр «unverified claims».
4. Прямые ссылки в кейсах (п.5).
5. Ценовой якорь (п.6) — после того как в портфолио появятся 2–3 кейса с методом.

## Про твою нулевую историю

Формально она почти не мешает: фильтр по Job Success Score выставлен только
в 2 из 10 дорогих вакансий, а требований «Top Rated» или «N выполненных работ»
в текстах 15 карточек нет вообще.

Отсекают не цифры профиля, а содержание заявки:
«Applications without a Figma link, without screening question answers, or with vague
or templated responses will be **rejected immediately**» ($6 500).
