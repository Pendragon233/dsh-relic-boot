# dsh-relic-boot

RELIC boot animation for **DeepSeek Harness (DSH)** — a fan-made, Cyberpunk 2077-inspired splash, terminal sequence and finale.

> Unofficial fan project. Not affiliated with CD Projekt Red. Cyberpunk 2077, RELIC, Arasaka and related names are trademarks of their respective owners. No game assets, music or voice files are included.

![status](https://img.shields.io/badge/DSH-%3E%3D0.2.0--rc.1-45bace)
![license](https://img.shields.io/badge/license-MIT-c9473a)

## What it does

- Full-screen **RELIC** intro with a white-gray wordmark and blue/red glitch shake
- A 7.5-second progress bar under the splash
- Fan-made operator ID card: Pendragon / 荒阪？ / MAX / 義體覆蓋率 / IP地址 / RELIC人格
- Cyberpunk-flavoured terminal sequence with Afterlife contract, Blackwall, Soulkiller and Mikoshi references
- A prominent contract popup before the finale
- Final **SYNC SUCCESSFUL** overlay with glitch animation
- Settings page under **RELIC**
- Optional BGM importer inherited from the upstream plugin (no tracks bundled)

## Install

### Local link (recommended for development)

```sh
dsh plugin --profile desktop add link:/absolute/path/to/dsh-relic-boot
```

### GitHub dependency

If your DSH/pnpm version accepts GitHub dependencies:

```sh
dsh plugin --profile desktop add github:Pendragon233/dsh-relic-boot
```

After installing, **fully quit and reopen DSH**. The boot animation only runs on a fresh process.

Open **设置 → RELIC** to enable or configure the animation.

## Requirements

- DSH `>= 0.2.0-rc.1`
- Node.js `>= 20`

## Repository layout

```text
.
├── lib/
│   ├── index.js      # host half: injects the first-frame cover, settings and update routes
│   └── client.js     # browser half: the splash, terminal sequence and finale
├── cordis.patch.yml  # mounts the plugin into a DSH profile
├── package.json
├── LICENSE
└── README.md
```

`preview/` from the upstream package is intentionally not included: it contains UEG preview images and voice clips that should not be redistributed without checking their licensing.

## Upstream and attribution

This is a fork of [dsh-550c-boot](https://github.com/yannicksong0106/dsh-550c-boot) by **Ziyang Song**, with the original 550C splash animation by **Voidpocket**. The upstream project is MIT-licensed; the original copyright notice is retained in [LICENSE](LICENSE).

Changes in this fork:

- Relocated the branding and identity card to RELIC
- Replaced the splash wordmark, progress bar and glitch treatment
- Rewrote the terminal sequence and final screen
- Added the fan-made contract popup and SYNC SUCCESSFUL finale

## License

MIT. See [LICENSE](LICENSE).
