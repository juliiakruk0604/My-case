# Публикация №1 — сегодня, 20.08.2026

Первый пост серии. Задача не «набрать охват», а поставить утверждение, к которому
будут крепиться все следующие четыре разбора. Поэтому он на **твоих собственных
проверяемых числах**, а не на чужом экране.

**Допущение, называю вслух:** основная площадка — личный профиль LinkedIn.
Профиль я не видел (доступа нет). Если его нет или он пустой — сначала одно поле:
заголовок профиля = строка позиционирования из `BRAND-7days.md` §1. Пятнадцать минут.

**Время:** вторник–четверг, 09:00–11:00 по Центральной Европе — окно, когда
фаундеры ЕС читают ленту до начала дня. Сегодня четверг: публиковать до 11:00,
иначе перенести на 21.08 в 09:00 и сегодня отправить письмо в поддержку Upwork.

**Ссылку в тело поста не ставить.** Ссылка — первым комментарием, сразу после публикации.

---

## Текст для LinkedIn — копировать как есть

```
5 colors. In the entire product.

That's not a style choice. It's the only way I know to build a screen someone will
trust with their money.

Raw counts from the last site I built. Anyone can verify them in the repo in ten seconds:

— 5 colors, whole project
— 3 breakpoints, written by hand. No auto-reflow.
— 869 lines of my own code, 6 components
— 2,862 lines I did not write, because shadcn had already written them
— 10 commits. First commit 12 Aug, live 15 Aug. Four days.

Method: counted with grep over the config and the markup on 19 Aug 2026; dates from
git log --reverse. Measured, not estimated.

I don't add. I subtract.

Every screen I take on loses one typeface, one color, and one step between the user
and the thing they came for. A large palette proves you own an eyedropper. A constraint
proves you made a decision — and a decision is the only thing a user can feel in four
seconds.

Four seconds is about what a fintech screen gets. Crypto exchange, payout dashboard,
B2B billing: before anyone reads a word of your copy, they've decided whether this
looks like it can hold their money. Decoration doesn't buy those four seconds.
Removing everything that isn't the decision does.

So, for the next two weeks, in public: one real SaaS or fintech screen, rebuilt.
Before and after with the counts. Plus what I predict will change, and the condition
under which I'll call myself wrong. Then I send it to the founder. Free, finished,
no meeting.

Want yours to be the first one? Send the URL. I'll reply with one specific
observation — not a pitch.
```

Первым комментарием:

```
Repo with the counts: [ссылка]
The case this method came out of: [ссылка]
```

### Почему текст устроен так

| Элемент | Что делает | Кто приходит |
|---|---|---|
| `5 colors.` первой строкой | В превью до «see more» видны ~210 знаков. Число без контекста заставляет раскрыть | Все, кто увидел |
| Строка `2,862 lines I did not write` | Признание, которое никто не делает. Доказывает метод сильнее, чем ещё одна похвала себе | Технический фаундер: он проверит и увидит, что не соврала |
| `Method:` с инструментом и датой | `SPEC.md` §3. Прямой ответ на фильтр «unverified claims will not be shortlisted» | Заказчик с бюджетом $5 000+: 3 из 10 таких вакансий отсеивают именно по этому |
| `four seconds` | Твоя формулировка из кейса Empresex, переведённая в отраслевой контекст | Финтех / крипта / B2B-биллинг |
| Анонс двух недель разборов | Превращает пост в обещание с датой. Следующие посты читаются как серия | Те, кто вернётся на второй |
| `Send the URL… not a pitch` | Твоя строка из профиля, лучший её элемент. Отправитель ничего не теряет | Входящий адресат — тот, кому потом можно продать ступень 1 |

Чего в тексте намеренно нет: цифры 38%, слова «passionate», «pixel-perfect», «user-centric»,
превосходных степеней и ни одного прилагательного о собственном вкусе.

---

## Вариант для польского рынка

Отдельным постом, **не сегодня — в понедельник 24.08**. Два поста в один день дробят охват.
Краков — реальный рынок для ступени €2 000, и польский у тебя свободный: это преимущество,
которым сейчас не пользуется никто из твоих конкурентов на английском.

