---
description: "Daily 5-minute energy-mood-focus journal. Creates structured daily logs in notes/ folder. Run this every day to build your personal data foundation for Week 2's Knowledge OS."
allowed-tools:
  - AskUserQuestion
  - Write
  - Read
  - Bash
---

# /daily-log — Daily Journal

Run a quick 5-minute daily check-in. Ask 6 questions, save a structured note.

## Interview Flow

Ask each question one at a time using `AskUserQuestion`. Keep it brisk and friendly.

### Question 1: Energy
- **Question:** "How's your energy today?"
- **Options:** `["1-3 (Low)", "4-5 (Below average)", "6-7 (Good)", "8-10 (Great)"]`
- Map the answer to a number: Low=2, Below average=5, Good=7, Great=9

### Question 2: Focus
- **Question:** "How well could you concentrate today?"
- **Options:** `["1-3 (Low)", "4-5 (Below average)", "6-7 (Good)", "8-10 (Great)"]`
- Map the answer to a number: Low=2, Below average=5, Good=7, Great=9

### Question 3: Mood
- **Question:** "Overall mood?"
- **Options:** `["1-3 (Low)", "4-5 (Below average)", "6-7 (Good)", "8-10 (Great)"]`
- Map the answer to a number: Low=2, Below average=5, Good=7, Great=9

### Question 4: Highlight
- **Question:** "What was the highlight of your day?"
- **Options:** `["Got something important done", "Had a great conversation", "Learned something new", "Other"]`
- Accept whatever they type — the options are just prompts.

### Question 5: Blocker
- **Question:** "What slowed you down or frustrated you?"
- **Options:** `["Too many meetings", "Couldn't focus", "Stuck on a problem", "Nothing major", "Other"]`
- Accept whatever they type.

### Question 6: Tomorrow
- **Question:** "What's the one thing you want to accomplish tomorrow?"
- **Options:** `["Finish a key task", "Start something new", "Clear my backlog", "Other"]`
- Accept whatever they type.

## Save the Log

1. Get today's date in YYYY-MM-DD format (run `date +%Y-%m-%d` via Bash).
2. Create the `notes/` directory in the current working directory if it does not exist.
3. Write the file to `notes/daily-log-YYYY-MM-DD.md` with this format:

```markdown
# Daily Log — YYYY-MM-DD

## Vitals
- Energy: X/10
- Focus: X/10
- Mood: X/10

## Highlight
[their answer]

## Blocker
[their answer]

## Tomorrow
[their answer]

---
*Logged via /daily-log*
```

## After Saving

Print a one-line confirmation:

> Logged! Energy X, Focus X, Mood X. See you tomorrow.

If an `achievements.md` file exists in the current directory, update it:
- Count `notes/daily-log-*.md` files to update streak and check achievement unlocks (First Log, Consistency, Week Warrior, Fortnight Force).
- Add an entry to the Activity Log table.

Do NOT turn this into a long conversation. The whole interaction should take under 5 minutes.
