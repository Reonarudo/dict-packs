# dict-packs

Published dictionary packs for **Vocabolario** — the Italian dictionary app —
and the signed manifest its update channel reads.

This repository is the **public, in-the-clear download location** the data
licence requires: every pack the app ever installs is downloadable from here
without an account, a token, or a client.

## Contents

| Path | What it is |
|---|---|
| [`manifest.json`](manifest.json) | The pack index the app fetches. Schema-versioned; entries are append-only. |
| [`manifest.json.minisig`](manifest.json.minisig) | Detached Ed25519 signature (minisign) over the manifest. |
| [Releases](../../releases) | One release per pack build, tagged with the build's ULID. The pack is the `dict.pack` asset. |
| [`ATTRIBUTION.md`](ATTRIBUTION.md) | Data sources and credits, copied verbatim from the producer. |
| [`LICENSE-DATA`](LICENSE-DATA) | The data licence, copied verbatim from the producer. |

## Licence

The dictionary data — including every `dict.pack` published here — is
released under **CC BY-SA 4.0**. See [`LICENSE-DATA`](LICENSE-DATA) for the
licence and [`ATTRIBUTION.md`](ATTRIBUTION.md) for the sources it is compiled
from, the credits they require, and the modifications made.

If you redistribute a pack, keep `ATTRIBUTION.md` with it.

## Verifying a download

The pack itself is not signed; its SHA-256 lives inside the signed manifest.

```sh
# 1. the manifest is authentic
minisign -Vm manifest.json -P 'RWR4Rfw/2hylt86im2ikMLBnYRLvmnksVi2IohYYpNtyEZfeevvWr9gs'

# 2. the pack matches what the manifest says
shasum -a 256 dict.pack
```

The app pins that public key at build time and rejects a manifest it cannot
verify, so a compromise of this hosting account cannot push a pack to an
install.

## How a pack gets here

Packs are emitted by the producer, which stamps each build with a ULID and
derives its `{buildId, formatVersion, sha256, size}` identity from the
finished file. The manifest entry carries those same four fields plus the
release URL and a timestamp decoded from the ULID — so nothing in this
repository is a second, hand-maintained opinion about which pack is which.
