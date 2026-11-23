<p align="center">
  <img src="https://raw.githubusercontent.com/oikos-suite/.github/main/profile/assets/oikos.png" width="96" height="96" alt="Oikos logo" />
</p>

<h1 align="center">Oikos</h1>

<p align="center">
  <i>οἶκος, household.</i> Your phone and your server, run as one home.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/license-EUPL--1.2-blue" alt="License EUPL-1.2"/>
  <img src="https://img.shields.io/badge/made%20in-%F0%9F%87%AB%F0%9F%87%B7%20France-002395" alt="Made in France"/>
  <img src="https://img.shields.io/badge/built%20for-GrapheneOS-f3b9c6" alt="Built for GrapheneOS"/>
  <img src="https://img.shields.io/badge/telemetry-none-5b1027" alt="No telemetry"/>
</p>

<p align="center">
  <a href="https://github.com/pharos-hq">Pharos, the sister suite</a> ·
  <a href="https://github.com/Kolbxyz">Kolb</a>
</p>

---

Oikos is a suite of self-hosted, privacy-first apps for Android, the terminal and your home server. Everything runs on hardware you own. Nothing phones home: no telemetry, no analytics, no Google services.

Every app works on its own. The music apps can also share one home server, Agro.

## Music

| | App | What it does | Runs on |
|:-:|---|---|---|
| <img src="https://raw.githubusercontent.com/oikos-suite/.github/main/profile/assets/agro.png" width="48" alt=""/> | **[Agro](https://github.com/oikos-suite/Agro)** | The home server: library sync, Jam rooms, friends and end-to-end encrypted listen-along | Your server (Rust) |
| <img src="https://raw.githubusercontent.com/oikos-suite/.github/main/profile/assets/wanda.png" width="48" alt=""/> | **[Wanda](https://github.com/oikos-suite/Wanda)** | Music player that merges Subsonic servers, local files, YouTube Music and Deezer into one library | Android |
| <img src="https://raw.githubusercontent.com/oikos-suite/.github/main/profile/assets/wander.png" width="48" alt=""/> | **[Wander](https://github.com/oikos-suite/Wander)** | Music player for the terminal, streaming from Navidrome and Subsonic or playing local files | Terminal (Rust) |
| <img src="https://raw.githubusercontent.com/oikos-suite/.github/main/profile/assets/frwd.png" width="48" alt=""/> | **frwd** | Share links that open a track in Wanda or Wander | Web (not public yet) |

## Phone

| | App | What it does | Runs on |
|:-:|---|---|---|
| <img src="https://raw.githubusercontent.com/oikos-suite/.github/main/profile/assets/mono.png" width="48" alt=""/> | **[Mono](https://github.com/oikos-suite/Mono)** | A quiet launcher: your apps as one list of names, with no network permission at all | Android |
| <img src="https://raw.githubusercontent.com/oikos-suite/.github/main/profile/assets/phalanx.png" width="48" alt=""/> | **[Phalanx](https://github.com/oikos-suite/Phalanx)** | Matrix messaging on the Matrix Rust SDK, end-to-end encrypted, with UnifiedPush | Android |
| <img src="https://raw.githubusercontent.com/oikos-suite/.github/main/profile/assets/kitsune.png" width="48" alt=""/> | **Kitsune** | Self-hosted parental control. Your server, your data, encrypted at rest | Your server + Android (not public yet) |

## Shared rules

- **Self-hosted.** There is no Oikos cloud. Where an app needs a server, you run it.
- **No telemetry.** No analytics, no crash reporting, no third-party fonts or scripts.
- **Battery-first.** Built to stay out of your battery stats.
- **Built for hardened phones.** Designed for GrapheneOS, with no Google services.
- **Open source.** EUPL-1.2 unless a repository says otherwise.

---

<p align="center">
  Made in France · <a href="https://github.com/pharos-hq">See also: Pharos</a>
</p>
