---
name: new-project
description: Create a new project folder from the project template. Use when they say "start a new project", "new project", "set up a project for X", "make a folder for X", or when a piece of work clearly needs its own project.
---
# Start a new project

1. **Ask for what is missing, in one go:** the project's name, what it is in one or two sentences, who is involved, and what done looks like. Short dictated answers are fine.
2. **Choose the folder name:** lowercase, hyphens, short, no dates (for example `ava-lin-tour`). Check `projects/` first; if a project already covers this, say so and ask.
3. **Copy** `templates/project/` to `projects/<folder-name>/`, with every subfolder.
4. **Fill in** `projects/<folder-name>/CLAUDE.md`: the name, the paragraph on what it is, who is involved (spellings from `me/names.md`; new names go there, marked unverified), status "starting", today's date. Label origins.
5. **First plan.** If they mentioned a first task or a deadline, create the first plan note in `plans/` from `templates/plan.md`.
6. **Connect it to the week.** If the project belongs in the next seven or thirty days, add one line to `plan.md`.
7. **Save** with Git: "New project: <name>".
8. **Tell them** what was created, and that the folder works on its own when opened directly and shows up in "catch me up" from here.
