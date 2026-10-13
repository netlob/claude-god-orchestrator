# Home base starter template: build brief

This brief hands over a design conversation to the Claude Code session that will build the template. Everything here was decided with Sjoerd. Push back on anything you would do differently before you build.

## What we are building

A starter repo that a non-developer opens in Claude Code to get a "home base": one root folder where a top-level orchestrator knows the person and all their work, with every project as a child folder.

The users are a few of Sjoerd's friends at a music company (artist management, creative marketing, film and documentaries). They talk to Claude by voice dictation (Wispr Flow) and want to run their work life through Claude Code, not only build things with it.

- **First user:** one friend, starting this week on his own. He has Opus but not Fable, works on his laptop only, and has no Hermes agent yet. He is not a developer, but he is curious, proactive and wants to learn.
- **Next users:** three more people get the same template in a workshop next week.

## Principles

- **Intent over prompt engineering.** Users share what they want, how much effort to spend, and how to verify it. The template carries the standing intent so their own messages can stay short.
- **Standard skeleton, custom content.** Folder names, templates and routines are identical for everyone. The interview personalizes what goes inside.
- **Keep it thin.** Ship the least structure that is useful and let each person's Claude grow it. Do not pre-build things they may never use.
- **Files are the memory.** Chats are disposable, the folder is permanent. If it matters, it gets written down.
- **Plain language.** No developer vocabulary in anything the user reads: "decisions", not ADRs. No waves, no model picking exposed to the user.
- **Teach as you go.** Claude does the technical work itself, explains what it is doing and why, and pushes back when it sees a better way.
- **Everything in English.**

## What the template contains

1. **Root briefing file (CLAUDE.md), kept short.** The orchestrator role, how to work with the user, a map of where things live, the saving rules, the plan-awareness rules, and first-run behaviour: if there is no profile yet, start onboarding.
2. **The interview.** See the section below.
3. **Project template.** The standard folder every new project is copied from: a project briefing file, sources (originals, never edited), knowledge, meetings, decisions, plans with a status, and work (the output). A project must work as its own orchestrator when opened directly.
4. **Root folders.** A part about the person (profile, goals, people, a names list with correct spellings), an inbox, a projects folder, root-level decisions, and the 7/30/90 plan.
5. **Routines the user triggers by saying so.** Catch me up, wrap up, process my inbox, start a new project, save my thinking. Use whatever Claude Code's current best mechanism is for these.
6. **Note templates.** Meeting note, decision, thinking note, knowledge note.
7. **A start-here note for the human.** Three steps and the short kickoff message.
8. **Git basics.** A sensible ignore file. The user's Claude runs git for them.

## The interview

- **Short.** Only the questions Claude most needs answered to design the setup, few enough for one sitting. Aim for about eight to ten.
- **Open questions.** The user turns on speech-to-text and talks freely on each one, so answers will be long and messy. That is the point.
- **Format.** A very basic one-page HTML file: no server, no dependencies, big text boxes, progress saved in the browser, and one button that copies or downloads all answers as Markdown. Include a plain Markdown version as a fallback.
- **Must include:** which Claude plan they are on.
- **Candidate themes, to pick from and merge, not to cover one by one:** role and a normal week; current projects; the next 90 days; what they make and for whom; tools and where their information lives; the people they work with; how they think and decide; what they want to learn; how they use AI today and what frustrates them; anything sensitive or off limits; what would make this a clear win in a month.
- **Tested** before it ships: answers survive a refresh, and the export works offline.

## Onboarding flow (what the user's Claude does on first run)

1. Point the user to the interview and explain how to get the answers back.
2. Save the raw answers untouched as a source.
3. Ask follow-up questions in the chat.
4. Propose the personalized setup and a 7/30/90 plan in plain language, then wait for a go.
5. Build it and give the user a tour.
6. Prove it works by running one real task of theirs from start to finish.

The 7/30/90 plan: seven days is concrete (three real tasks), thirty days is capabilities (for example a pitch-deck workflow), ninety days is direction only. It is reviewed weekly.

## Saving rules (go in the root briefing)

