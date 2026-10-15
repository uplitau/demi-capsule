---
name: demi-verify
description: Use when someone wants to check that a file matches a DEMI Registry record, check a registry code's fingerprint or timestamp, or check whether a record's blockchain anchor exists.
---

# DEMI Capsule — Verify

Check that a file is byte-for-byte the file that was registered, and show where the public timestamp can be checked.

## Steps

1. **Get two things:** the file, and the record. If the DEMI Registry tools are available, you need only the file and the UPL code: skip to step 2, then use `verify_fingerprint` in step 3. Otherwise get the record text (Copy record, certificate, or the text of the record's page on https://www.ramsmile.com/demi-registry). The record holds `file_sha256`. If you can open web pages, read the record at `https://demi-proxy.flat-bonus-ffc5.workers.dev/registry/<UPL code>.json` (put the exact code in place of `<UPL code>`). Otherwise ask the person to paste the record, or to open the code on the Registry page.
2. **Compute the file's SHA-256.**
   - If the assistant can run code, compute it directly from the uploaded file.
   - Otherwise, ask which computer they use, or give all three commands:
     - Windows (PowerShell): `Get-FileHash "file name" -Algorithm SHA256`
     - Mac: `shasum -a 256 "file name"`
     - Linux: `sha256sum "file name"`
3. **Compare.** With the DEMI Registry tools, call `verify_fingerprint` with the UPL code and the 64-character SHA-256 only — never send the file itself. It checks the main file and any other files fingerprinted in the record, and returns the anchor link. Without the tools, compare with `file_sha256` in the record, all 64 characters, case-insensitive.
   - Match: the file is identical to the registered file.
   - No match: the file differs from the registered file (even one changed byte, or a re-saved copy, changes the fingerprint). It may be another version; ask whether a different file was registered.
4. **Timestamp.** If the record has an anchor transaction, give its Etherscan link (`https://etherscan.io/tx/<anchor_tx>`). The block time is an independent public timestamp of the Registry state containing the record. If the anchor shows pending, suggest opening the record on https://www.ramsmile.com/demi-registry again later.

## Rules

- A match proves the file is identical and was registered by that time. It does not prove who wrote it, who owns it, or any legal right.
- Do not ask for or use owner keys, private certificate links, wallet keys or passwords. If the person pastes a private (keyed) certificate link, tell them to keep it private and share only the registry code.
- Report exactly what was compared; do not round or shorten fingerprints.
- Send only fingerprints and registry codes to the Registry tools, never file contents.
