# Skills

Personal agent skills by [Iurii Cherkashin](https://github.com/4erkashin). The first release is **Initiative**: a small, durable Markdown brief for one meaningful change that takes more than one AI session.

> Too much work for one chat. Still small enough to keep in one file.

## Initiative

Initiative turns a goal or rough plan into an `INITIATIVE.md` that retains the goal, current step, completion checks, open questions, decisions, and results. It creates the draft and stops. The brief, rather than a workflow controller, is what lets a later session continue knowing what was agreed, why, and what to do next.

### Install

Install it with the Skills CLI:

```sh
npx skills@latest add 4erkashin/skills --skill initiative
```

The CLI installs the skill into the agent environment it supports. If your agent uses a different skill location, copy the `[skills/initiative](skills/initiative)` directory there.

### Use

Ask your agent to create a brief, for example:

```text
Use the initiative skill to create an initiative for CSV import. The goal is to reduce manual entry. Put the file near the import feature.
```

Initiative inspects relevant project context, writes a draft, and stops. In any later session, continue from the file in ordinary language:

```text
Read features/import/INITIATIVE.md. Resolve the open questions for its current step, save the decisions and reasons in the file, and do not implement yet.
```

When the current step is agreed, ask the agent to implement it and update the brief with the result. Existing initiative files are preserved unless you explicitly ask to update or replace one.

### Recommended Matt Pocock-based workflow (optional)

For a structured interview, install [Matt Pocock's skills](https://www.aihero.dev/skills).

Initiative grew out of constantly working with those skills. I found the combination convenient, and a durable brief made it easier to continue across sessions. A typical loop is **initiative** (write or refresh the brief) → **grill-me** plus **research** when a step still needs clarity → **implement** the step once that clarity is in the file.

## Credits and notices

Initiative is original work by Iurii Cherkashin and is released under the [MIT License](LICENSE). Its optional interview workflow was inspired by [Matt Pocock's skills](https://www.aihero.dev/skills). Those skills are not copied into this repository and remain separately installed; see their upstream repository and [MIT license](https://github.com/mattpocock/skills/blob/main/LICENSE) for their terms and notices.

The skill directory follows the [Agent Skills specification](https://agentskills.io/specification).
