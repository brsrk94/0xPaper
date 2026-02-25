---
title: "Nox — Raycast-style Application Launcher"
date: 2026-02-25
draft: false
summary: "Building a Qt6/QML launcher inspired by Raycast with modular plugins and sub-50ms search latency."
---

Building **Nox** meant wiring together Qt6, QML, and modern C++ so the UI felt snappy while the backend handled fuzzy search, plugins, and system-wide hotkeys.

Each keystroke is routed through a multithreaded indexing pipeline, letting the launcher stay under 50 ms across 10,000+ entries. That performance gave the app the same “instant” feel Raycast sets, even when querying files, apps, or shortcuts in the same frame.

Key highlights:

- **Tools:** Qt6, QML, C++, CMake, GitHub for source control and releases.
- **Launcher core:** Keyboard-driven surface with fuzzy search that combines apps, documents, and custom commands into a single palette.
- **Plugin architecture:** Modular QtQuick panels (calculator, clipboard history, web search) plus a system tray presence and global hotkeys for Linux/Windows.
- **Concurrency:** Indexing runs on worker threads that keep the UI responsive while reflecting changes immediately.

Building Nox also meant fine-tuning the QML animations so the launcher slides in smoothly, then routing the chosen command back to the C++ backend to execute.

> Will resume later