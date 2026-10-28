<div align="center">

<img src="https://raw.githubusercontent.com/somaylab/somaylab/main/assets/banner.svg" alt="Somay Security Research Lab" width="100%" />

<br/>

<a href="https://github.com/somaylab"><img src="https://img.shields.io/badge/RESEARCH_LAB-OFFENSIVE_DEFENSIVE-0D1117?style=flat-square&logo=shield&logoColor=10B981" alt="Research Lab"/></a>
<a href="https://github.com/somaylab"><img src="https://img.shields.io/badge/ENGINE-CHROMIUM_%2F_GECKO_MV3-0D1117?style=flat-square&logo=googlechrome&logoColor=38BDF8" alt="Engine"/></a>
<a href="https://github.com/somaylab"><img src="https://img.shields.io/badge/DATA_SOVEREIGNTY-100%25_OFFLINE-0D1117?style=flat-square&logo=databricks&logoColor=F59E0B" alt="Data Sovereignty"/></a>
<a href="https://github.com/somaylab"><img src="https://img.shields.io/badge/TELEMETRY-STRICT_ZERO-0D1117?style=flat-square&logo=target&logoColor=EF4444" alt="Telemetry"/></a>
<img src="https://komarev.com/ghpvc/?username=somaylab&label=LAB_VISITORS&color=0d1117&style=flat-square" alt="Visitors"/>

</div>

<br/>

## Laboratory Mandate

Somay Security Research Lab develops deterministic software, security audit utilities, and extraction engines. The mandate focuses on offensive security research directed toward defensive hardening, browser runtime isolation, anti-fingerprinting entropy, and client-side data sovereignty.

All systems are engineered under a strict zero-trust operational doctrine:
- **Client-Side Sovereignty**: Zero upstream telemetry, zero cloud synchronizers, and zero analytics sinks. Data never leaves the host runtime.
- **Deterministic State Fidelity**: State capture, serialization, and restoration achieve 1:1 parity with RFC specifications (including RFC 6265bis CHIPS partition keys).
- **Minimal Attack Surface**: Native browser and OS APIs are prioritized over runtime bloat to prevent privilege escalation and memory decay.

<br/>

## Core Repositories & Systems

