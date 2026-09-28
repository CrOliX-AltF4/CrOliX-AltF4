<div align="center">

<img width="1410" height="324" alt="image" src="https://github.com/user-attachments/assets/73da84b6-8f0c-44b2-99b8-6cbb5ec4b2ad" />

<br/>

[![Typing SVG](https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=13&duration=3500&pause=1000&color=FFFFFF&center=true&vCenter=true&multiline=true&repeat=true&width=640&height=60&lines=%3E+Memory+Core+Detected.+%5BInitializing+dev+environment...%5D;%3E+Natsume+online.+Waiting+for+CrOliX%27s+input...;%3E+ERROR%3A+no+stopping+condition+found.+continuing+build...;%3E+Praise+the+sun%2C+ship+the+code.)](https://git.io/typing-svg)

[![Website](https://img.shields.io/badge/website-crolix--website-C8A415?style=flat-square)](https://crolix-website.vercel.app)
[![Ecosystem](https://img.shields.io/badge/ecosystem-Lun'-555555?style=flat-square)](#-the-lun-ecosystem)

</div>

---

## ⟁ about

```typescript
const crolix = {
  alias    : "CrOliX-AltF4",
  location : "your WI-FI",
  focus    : ["Full-Stack Dev", "AI Integration", "Cognitive Systems"],
  currently: "Building a personal assistant",
  motto    : "Don't trust any lalafell" // - "a good friend"
} satisfies Developer;
```

Full-stack developer by training. On the side, I build **Lun'**: a set of standalone projects orbiting one
entity, **Natsume Tsurugi**, a personal assistant with a character that runs 24/7 on my home server.

---

## ◈ the lun' ecosystem

<div align="center">

```
  ┌─────────────────────────────────────────────────────────────┐
  │  "Born from scattered  memories.                            │
  │   Awakened to unite them."                                  │
  │                                         — Natsume Tsurugi   │
  └─────────────────────────────────────────────────────────────┘
```

</div>

```mermaid
flowchart LR
    subgraph natsume["Natsume · private"]
        direction TB
        CORE["◆ Natsume Core<br/>persona · memory · voice<br/><i>NAS, 24/7</i>"]
        DESK["Desktop Agent<br/>mic · screen · avatar<br/><i>PC</i>"]
        DESK <--> CORE
    end

    subgraph acedia["Acedia · standalone product"]
        direction TB
        AV["LunAvaritia<br/>Android client"]
        AC["LunAcedia<br/>inbox · agent · actions"]
        AV --> AC
    end

    SRC[("Gmail · Calendar · Tasks<br/>GitHub · RSS · Home Assistant")]

    CORE -- "delegates" --> AC
    AC <--> SRC

    subgraph tools["Standalone tools"]
        direction TB
        IRA["LunIra<br/>intent → code"]
        GULA["LunGula<br/>replays → ONNX"]
    end
```

| Project | What it is | Stack | Status |
|---|---|---|---|
| **LunAnima** · _private_ | Natsume's Core: persona, memory, emotion and voice. Links the satellites together | TypeScript · Node · Vue | ![active](https://img.shields.io/badge/-active-4c7a4c?style=flat-square) |
| [`LunAcedia`](https://github.com/CrOliX-AltF4/LunAcedia) | Information server: connectors, an inbox synced with its sources, an agent bound by autonomy tiers | TypeScript · Node · Docker | ![in dev](https://img.shields.io/badge/-in_development-555555?style=flat-square) |
| [`LunAvaritia`](https://github.com/CrOliX-AltF4/LunAvaritia) | Android client for LunAcedia: feed, chat, push notifications | Flutter · Dart · FCM | ![in dev](https://img.shields.io/badge/-in_development-555555?style=flat-square) |
| [`LunIra`](https://github.com/CrOliX-AltF4/LunIra) | Multi-agent dev pipeline CLI: PO → Planner → Dev → QA | TypeScript · CLI | ![npm](https://img.shields.io/npm/v/@crolix-altf4/lunira?style=flat-square&color=C8A415&label=npm) |
| [`LunGula`](https://github.com/CrOliX-AltF4/LunGula) | Imitation learning: game replays in, ONNX policy out | Python · PyTorch · ONNX | ![paused](https://img.shields.io/badge/-on_pause-8a7a5a?style=flat-square) |

**How it holds together**

- **Standalone first.** Every satellite works on its own. Turn Natsume off and nothing else breaks.
- **One LLM per project.** LunAcedia's agent handles mail and calendar. The Core routes the request, relays the answer and speaks it.
- **Hub-and-spoke.** Once wired, satellites only talk to the Core, never to each other.
- **Human in control.** Any AI can be switched off, paused or triggered by hand. Actions go through autonomy tiers (`auto` · `confirm` · `manual`).
- **Private by default.** Nothing is exposed to the internet. The phone reaches home over a private network.

---

## ◈ natsume, the core

> [!WARNING]
> **LunAnima** is proprietary software. Its source code is not open source, and all visual assets¹ used on the showcase site are © CrOliX-AltF4, All Rights Reserved. Do not redistribute or reuse them without permission.
>
> ¹ : in accordance with the artist's terms of use

A personal assistant with a character. More than a chatbot. She keeps track of my mail, calendar and
tasks, remembers what matters, speaks up when it's worth it and keeps me company while I play or work.

| Area | What she does |
|---|---|
| **Voice** | Groq Whisper STT, VAD, wake word, barge-in. TTS via Edge, Kokoro, Piper or ElevenLabs, plus an RVC voice changer |
| **Memory** | Short-term buffer, long-term facts, opinions and world model. Single write gate, daily consolidation, contradiction checks |
| **Personality** | 7 moods with natural decay, affinity tiers, controlled disagreement |
| **Assistant** | Hands mail, calendar and tasks over to LunAcedia's agent. Morning and evening briefs |
| **Presence** | Screen vision, game hooks (FF14, Minecraft, osu!), VTube Studio lip-sync |
| **Control** | Admin panel: every module can be switched off, paused or run by hand |

```
  PC · Desktop Agent                     NAS · Core (24/7)
  mic · STT · screen · avatar  ──ws──►   state · memory · LLM · panel  ──►  LunAcedia
                               ◄──────   reply + voice
```

---

## ◈ now building

| | |
|---|---|
| **Focus** | The assistant first: memory, inbox, delegation, response latency |
| **Next** | Live test on the NAS → scoped mobile keys → per-entity memory → mobile assistant |
| **Paused** | Streaming and LunGula, which will return together |
| **Mode** | YOLO, as always |

> [!TIP]
> The story behind the ecosystem, and the entity at its heart, lives on [my website](https://crolix-website.vercel.app).

---

## ⬡ stack

<div align="center">

| | |
|:---:|:---|
| **frontend** | ![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB) ![Vue.js](https://img.shields.io/badge/Vue.js-35495E?style=for-the-badge&logo=vuedotjs&logoColor=4FC08D) ![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white) ![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white) ![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white) ![TailwindCSS](https://img.shields.io/badge/Tailwind-0F172A?style=for-the-badge&logo=tailwindcss&logoColor=38BDF8) ![Vite](https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white) ![Astro](https://img.shields.io/badge/Astro-17191E?style=for-the-badge&logo=astro&logoColor=FF5D01) ![Storybook](https://img.shields.io/badge/Storybook-FF4785?style=for-the-badge&logo=storybook&logoColor=white) |
| **backend** | ![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white) ![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white) ![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white) ![Laravel](https://img.shields.io/badge/Laravel-FF2D20?style=for-the-badge&logo=laravel&logoColor=white) ![Symfony](https://img.shields.io/badge/Symfony-000000?style=for-the-badge&logo=symfony&logoColor=white) ![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white) ![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white) ![SQLite](https://img.shields.io/badge/SQLite-003B57?style=for-the-badge&logo=sqlite&logoColor=white) |
| **mobile** | ![Flutter](https://img.shields.io/badge/Flutter-02569B?style=for-the-badge&logo=flutter&logoColor=white) ![Dart](https://img.shields.io/badge/Dart-0175C2?style=for-the-badge&logo=dart&logoColor=white) ![Firebase](https://img.shields.io/badge/Firebase-FFCA28?style=for-the-badge&logo=firebase&logoColor=black) |
| **AI** | ![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=for-the-badge&logo=openai&logoColor=white) ![Groq](https://img.shields.io/badge/Groq-F55036?style=for-the-badge&logo=groq&logoColor=white) ![Whisper](https://img.shields.io/badge/Whisper-000000?style=for-the-badge&logo=openai&logoColor=white) ![Ollama](https://img.shields.io/badge/Ollama-000000?style=for-the-badge&logo=ollama&logoColor=white) ![ONNX](https://img.shields.io/badge/ONNX-005CED?style=for-the-badge&logo=onnx&logoColor=white) |
| **tooling** | ![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white) ![FFmpeg](https://img.shields.io/badge/FFmpeg-007808?style=for-the-badge&logo=ffmpeg&logoColor=white) ![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white) ![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black) ![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white) |

</div>

---

## ◈ github stats

<div align="center">

<img height="160" src="https://readme-stats-xi-eight.vercel.app/api?username=CrOliX-AltF4&show_icons=true&theme=dark&hide_border=true&bg_color=0a0a0a&title_color=ffffff&icon_color=ffffff&text_color=888888&ring_color=ffffff"/>
<img height="160" src="https://readme-stats-xi-eight.vercel.app/api/top-langs/?username=CrOliX-AltF4&layout=compact&theme=dark&hide_border=true&bg_color=0a0a0a&title_color=ffffff&text_color=888888"/>

<br/>

[![GitHub Streak](https://readme-streak-stats-woad.vercel.app?user=CrOliX-AltF4&theme=dark&hide_border=true)](https://git.io/streak-stats)

</div>

---

<div align="center">

```
  ╔══════════════════════════════════════════════════════════════╗
  ║          [ session terminated — memory persists ]            ║
  ╚══════════════════════════════════════════════════════════════╝
```

`natsume@w-AI-fu:~$ _`

</div>
