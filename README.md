# Rostyman

**Local-first desktop API client — powerful, private, and free**

Rostyman runs entirely on your machine with no account required. Your APIs. Your machine. Your rules.

![Rostyman](https://img.shields.io/badge/version-1.0.0--rc.6-blue) ![Platforms](https://img.shields.io/badge/platforms-Windows%20%7C%20macOS%20%7C%20Linux-green) ![Architectures](https://img.shields.io/badge/arch-x64%20%7C%20ARM64-lightgrey) ![Protocols](https://img.shields.io/badge/protocols-8-orange)

## Download

The easiest way to get the right build is **[rostyman.com/download](https://rostyman.com/download)** — it detects your OS and CPU and highlights the matching installer. All installers are also attached to every [GitHub release](https://github.com/rostymanteam/rostyman/releases).

| Platform | Package | Install |
|----------|---------|---------|
| **Windows** (x64 / ARM64) | `.exe` installer | Run the installer. If you see "Windows protected your PC", click **More info** → **Run anyway** |
| **macOS** (Apple Silicon / Intel) | `.dmg` | Drag to Applications, then see the note below |
| **Linux** (x64 / ARM64) | `.deb`, `.rpm`, `.AppImage` | `sudo apt install ./rostyman_*.deb` · `sudo dnf install ./rostyman-*.rpm` · or `chmod +x` the AppImage and run |

### macOS — First Launch

Rostyman is not yet code-signed. On first launch, right-click the app → **Open** → **Open**. If macOS says the app is "damaged", run this once in **Terminal**, then open it normally:

```bash
xattr -dr com.apple.quarantine /Applications/Rostyman.app
```

## What's New in v1.0.0-rc.6

> Release candidate on the road to 1.0 — stable for everyday work. Please report anything that looks off in [Issues](https://github.com/rostymanteam/rostyman/issues).

### Specifications — edit your common files, manage your project documents
- A new sidebar section for the files around your API work — notes, specs, README, JSON/YAML/env config, CSV, SQL and code snippets
- Real files in `Documents/Rostyman/Specifications/`, organised into projects and folders — git and other editors see exactly what you see
- Syntax highlighting, **Pretty / Compact** for JSON, XML, YAML, SQL, CSS and HTML (`Shift+Alt+F`), Markdown **Edit / Split / Preview** with sticky headings
- Explicit Save only — files are never written behind your back
- **Opt-in file associations** on Windows, macOS and Linux — double-click a file to open it in Rostyman, even when the app isn't running; uninstalling restores your previous defaults

### Screenshots you can mark up
- Pen, highlighter, arrow, rectangle, ellipse, text, eraser and crop, with undo/redo — copy the result, save a copy, or overwrite the original
- Region capture is much faster — the selection overlay appears almost instantly

### Help shape Rostyman
- An occasional, **optional** feedback card asks what you'd like us to build next — it never asks about pricing; open it any time from **More → Shape Rostyman**

### Updates, polish & fixes
- The Updates tab shows whether you're on the **x64** or **ARM64** build, plus an **"Include pre-release versions"** toggle
- First-launch prompts appear one at a time instead of all at once
- `.rostyman` imports select the collection's default environment; Sync from source is more reliable

Full notes: [v1.0.0-rc.6 release](https://github.com/rostymanteam/rostyman/releases/tag/v1.0.0-rc.6)

### Earlier release candidates
- **rc.5** — native ARM64 builds for Windows and Linux, `.rpm` packages, Create Request from Code (17 languages), architecture-aware updater
- **rc.4** — your data is preserved across updates
- **rc.3** — Find & Replace across collections, Server-Sent Events as a request type, 18 languages
- **rc.1 / rc.2** — first public release candidates: CLI/app parity, 14 auth types, anonymous opt-out crash reports

## Features

### 8 Protocols
- **HTTP/HTTPS** — full request builder with auth, headers, body, params, scripts
- **GraphQL** — Monaco editor, schema introspection, autocomplete, variables
- **gRPC** — proto import, unary + streaming, auth, scripts
- **WebSocket** — connect/disconnect, send/receive, message log
- **Socket.IO** — emit events, auto-capture, auth/query config
- **MQTT** — publish/subscribe, QoS 0/1/2, retain flag, topic management
- **SSE** — Server-Sent Events with real-time event log
- **MCP** — Model Context Protocol server (18 tools) + client (stdio + HTTP)

### AI Assistant
- Multi-turn conversational chat with persistent history
- 3 providers: Anthropic Claude, OpenAI, Ollama (local)
- 7 quick actions: Generate, Explain, Tests, Fix, Mock Data, Document, Validate Schema
- Vault-secured API keys

### MCP Support
- **MCP Server** — expose collections to AI agents (Claude, Cursor, Windsurf, VS Code)
- **18 tools** for reading, executing, and creating API resources
- **TLS/HTTPS** support via mkcert, tunnel support (ngrok, cloudflared)
- **Connected clients tracking** with disconnect capability
- **MCP Client** — connect to external MCP servers (stdio + HTTP)

### Collections & Sharing
- Collections with folders, nested subfolders, drag-and-drop
- **Folder-level auth & scripts** — set once, inherited by all child requests
- **Cloud sharing** — connect Google Drive or Dropbox, share collections via link, publish updates
- **Drag & drop import** — drop files to import, auto-detect format
- **Source watching** — auto-detect when linked files or URLs change
- **Collection descriptions** — editable, auto-saved
- Bulk operations — multi-select, bulk delete, copy cURL

### Environments & Variables
- Collection-scoped environments with `{{variable}}` resolution
- Global variables and encrypted Vault
- Variable hover popups with source badges (E/C/G/V)

### Import & Export
- Import from: Postman, Insomnia, OpenAPI, HAR, Thunder Client, Hoppscotch, Bruno, cURL, Rostyman
- Export to: Rostyman JSON, Postman v2.1, and more via plugins
- Import from URL — paste any link, auto-sync when content changes
- `.rostyman` file association — double-click to open on any OS

### Specifications
- Edit the everyday files around your API work — Markdown, text, JSON, YAML, CSV, XML, SQL, env/ini/toml and code
- Real files in `Documents/Rostyman/Specifications/`, projects and folders, import, search, Send to device
- Pretty / Compact formatting, Markdown preview with sticky headings, opt-in OS file associations

### Databases
- 8 drivers — SQLite, PostgreSQL, MySQL, MariaDB, SQL Server, MongoDB, Redis, CockroachDB
- Schema browser, query editor with autocomplete, EXPLAIN visualizer, ER diagram, SSH tunnels
- AI query assistant, generate a CRUD API collection from a schema, DB checks on HTTP requests

### Visual Workflow Editor
- Drag-and-drop canvas with 10 node types (Start, End, HTTP Request, Condition, Loop, Transform, Delay, Set Variable, Comment, Sub-Workflow)
- **Retry logic** — automatic retries with fixed/linear/exponential backoff
- **Response assertions** — pass/fail checks on status, body, headers, and response time
- **Error handling edges** — route failures to any downstream node
- **Run history** — replay any past execution with full trace and timings
- **5 built-in templates** — Health Check, Data Pipeline, Auth Flow, CRUD Suite, Retry Resilience
- Flow Tracer — live execution log with node tracking

### More
- **20 built-in themes** + custom theme builder
- **Mock Server** — local API mocks with variables and environments
- **Scheduler** — cron-based job scheduling with timezone support
- **Collection Runner** — run collections with data files
- **Git Sync** — built-in Git panel with diff viewer, conflict detection, branch management
- **CLI Runner** — `rosty-cli` for CI/CD integration
- **Notifications Center** — searchable panel with native OS alerts
- **Screenshot & Video Capture** — screen capture with mic audio, screenshot annotation, media sidebar
- **File Sharing** — send files and collections to devices on your local network (encrypted, no cloud)
- **Web Intelligence (Beta)** — record and replay browser tests alongside your API tests
- **Request History** — full request + response saved, schema change detection
- **Response Viewer** — JSON viewer, code snippets (30+ languages)
- **System Tray** — minimize to tray
- **Onboarding Tour** — 8-step first-run tour
- **19 keyboard shortcuts** — all cross-platform (Ctrl/Cmd)
- **18 built-in languages** — fully translated
- **Local-first** — works fully offline, no account, no cloud; only anonymous, opt-out usage and crash reports

## Documentation

- [Docs Site](https://docs.rostyman.com)
- [Wiki Home](https://github.com/rostymanteam/rostyman/wiki)
- [Getting Started](https://github.com/rostymanteam/rostyman/wiki/Getting-Started)
- [Collections & Requests](https://github.com/rostymanteam/rostyman/wiki/Collections-and-Requests)
- [AI Assistant](https://github.com/rostymanteam/rostyman/wiki/AI-Assistant)
- [Scripting API](https://github.com/rostymanteam/rostyman/wiki/Scripting)
- [Cloud Storage](https://github.com/rostymanteam/rostyman/wiki/Cloud-Storage)
- [Visual Workflows](https://github.com/rostymanteam/rostyman/wiki/Visual-Workflows)

## Report Issues

Found a bug? [Open an issue](https://github.com/rostymanteam/rostyman/issues).
