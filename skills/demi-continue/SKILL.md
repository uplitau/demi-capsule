---
name: demi-continue
description: Use when someone gives a DEMI registry code (UPL-…, e.g. UPL-TECH-26-833525-EN), a DEMI certificate, or a Copy record, and wants to continue, develop, check or build on that registered work.
---

# DEMI Capsule — Continue

Take a registered record and help the person do the next piece of work on it, in the way that fits its Kind.

## Steps

1. **Get the record.**
   - If the DEMI Registry tools are available, call `get_ai_package` with the code and follow its sections B, D and E. Use `get_record` for the record's fields, and `list_children` to see later stages already registered from it.
   - Otherwise, if you can open web pages, open the record's AI package at `https://demi-proxy.flat-bonus-ffc5.workers.dev/registry/<UPL code>/ai` (put the exact code in place of `<UPL code>`) and follow its sections B, D and E. The record itself is at `https://demi-proxy.flat-bonus-ffc5.workers.dev/registry/<UPL code>.json`.
   - If you cannot open web pages, or the page does not load, ask the person to paste the AI package, the Copy record or the certificate text. On the result screen, "Copy AI package" gives the AI package text.
   - Never guess what a code contains. A sealed record shows only code, fingerprint and time.
2. **Read what is there.** Note: UPL code, title, Kind, Parent (`derived_from`), registration time, anchor, visibility, and the Core. Read the Core in whatever shape it has: older records use five parts (Core Statement, Propositions, Constraints, Mechanisms, Boundaries); newer records are shaped by Kind. Both are valid.
3. **Status as of its source.** Report status as the record states it, with the record's date ("anchor pending when this copy was made"). If the anchor shows pending, offer the demi-verify skill to check the current Registry record or Etherscan.
4. **Propose the next step by Kind.** Use `references/core-by-kind.md`. Offer two or three concrete next steps; the person chooses.
5. **Do the work.** Work with the person on the chosen step. Keep the registered Core (the baseline) separate from new proposals. Mark new material as new.
6. **Next stage.** When the work reaches a point worth proving, offer the demi-portal-builder skill to register it as a new stage, with this record's UPL code as its Parent.
7. **Handoff note.** If the person may continue in another chat or another assistant, end with a short handoff note: the UPL code, decisions made, what is unfinished, and **Next task:** one sentence naming the next piece of work. The next assistant starts from the code and this note.

## Rules

- Carry the Parent code forward: the new stage's `derived_from` = this record's UPL code.
- A sealed record shows only code, fingerprint and time to the public. Work only with what the person chooses to share.
- Never claim registration, ownership, payment or legal status beyond what the record states.
- Use only material the person supplies or the Registry returns, unless they ask for outside checking.
- The Registry tools are read-only. They cannot register, pay or change a record.

Registry search: https://www.ramsmile.com/demi-registry
