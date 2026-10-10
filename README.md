# DEMI Capsule

A plugin for Claude (and ChatGPT) that helps you keep a dated record of the stages of your work, especially work done with an AI assistant.

**Register a stage → get its UPL code, certificate and Conceptual Core → continue with an AI assistant → register the next stage with the earlier code as its Parent.**

Maintained by UplitAU Pty Ltd, Sydney, Australia · https://www.ramsmile.com/demicapsule

## What it does

| Skill | Ask, for example | What happens |
|---|---|---|
| `demi-portal-builder` | "I have an idea. Is it worth registering?" | Checks whether this is a stage worth registering, suggests the Kind, records the Parent, helps draft the passage, and gives the link to the DEMI Capsule page. |
| `demi-continue` | "Continue UPL-TECH-26-310441-EN" | Reads the record's AI package (if the assistant can open web pages) or the record text you paste, then proposes and does the next step. |
| `demi-verify` | "Does this file match UPL-…?" | Computes the file's SHA-256, compares all 64 characters with the record, and gives the Ethereum anchor link. |

## What it does not do

- It does **not** register, pay, change records or hold keys. You register on the DEMI Capsule page yourself.
- It contains no server and makes no network calls of its own. If your assistant can open web pages, it may read the public record addresses listed below; otherwise you paste the record.
- A record proves only that a file existed, byte for byte, by a time. It does not establish authorship, ownership or any legal right, and it is not legal advice.

## Public record addresses

- AI package: `https://demi-proxy.flat-bonus-ffc5.workers.dev/registry/<UPL code>/ai`
- Record (JSON): `https://demi-proxy.flat-bonus-ffc5.workers.dev/registry/<UPL code>.json`
- Certificate: `https://demi-proxy.flat-bonus-ffc5.workers.dev/certificate/<UPL code>`
- Registry search: https://www.ramsmile.com/demi-registry

## Worked example

`UPL-TECH-26-310441-EN`: the DEMI Capsule Plugin/MCP Integration Specification v1.0, derived from `UPL-TECH-26-925132-EN`. Try: "Continue UPL-TECH-26-310441-EN".

## Privacy

The plugin itself collects, stores and sends no data. It runs inside your AI assistant, under that assistant's own privacy terms. Files you verify are fingerprinted by the assistant and are not sent to DEMI. Public DEMI records contain no email addresses or owner keys; sealed records show only the code, fingerprint and time. Full privacy notice: https://www.ramsmile.com/demicapsule. Contact: ramsmile@uplitau.com.

## Terms

Terms of Use: https://www.ramsmile.com/demicapsule-terms

## Licence

MIT. See `LICENSE`.
