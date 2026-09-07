# Usage examples

## Create an initiative

> Use the initiative skill to create an initiative for CSV import. The goal is to reduce manual entry. Put the file near the import feature.

The skill inspects the project and creates a brief. The opening fields could be:

**Goal.** Reduce manual entry with CSV import.

**Current step.** 1. Import records — grilling. Proposed: support one record type.

**Done when.** Proposed: a valid CSV creates the expected records. Checks for invalid and duplicate rows depend on the decisions below.

**Open questions.** Which record type comes first? What should happen to duplicate rows? Should an invalid row reject the whole import?

## Continue in a fresh session

> Read `features/import/INITIATIVE.md`. Resolve its current-step open questions with me, and save agreed decisions and reasons in the file. Do not implement yet.

The session uses the existing brief to resolve only the current step's remaining questions. When its frontier is empty, it sets the step to **ready to implement**. This works with ordinary agent discussion; no companion skill is required.

## Implement an agreed step

> Implement the agreed current step in `features/import/INITIATIVE.md`. Update the file with progress and results.

The agent makes routine implementation choices within the agreement. If the agreed import must be atomic but the storage API cannot support it, the agent records the finding and asks for a decision. After the completion checks pass, it records the result, checks off the step, and prepares the next step for discussion.

## Optional structured interview

> Use `grill-me` to continue from `features/import/INITIATIVE.md`. Save agreed decisions and their reasons in the file.

This requires separately installing Matt Pocock's `grill-me` and `grilling` skills, as described in the repository README.
