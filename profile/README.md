<div align="center">

# AgroUPlus

**High-performance, self-hosted audio streaming & synchronization ecosystem.**

[![Rust](https://img.shields.io/badge/Language-Rust_2024-orange.svg?style=flat-square&logo=rust)](https://www.rust-lang.org/)
[![Kotlin](https://img.shields.io/badge/Language-Kotlin-7F52FF.svg?style=flat-square&logo=kotlin&logoColor=white)](https://kotlinlang.org/)
[![Android](https://img.shields.io/badge/Platform-Android_8.0+-3DDC84.svg?style=flat-square&logo=android&logoColor=white)](https://developer.android.com)
[![TUI: Ratatui](https://img.shields.io/badge/TUI-Ratatui-purple.svg?style=flat-square)](https://ratatui.rs/)
[![API: Subsonic](https://img.shields.io/badge/API-Subsonic%20%2F%20Navidrome-green.svg?style=flat-square)](https://www.navidrome.org/)
[![License: MIT / AGPL](https://img.shields.io/badge/License-MIT%20%2F%20AGPL--3.0-blue.svg?style=flat-square)](https://opensource.org/)

</div>

---

### 📦 Ecosystem Repositories

| Project | Description | Stack |
| :--- | :--- | :--- |
| [**`Wander`**](https://github.com/AgroUPlus/Wander) | **Terminal Music Player (TUI)**<br>Fast keyboard- and mouse-driven desktop music player. Unifies local audio files (MP3/FLAC/Opus) and remote Navidrome/Subsonic servers into a single gapless queue with live visualizers and synced lyrics. | `Rust`, `Ratatui`, `cpal`, `symphonia` |
| [**`Wanda`**](https://github.com/AgroUPlus/Wanda) | **Android Mobile Music Player**<br>Native Android client built with Material 3 Expressive. Unifies Navidrome, local files, YouTube Music, and Internet Archive into a single battery-optimized player with zero trackers, audio offload, and canvas visualizers. | `Kotlin`, `Jetpack Compose`, `Media3`, `Room`, `Hilt` |
| [**`Agro`**](https://github.com/AgroUPlus/Agro) | **Sync Daemon & Social Server**<br>Lightweight self-hosted daemon powering real-time cross-device session handoff (between Wander and Wanda), listen-along, private friend feeds, and custom-domain share link resolution. | `Rust`, `GraphQL`, `WebSocket`, `SQLite`, `React` |

---

### 🏛️ Architecture Overview

```text
 ┌──────────────────────────────────────────────────────────────┐
 │                    Music Backends & Sources                  │
 │      (Navidrome / Subsonic · Local Storage · YT Music · IA)  │
 └──────────────────────────────┬───────────────────────────────┘
                                │
                      ┌─────────┴─────────┐
                      │    Agro Daemon    │ (Live Push & State Handoff)
                      │  (Sync & Social)  │
                      └────┬───────────┬──┘
                           │           │
             ┌─────────────┘           └─────────────┐
             ▼                                       ▼
    ┌─────────────────┐                     ┌─────────────────┐
    │  Wander (TUI)   │                     │  Wanda (Mobile) │
    │  Desktop Client │ ◄── Session Sync ──►│  Android Client │
    │  (Linux/macOS)  │     Listen-Along    │    (Android)    │
    └─────────────────┘                     └─────────────────┘
```

---

### ✨ Core Pillars

- ⚡ **Zero-Latency Audio & Offload**: Decoupled lock-free audio engine on desktop (`cpal`/`symphonia`) and native DSP hardware audio offload on Android (`Media3`).
- 🔄 **Unified Unified Queues**: Mix and match local files, Subsonic/Navidrome servers, YouTube Music, and Internet Archive seamlessly.
- 📲 **Seamless Cross-Device Handoff**: Start playing in your terminal with `Wander`, pick up exactly where you left off on `Wanda` mobile via `Agro`.
- 🔒 **Privacy by Default**: Strict opt-in social boundaries, zero trackers/analytics, Keystore-backed secrets (AES-256-GCM), and no telemetry.
- 🪶 **Self-Contained & Minimal**: Single-binary Rust daemons with embedded React dashboards, SQLite storage, and zero external database dependencies.