```
5 kolorów. W całym produkcie.

To nie kwestia stylu. To jedyny znany mi sposób, żeby zbudować ekran, któremu ktoś
powierzy swoje pieniądze.

Surowe liczby z ostatniej strony, którą zbudowałam — każdy sprawdzi je w repo w 10 sekund:

— 5 kolorów w całym projekcie
— 3 breakpointy, napisane ręcznie
— 869 linii mojego kodu, 6 komponentów
— 2 862 linie, których nie napisałam, bo napisał je już shadcn
— 10 commitów. Pierwszy 12 sierpnia, produkcja 15 sierpnia. Cztery dni.

Nie dodaję. Odejmuję.
Każdy ekran traci u mnie jeden krój, jeden kolor i jeden krok między użytkownikiem
a tym, po co przyszedł.

Przez dwa tygodnie robię to publicznie: jeden prawdziwy ekran SaaS lub fintech,
przebudowany, z liczbami przed i po. Za darmo, gotowe, bez spotkania.

Chcesz, żeby to był twój? Wyślij URL. Odpiszę jedną konkretną obserwacją — nie ofertą.
```

---

## Картинка — 1080×1350, одна

Делаешь в Figma, 30–40 минут. Токены уже зафиксированы в `HANDOFF.md`,
изобретать не надо. Арт-дирекшн твой, ниже — только границы.

**Что это:** страница бортжурнала, а не обложка кейса.

```
Фон            #141414
Панель         #212020
Текст          #FFFFFF / #AEABAB / #918F8F
Акцент         #EF7759 — не больше 3% площади. Только на числе «5» и на слове MEASURED
Шрифт величин  JetBrains Mono
Радиусы        16px панель, 12px блок
```

**Композиция:**
- Верх: `5` — крупно, акцентом. Под ним мелким моноширинным: `colors in the entire product`
- Центр: пять строк-величин, выключка по краям, между ключом и значением — лидер из точек:

```
colors ....................................... 5
breakpoints, hand-written .................... 3
lines of my own code ....................... 869
lines I did not write .................... 2 862
first commit → production ............... 4 days
```

- Низ, мелко, серым `#918F8F`:
  `METHOD — grep over config and markup, 19 Aug 2026 · dates from git log --reverse`
- Подпись в самом низу: `Yuliia Kruk — Product Designer, SaaS / Fintech`

**Запрещено** (`SPEC.md` §5): мокапы в перспективе, градиенты, скриншоты интерфейса,
стоковые фото, слова Problem / Process / Solution / Result.

Плотность чисел выше плотности слов. Если картинку можно спутать с чьей-то ещё —
она не та.

---

## Дублирование в тот же день

**Dribbble** — та же картинка, подпись:

```
5 colors in the entire product. 3 breakpoints, hand-written. 869 lines of my own code.
First commit to production: 4 days.

Counted with grep on 19 Aug 2026, not estimated.

I design SaaS and fintech interfaces and ship them in Next.js.
Next two weeks: I rebuild one real fintech screen a day or two and send it to the founder.
Send your URL if you want yours.
```

Только после правок 6 из `BRAND-diagnosis.md` — иначе шот подписан ником-датой рождения.
Если правки ещё не сделаны, Dribbble сегодня пропускается.

**Behance** — сегодня ничего. Behance — для полного листа, не для одиночной картинки.

---

## Что считать через 48 часов, 22.08 в 12:00

Записать до публикации, одну строку прогноза по каждой (`PLAN-today.md`, тот же приём):

| Метрика | Где смотреть | Прогноз ставишь ты, до публикации |
|---|---|---|
| Показы поста | LinkedIn analytics | |
| Просмотры профиля за 48 ч | LinkedIn analytics | |
| Ответов на CTA «send your URL» | Комментарии + личные сообщения | |
| Просмотры профиля Upwork | Upwork | |

Смысл прогноза не в точности. Смысл в том, что без записанного ожидания
ни один результат — включая ноль — ничему не научит.

**Ноль ответов на CTA при показах выше двухсот** означает не «пост плохой»,
а что широкая публикация не твой канал, и вся ставка недели переносится
на адресные письма. Это тоже результат, и он стоит одного поста.
