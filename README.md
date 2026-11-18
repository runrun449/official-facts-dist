# official-facts-dist

Signed bundles of official-site facts (own-words summaries with source URL and retrieval date).

- `current/manifest.json` — bundle manifest (sequence number, validity period, per-file SHA-256, policy hashes)
- `current/manifest.sig` — Ed25519 signature (hex) over the exact bytes of `manifest.json`
- `current/facts_<BRAND>.json` — facts of one brand (`facts_KIMINI.json`, ...)

The three kinds of files are published together in one commit. A client must verify the signature and the SHA-256 values before using any fact, and must reject a bundle whose files do not match each other.

This repository contains no secrets. Do not rename or transfer this repository: clients do not follow redirects.
