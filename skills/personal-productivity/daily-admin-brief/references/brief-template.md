# Brief Template

The output page skeleton for Step 8, in both languages. Sections appear in this order; a section with no content is dropped and replaced by a single line saying so.

---

## English

```markdown
# Daily Admin Brief — {weekday, date}
Streams found: {calendar, inbox, todos}. **{missing stream} not provided** — {consequence}.
{one line stating the target-day assumption, only if the input spanned several days}

## Top Actions
1. **{action}** — {why it has to be today}. *(from: {stream} — {source})*
2. **{action}** — {why}. *(from: {stream} — {source})*
3. **{action}** — {why}. *(from: {stream} — {source})*

## Schedule Risk
- **{HH:MM–HH:MM} overlaps {HH:MM–HH:MM}** — "{event A}" and "{event B}". One has to move.
- **{HH:MM} → {HH:MM} → {HH:MM} back-to-back**, no gap before {event}.
- **{HH:MM} "{event}"** — duration not stated; adjacency with {event} unverified.
- **Prep the {HH:MM} {event}** — no prep block on the calendar.

## Draft Replies — copy manually, nothing is sent
**→ {sender}, "{subject}"**
> {2–4 lines, register matched to the original, […] where a fact is missing}

**→ {sender}, "{subject}"**
> {2–4 lines}

## FYI
- {item} — no action today. *(from: {source})*

## Needs Your Call
- {ambiguity phrased as a question the user answers, not one the skill guesses at}

## Dates to Capture — not on the pasted calendar
- **{date}** — {commitment}. *(from: {source}, "{quoted fragment}")*
```

**Empty-section lines:**
- `No schedule conflicts found in the pasted calendar.`
- `No inbox items needed a short reply.`
- `Nothing filed as FYI.`
- `No ambiguities — everything mapped cleanly.`
- `No uncaptured dates found.`

---

## Russian

```markdown
# Бриф на день — {день недели, дата}
Найдено: {календарь, почта, задачи}. **{отсутствующий поток} не предоставлен** — {следствие}.
{одна строка о том, какой день взят за целевой, только если материал охватывал несколько дней}

## Главное на сегодня
1. **{действие}** — {почему именно сегодня}. *(источник: {поток} — {ссылка})*
2. **{действие}** — {почему}. *(источник: {поток} — {ссылка})*
3. **{действие}** — {почему}. *(источник: {поток} — {ссылка})*

## Риски расписания
- **{ЧЧ:ММ–ЧЧ:ММ} пересекается с {ЧЧ:ММ–ЧЧ:ММ}** — «{встреча A}» и «{встреча B}». Одну нужно двигать.
- **{ЧЧ:ММ} → {ЧЧ:ММ} → {ЧЧ:ММ} подряд**, без перерыва перед {встреча}.
- **{ЧЧ:ММ} «{встреча}»** — длительность не указана; смежность с {встреча} не подтверждена.
- **Подготовиться к {ЧЧ:ММ} {встреча}** — блока подготовки в календаре нет.

## Черновики ответов — копировать вручную, ничего не отправляется
**→ {отправитель}, «{тема}»**
> {2–4 строки, регистр по оригиналу, […] там, где не хватает факта}

**→ {отправитель}, «{тема}»**
> {2–4 строки}

## К сведению
- {пункт} — сегодня действий не требует. *(источник: {ссылка})*

## Требует вашего решения
- {неоднозначность, сформулированная вопросом, а не догадкой}

## Даты, которых нет в календаре
- **{дата}** — {обязательство}. *(источник: {ссылка}, «{цитата}»)*
```

**Строки для пустых разделов:**
- `Конфликтов в расписании не найдено.`
- `Ни одно письмо не требует короткого ответа.`
- `В раздел «К сведению» ничего не попало.`
- `Неоднозначностей нет — всё разложилось однозначно.`
- `Незахваченных дат не найдено.`

---

## Rules that hold in both languages

- Every item in Top Actions, FYI, and Dates to Capture carries a source reference. No exceptions.
- Quoted fragments keep the original language even when the surrounding brief is translated.
- Each reply stub is written in the language of the message it answers, which may differ from the brief's language.
- The Draft Replies heading always carries the "copy manually, nothing is sent" clause.
- Never pad a section to look complete. Drop it and state that it is empty.
