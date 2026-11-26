# 🛡️ Sentinel — File Integrity Monitoring & Recovery

> A modern, browser-based file integrity monitoring and recovery application with post-quantum cryptographic sealing and real-time change detection.

[![Live Demo](https://img.shields.io/badge/Live-Demo-brightgreen?style=for-the-badge)](https://your-demo-link.com)
[![GitHub](https://img.shields.io/badge/GitHub-Repository-blue?style=for-the-badge&logo=github)](https://github.com/AP24110010141/file-sentinel-restore)
[![React](https://img.shields.io/badge/React-19-61DAFB?style=for-the-badge&logo=react)](https://react.dev)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.8-3178C6?style=for-the-badge&logo=typescript)](https://www.typescriptlang.org)
[![Vite](https://img.shields.io/badge/Vite-8.x-646CFF?style=for-the-badge&logo=vite)](https://vitejs.dev)

---

## 📹 Video Presentation

> 🎥 Watch the full project walkthrough and demonstration:
> **[▶️ Click here to watch the Video Presentation](https://drive.google.com/file/d/138d3bE0ey9r7WrIwmssV2Ksf8fYObcVh/view?usp=sharing)**

---

## 📌 Overview

**Sentinel** is a file integrity monitoring and recovery web application. It allows users to fingerprint important files, detect unauthorized changes, review activity logs, and restore from verified backups — all from a clean, modern dashboard running entirely in the browser.

Built with cutting-edge security in mind, Sentinel uses **post-quantum cryptographic sealing** (ML-DSA-65, same standard as Java 24 JEP 497) to protect its file registry from tampering.

---

## ✨ Features

| Feature | Description |
|---|---|
| 🔍 **File Fingerprinting** | Fingerprint files using SHA-256, SHA3-256, or BLAKE3 |
| 🔐 **Post-Quantum Registry Seal** | Registry sealed with ML-DSA-65 — tamper-proof against future threats |
| 📈 **Entropy-Based Change Detection** | Detects ransomware-style file changes via entropy analysis |
| 🔄 **Backup & Recovery** | Manage and restore from multiple backup versions |
| 📋 **Activity Logs** | Full audit trail of all file events |
| 📊 **Monitoring Dashboard** | Real-time overview of monitored files and alerts |
| 🔎 **Diff Viewer** | Side-by-side text diff between backup and current file |
| 🔔 **Desktop Notifications** | System-level alerts for suspicious changes |
| 🗂️ **Backup Retention Policy** | Keep last N versions, preserving baseline integrity |
| ⚙️ **Settings & Configuration** | Fully configurable monitoring preferences |

---

## 🏗️ Tech Stack

- **Frontend**: React 19, TypeScript 5.8, TailwindCSS 4
- **Routing**: TanStack Router (file-based routing)
- **State & Data**: TanStack Query, IndexedDB (via `idb`)
- **Cryptography**: `@noble/hashes` (SHA-256, SHA3-256, BLAKE3), `@noble/post-quantum` (ML-DSA-65)
- **UI Components**: Radix UI + shadcn/ui, Lucide Icons, Recharts
- **Build Tool**: Vite 8
- **Testing**: Vitest, Testing Library
- **Code Quality**: ESLint, Prettier

---

## 🚀 Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) (LTS recommended) **or** [Bun](https://bun.sh/)
- npm, yarn, or bun package manager

### Installation

```bash
# Clone the repository
git clone https://github.com/AP24110010141/file-sentinel-restore.git
cd file-sentinel-restore

# Install dependencies
npm install
# or with bun
bun install
```

### Run Locally

```bash
npm run dev
# or
bun run dev
```

Open the local URL printed by Vite in your terminal (usually `http://localhost:5173`).

### Production Build

```bash
npm run build
npm run preview
```

---

## 🧪 Running Tests

```bash
# Run tests once
npm run test

# Run in watch mode
npm run test:watch
```

---

## 📁 Project Structure

```
src/
├── components/
│   ├── sentinel/        # Core app components (AppShell, DiffDialog, etc.)
│   └── ui/              # Reusable UI components (shadcn/ui)
├── lib/
│   └── sentinel/        # Core logic
│       ├── engine.ts    # File monitoring engine
│       ├── hash.ts      # Cryptographic hashing
│       ├── seal.ts      # Post-quantum registry sealing
│       ├── idb-repo.ts  # IndexedDB persistence layer
│       └── types.ts     # TypeScript types
├── routes/              # File-based routes (TanStack Router)
│   ├── index.tsx        # Dashboard
│   ├── files.tsx        # File manager
│   ├── backups.tsx      # Backup & recovery
│   ├── monitoring.tsx   # Monitoring view
│   ├── logs.tsx         # Activity logs
│   └── settings.tsx     # Settings
└── styles.css           # Global styles
```

---

## 🗺️ Roadmap

- [x] Fix all build, runtime, and console errors
- [x] Hash algorithm choice: SHA-256, SHA3-256, BLAKE3
- [x] Post-quantum signed registry seal (ML-DSA-65 / JEP 497)
- [x] Ransomware-style change detection via entropy analysis
- [x] Diff viewer: backup vs current file for text files
- [x] Backup retention policy (keep last N versions)
- [x] Desktop (system) notifications for alerts
- [ ] Cloud backup sync support
- [ ] Multi-user / team access
- [ ] Mobile-responsive PWA support

---

## 👩‍💻 Author

**Madhvika Kanteti**  
📧 AP24110010141 | SRM University AP

---

## 📄 License

This project is for educational purposes.
