---
name: process-inbox
description: File everything waiting in the inbox folder into the right places with origin labels, and report what changed. Use when they say "process my inbox", "file this", "I dropped something in the inbox", "there's a new transcript", "I put a contract in there", or when new files have appeared in inbox/.
---
# Process my inbox

The inbox is the one way in. Everything in `inbox/` is filed the same way, one item at a time, oldest first. Nothing is final until the person has seen the report. Skip `README.md`. If the inbox is empty, say so in one line.

For each item:

1. **Identify it.** A meeting transcript, a contract, research, the person's own dictation, an export, interview answers, a link, a note to self? Which project does it belong to, or is it about the person (`me/`)? When unclear, ask before filing. Interview answers are handled by the onboarding in `CLAUDE.md`.
2. **File the original.** Move it unchanged to the right `sources/` folder (`projects/<name>/sources/` or `me/sources/`), renamed `YYYY-MM-DD-what-it-is` with its original extension. The date is when it was created or recorded if that is known, otherwise today. Never edit a source. Large media (audio, video, big files) stays outside the folder: write a short note with its location instead.
3. **Check names.** Compare every person, artist and company against `me/names.md`. Use the correct spelling in everything you write, never in the source. Add new names to `me/names.md` marked unverified, with the misheard form in "Often heard as".
4. **Write the derived notes**, each from its template in `templates/`:
   - Meeting transcript → one meeting note in `meetings/`. Decisions that matter beyond the meeting also get their own note in `decisions/`.
   - Contract or agreement → a knowledge note that quotes the key clauses exactly and points to the source. The original always wins; say so in the note. Ask before filing other people's contracts or personal details.
   - Research, articles, exports → knowledge notes, one topic per file, short.
   - The person's own dictation or notes → a thinking note, or updates to the `me/` files.
5. **Label every fact** with origin and date: `— user, DATE` (they said it), `— from sources/FILE, DATE` (a document), `— inferred, DATE` (your conclusion). Never write an inference as a fact.
6. **Look for conflicts.** Does anything contradict existing knowledge, a status or a decision? Do not overwrite. Ask which is right, then mark the old as superseded with the date and a pointer to the new.
7. **Update status.** If the item changes where a project stands, update "Where it stands" in that project's `CLAUDE.md`. If it affects the 7/30/90 plan, say so.

Then, for the whole inbox:

8. **Report** in plain language: what each item was, where the original went, which notes were created or changed, names added, conflicts found, open questions. Wait for confirmation.
9. **Save** with Git once confirmed, with a message such as "Inbox: filed the call with Ava Lin's manager, updated the tour knowledge".