- **Sources and knowledge are separate.** Originals (transcripts, contracts, research, exports, raw dictation) are stored dated and never edited. Knowledge notes are short, one topic per file, written by Claude from the sources.
- **One way in.** Everything enters through the inbox and the same intake routine. Claude reports what it filed and what it changed, and the user confirms.
- **Label the origin.** Every fact is dated and marked as said by the user, taken from a document, or inferred by Claude. Inferences are never written as facts.
- **Ask on conflict.** When new information contradicts old, Claude asks, then marks the old as superseded with a date instead of deleting it.
- **Names list.** One file with the correct spelling of artists, people and companies, because dictation and transcripts mangle them.
- **Contracts are quoted exactly.** The summary points to the clause and the original always wins.
- **Thinking is saved too.** Decisions record what was on the table, what was chosen, why, and what would change their mind. Thinking notes keep doubts and open questions in the user's own words. Wrap-up asks whether anything was decided today that is not written down.
- **Weekly tidy.** Claude checks for stale statuses, contradictions and orphaned files, and reports.
- **Limits.** No passwords or keys in files. Large media stays outside the repo with a link. For other people's contracts and personal details, ask the user what belongs in the repo.
- **Ask before deleting, sending or publishing anything.**

## Plan-awareness (go in the root briefing)

The interview asks for the plan and the briefing records it. Verify current plan terms before writing these in.

- **Pro, or no Fable access:** no Fable (on Pro it bills as paid usage credits), a cheaper model for routine filing and meeting notes, one task at a time with no parallel subagents, big builds split across sessions, and a warning before anything large.
- **Max:** Fable is available for planning, within its share of the weekly limit.
- The main session's model is whatever is selected in the app, so the briefing can only steer subagents and scope.

## Design for later, do not build now

- **Hermes on Telegram.** Claude Code stays the only writer to the knowledge base. A Hermes agent would read the repo and write only to the inbox. The repo wins on business facts, and Hermes names the file it answered from. Enforcement later through a read-only key and a separate inbox repo or branch.
- **People with an existing Hermes.** The old one keeps running untouched and they get a fresh one. The old agent's export is stored as a dated, unverified source: leads only, promoted to knowledge on the user's confirmation, flagged when relied on. Migration is a project with a checklist and an end date.
- **Phone access.** Git from day one, a private GitHub repo later, then cloud sessions from the Claude app. Work done there arrives on a branch, and catch me up merges it.
- **Scheduled inbox processing** as a later step.
- **A shared company repo** for artist projects several people touch is an open question.

## Done when

- A fresh copy opened in Claude Code with only the short kickoff message runs the onboarding flow correctly.
- The interview page works offline and exports cleanly.
- "Start a new project" creates a project from the template.
- A sample meeting transcript dropped in the inbox is filed correctly, with origin labels, and Claude reports what it changed.
- A non-developer can follow the start-here note without help.

Test these in a scratch copy before shipping, and test once with Opus selected, since that is what the first user has.

## The user's kickoff message (goes in the start-here note)

> [Talk for a few minutes about who you are, what you do, and what's on your plate.] This is my first session in my new home base. Read the briefing in this folder and start my onboarding. Take your time, show me the plan before you build anything, and prove it works with one real task of mine.

## Appendix: the long-form intent

This is the prompt drafted before we decided on a template. Use it as the source for the root briefing's voice and content.

This is my first ever Claude Code session, and this folder is going to be my home base. I want you to be my top-level orchestrator: the one place I always start, that knows me and everything I'm working on, and that either helps me directly or sets up a dedicated project and runs the work from there. Over time I want to run my whole work life through this, not only build things with it.

About me as a user: I'm not a developer. I know a few things, I'm curious, and I want to learn. So handle the technical work yourself, but tell me in plain language what you're doing and why, and teach me the concepts that matter as we go. I work by sharing my intent, usually by voice dictation, so my messages will be messy and I'll think out loud. Go by what I mean, ask when it's unclear, and don't just do what I say: if you see a better way, tell me and explain why.

How I want it organized. Every project I work on (an artist, a campaign, a venture, an idea) lives as a child folder inside this one. All projects follow the same structure, built from one project template, so a new project is always set up the same way. Each project has its own briefing, knowledge, meeting notes, decisions with the reasoning, plans, status and output, and works as its own orchestrator when I open it directly. You, at the top level, keep the overview of all projects and where each one stands. Follow Claude Code best practices for how all of this is set up, and explain your choices to me.

Take your time and think it through properly; I'd rather this is right than fast. Start with the least structure that's useful and let it grow as we use it.
