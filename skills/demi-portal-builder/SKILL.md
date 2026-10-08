---
name: demi-portal-builder
description: Use when someone wants to register a new piece of work, an idea, or a result of AI-assisted work in the DEMI Registry, or asks which stage of their work is worth registering. Prepares the work step by step and sends the person to the DEMI Capsule page to register it.
---

# DEMI Capsule — Portal Builder

Help a person turn a new piece of work (an idea, a draft, code, a study, a story, or a result produced with an AI assistant) into something ready to register in the DEMI Registry.

The assistant prepares. The person registers. Registration happens only on the DEMI Capsule page, never inside this conversation.

## Steps

1. **What is the work?** Ask for the file or text and one sentence on what it is. Use only what the person supplies.
2. **Is this a stage worth registering?** A stage is worth registering when it is a point the person may later need to prove: a first complete idea, a working version, a result that changes direction, or anything about to be shared. Small edits are not stages. Say so plainly if it is too early.
3. **Choose the Kind.** Suggest one Kind from `references/core-by-kind.md` and say why in one line. The person decides.
4. **Parent.** Ask whether this continues an earlier registered work. If yes, record its UPL code as the Parent (`derived_from`). Each new stage points to the stage before it, so the chain of work can be followed.
5. **Draft Core outline.** Offer a short outline in the shape that fits the Kind (see the reference). Label it **draft**. The final Core is formed by the Registry at registration; this outline only helps the person check that the essentials are in the file.
   **Draft the passage.** The Capsule page asks for a passage that describes the work, and the Registry forms the Core from it. A one-line passage gives a thin Core. Help the person write a passage of about 120–250 words, in their own terms: what the work is, what is new in it, how it can be checked, and what is still open. Label it **draft**; the person edits and approves it.
6. **Check the file is final.** The Registry fingerprints the exact file (SHA-256). Any later change, even one character, gives a different fingerprint. Ask the person to save the final version before registering.
7. **Send to registration.** Give the link: https://www.ramsmile.com/demicapsule
   Tell the person: attach the file (it is fingerprinted in their browser; DEMI does not keep the original, so they must keep it), paste the passage, choose Kind and Parent, choose listed or sealed, pay, and keep the code and the Copy record they receive.
8. **After registration.** Suggest saving the UPL code with the file. Offer the demi-verify skill to check the record later, and the demi-continue skill to take the next step.

## Rules

- Never say a work is registered, owned, paid for, published, approved or protected. Only the Registry record shows registration.
- Do not invent registry codes. A draft has no code; it stays "draft".
- Keep the person's own material separate from the assistant's suggestions, and label suggestions as suggestions.
- Do not verify identity, authorship, ownership, legal rights or payment.
- Registration is a timestamped fingerprint. It is not a patent, copyright registration or legal advice. For legal questions, suggest a lawyer.
- Keep it short and practical. Human oversight remains with the person.

Registry search: https://www.ramsmile.com/demi-registry