| System | Domain | Architecture | Capabilities |
| :--- | :--- | :--- | :--- |
| **[session-swap](https://github.com/somaylab/session-swap)** | State Containerization | Manifest V3 / WebExtensions / DevPop UI | Multi-account container switching, CHIPS `partitionKey` isolation, 1:1 disaster recovery snapshotting, and zero-telemetry client storage. |
| **[ghost-profile](https://github.com/somaylab/ghost-profile)** | Anti-Fingerprinting | Chromium & Gecko Runtime Overrides | Multi-vector entropy spoofing: WebGL shader noise, Canvas 2D mutation, AudioContext jitter, and hardware/locale virtualization. |
| **[map-scrape](https://github.com/somaylab/map-scrape)** | Spatial Data Harvesting | Headless Chromium / Python & Node.js | High-throughput Google Maps entity scraping, stealth request orchestration, and automated normalization into structured XLSX/CSV. |
| **[Haha-Cookies](https://github.com/somaylab/Haha-Cookies)** | Runtime State Telemetry | Chrome Extension MV3 / Storage APIs | Real-time cookie jar lifecycle telemetry, partition inspection, and developer diagnostic auditing. |

<br/>

## System Architecture

```text
+-----------------------------------------------------------------------------------------+
|                      SOMAY SECURITY RESEARCH LAB ARCHITECTURE                           |
+-----------------------------------------------------------------------------------------+
|                                                                                         |
|  [ HARVESTING & EXTRACTION ]            [ RUNTIME ISOLATION & STEALTH ]                 |
|                                                                                         |
|      +--------------------+                 +---------------------+                     |
|      |     map-scrape     |                 |    ghost-profile    |                     |
|      | Spatial Extraction |                 | Entropy Spoofing    |                     |
|      | Headless Chromium  |                 | Canvas/WebGL/Audio  |                     |
|      +---------+----------+                 +----------+----------+                     |
|                |                                       |                                |
|                +-------------------+-------------------+                                |
|                                    |                                                    |
|                                    v                                                    |
|      +-------------------------------------------------------------+                    |
|      |                 BROWSER RUNTIME SANDBOX (MV3)               |                    |
|      |    - Offscreen Documents       - Chrome DevTools Protocol   |                    |
|      |    - Extension Service Worker  - WebExtensions Native APIs  |                    |
|      +-----------------------------+-------------------------------+                    |
|                                    |                                                    |
|                                    v                                                    |
|                        [ PERSISTENCE & ISOLATION ]                                      |
|                                                                                         |
|                        +-------------------------+                                      |
|                        |      session-swap       |                                      |
|                        | CHIPS RFC 6265bis Store |                                      |
|                        | 1:1 State Backup Engine |                                      |
|                        +------------+------------+                                      |
|                                     |                                                   |
|                                     v                                                   |
|  +-----------------------------------------------------------------------------------+  |
|  | SPECIFICATION: STRICT OFFLINE | ZERO TELEMETRY | DETERMINISTIC 1:1 REPLAY         |  |
|  +-----------------------------------------------------------------------------------+  |
+-----------------------------------------------------------------------------------------+
```

<br/>

## Technical Arsenal

```text
Browser Internals  : Manifest V3, WebExtensions, CDP (Chrome DevTools Protocol), CHIPS (RFC 6265bis)
Languages & Core   : TypeScript, JavaScript (ESNext), Python 3, Node.js (V8)
Automation         : Playwright, Puppeteer, Headless Chromium, Cheerio
UI & Desktop Apps  : Electron, Vite, TailwindCSS (Brutalist High-Density), HTML5 Canvas
Systems & Storage  : Docker, Linux (WSL), SQLite, Chrome Storage API, IndexedDB
Security & Recon   : Network Traffic Interception, Entropy Spoofing, Fingerprint Auditing
```

<div align="left">

<img src="https://img.shields.io/badge/TypeScript-0D1117?style=flat-square&logo=typescript&logoColor=3178C6" alt="TypeScript"/>
<img src="https://img.shields.io/badge/Python-0D1117?style=flat-square&logo=python&logoColor=3776AB" alt="Python"/>
<img src="https://img.shields.io/badge/Node.js-0D1117?style=flat-square&logo=nodedotjs&logoColor=5FA04E" alt="Node.js"/>
<img src="https://img.shields.io/badge/Chromium_MV3-0D1117?style=flat-square&logo=googlechrome&logoColor=4285F4" alt="Chromium"/>
<img src="https://img.shields.io/badge/Firefox_Gecko-0D1117?style=flat-square&logo=firefox&logoColor=FF7139" alt="Firefox"/>
<img src="https://img.shields.io/badge/Playwright-0D1117?style=flat-square&logo=playwright&logoColor=2EAD33" alt="Playwright"/>
<img src="https://img.shields.io/badge/Electron-0D1117?style=flat-square&logo=electron&logoColor=47848F" alt="Electron"/>
<img src="https://img.shields.io/badge/Docker-0D1117?style=flat-square&logo=docker&logoColor=2496ED" alt="Docker"/>
<img src="https://img.shields.io/badge/Linux_WSL-0D1117?style=flat-square&logo=linux&logoColor=FCC624" alt="Linux"/>

</div>

<br/>

## Pinned Systems

<div align="center">

<a href="https://github.com/somaylab/session-swap">
  <img src="https://github-readme-stats.vercel.app/api/pin/?username=somaylab&repo=session-swap&title_color=58a6ff&text_color=c9d1d9&icon_color=58a6ff&bg_color=0d1117&border_color=30363d&show_owner=true" alt="session-swap"/>
</a>
<a href="https://github.com/somaylab/map-scrape">
  <img src="https://github-readme-stats.vercel.app/api/pin/?username=somaylab&repo=map-scrape&title_color=58a6ff&text_color=c9d1d9&icon_color=58a6ff&bg_color=0d1117&border_color=30363d&show_owner=true" alt="map-scrape"/>
</a>

</div>

<br/>

## Telemetry & Activity

<div align="center">

<img height="150" src="https://github-readme-stats.vercel.app/api?username=somaylab&show_icons=true&hide_border=false&title_color=58a6ff&text_color=c9d1d9&icon_color=58a6ff&bg_color=0d1117&border_color=30363d" alt="GitHub Stats"/>
<img height="150" src="https://github-readme-stats.vercel.app/api/top-langs/?username=somaylab&layout=compact&hide_border=false&title_color=58a6ff&text_color=c9d1d9&bg_color=0d1117&border_color=30363d&langs_count=6" alt="Top Languages"/>

</div>

<br/>

## Operational Protocol & Disclosures

- **Mandate**: All utilities and research artifacts are developed for offensive security analysis, defensive infrastructure hardening, and educational auditing.
- **Responsible Disclosure**: Security inquiries or vulnerability findings regarding any SomayLab tool should be reported via repository issue or advisory.
- **Verification**: Production commits are cryptographically signed via verified keys.
