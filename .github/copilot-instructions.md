# Copilot instructions for Waywework

## What this repository is

Waywework is a personal work handbook written entirely in Markdown. There is no
application code, no package manager, and no test suite. The unit of work is a
document, and the quality bar is whether a reader can act on the guidance.

The handbook is written by one person about how he prefers to work. Some
documents are stated as personal preference and some are stated as team policy;
this tension is real and unresolved (see "Known inconsistencies" below). Do not
resolve it silently in a drive-by edit.

## Repository map

| Path | Role |
| --- | --- |
| `README.md` | Entry point: framing, the `Handbook` link list, and the contribution rules |
| `docs/*.md` | One topic per file; the handbook content |
| `templates/rule.md` | The prescribed format for a substantive rule |
| `.codacy/` | Codacy CLI configuration |

`README.md` is an index, not a summary. **Adding a file to `docs/` requires
adding a link to the `Handbook` list in `README.md`**, or the document is
unreachable.

## Commands

There is no build, test, or lint step for content. Codacy is the only configured
tooling:

- `.codacy/codacy.yaml` pins `java@17.0.10`, `opengrep@1.16.4`, `pmd@7.11.0`
- `.codacy/cli-config.yaml` sets `mode: local`

After editing any file, run Codacy analysis scoped to that single file, passing
the workspace root as `rootPath` and the edited file as `file`, leaving the tool
unset. Analyze one file at a time rather than the whole repository; there is no
"full suite" to run. If the Codacy CLI is not installed, ask before installing.

There is no CI workflow and no Markdown linter, so wrapping, heading case, and
link correctness are not checked automatically. Verify them by reading.

## Writing conventions

These are consistent across `docs/` and are not visible from any single file:

- **Hard-wrap prose at roughly 80 characters.** Every document follows this
  except `docs/meetings.md`.
- One `#` H1 title per file, `##` for sections, no deeper nesting.
- **Title Case** for `##` headings. `docs/security-over-competition.md` uses
  sentence case instead; match the file you are already in unless you are
  deliberately normalizing.
- Direct, observable, imperative guidance. Bare `Do not ...` sentences are
  normal and preferred over hedged phrasing.
- Bulleted lists use semicolons with a trailing `; and` before the final item
  when the list is a single grammatical sentence.
- Several documents close with a practical section rather than a conclusion:
  `Review Questions`, `Useful Boundary Language`, or a worked example. Prefer
  this over a summary paragraph.
- Cross-document links are relative and live inside `docs/`, for example
  `[Working with Restraint](working-with-restraint.md)`.

## The house structure for technical messages

`docs/communication.md` defines the repository's signature construct for writing
about work that is still being understood:

**Known** (evidence-backed facts) / **Unknown** (open questions) / **Not needed**
(work the evidence does not justify) / **Next** (smallest resolving action).

Reuse this framing when drafting examples or new guidance about uncertainty. It
is explicitly not a mandatory template for every message.

## Contribution rules

`README.md` states five rules. Treat them as binding when authoring content:

1. Start from something actually observed, not a hypothetical.
2. Use `templates/rule.md` for anything substantive.
3. Say why the guidance exists, not just what to do.
4. Keep changes small enough to stand on their own.
5. Update or remove a document once it stops matching how the work actually
   happens.

Rule 1 is the one most often violated. **Do not add generic handbook prose that
could appear in any company's wiki.** If a proposed paragraph is not traceable
to a specific observed situation, it does not belong here.

## Voice

Preserve the author's first person. `docs/meetings.md` is written as `I`/`my`
and carries personal experience; rewriting it into impersonal policy language
destroys its point. The other documents in `docs/` use an impersonal handbook
register, which is the source of the personal-versus-policy tension noted above.

## Known inconsistencies

Existing state that should not be treated as the pattern to copy:

- `docs/meetings.md` has no `#` H1, is not hard-wrapped, uses sentence-case
  headings, and is unedited relative to the other documents.
- `templates/rule.md` is referenced by `README.md` but used by no document.
- No document carries status, owner, or last-reviewed metadata, although
  `templates/rule.md` requires all three.
- No document links to any other document, so related guidance in a sibling
  file is not discoverable by navigation.
- Content overlaps across files: urgency appears in both `docs/meetings.md` and
  `docs/communication.md`; boundaries appear in both `docs/meetings.md` and
  `docs/work-boundaries.md`.
- The chronology described in `README.md` (meetings, then security, then
  boundaries, then restraint) does not match the order of the `Handbook` list.

## Commits

Single-line, capitalized, no conventional-commit type or scope, no body. Actual
examples: `Meetings`, `Update readme`, `How to resolve unknowns`,
`Security over competition doc`. `main` is the only branch and commits land
directly on it.
