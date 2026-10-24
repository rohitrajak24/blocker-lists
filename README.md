# blocker-lists

Signed, compiled block lists for a personal website blocker (gambling and adult sites).
Each [release](../../releases) holds one list. Devices always fetch the newest one from:

```
https://github.com/rohitrajak24/blocker-lists/releases/latest/download/latest.json
https://github.com/rohitrajak24/blocker-lists/releases/latest/download/blocklist.bin.gz
https://github.com/rohitrajak24/blocker-lists/releases/latest/download/blocklist.bin.sig
```

## Verify a list yourself

```bash
openssl dgst -sha256 -verify lists-public-key.pem -signature blocklist.bin.sig blocklist.bin
```

`lists-public-key.pem` is in this repo. The format is documented in the project's
`spec/list-format.md`.

## What's inside

Generic data only: public third-party lists plus generic keywords, keyword exceptions, a small
allowlist of problem-gambling help sites, and SafeSearch mappings. No personal data.

## Sources and licenses

See [NOTICE.md](NOTICE.md). The compiled lists contain data from GPL-3.0 sources, so they are
distributed under the GPL-3.0 ([LICENSE](LICENSE)).
