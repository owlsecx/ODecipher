# 🦉 ODecipher

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux%20%2F%20Windows-informational?style=flat-square&logo=linux&logoColor=white&color=0a0c10"/>
  <img src="https://img.shields.io/badge/Category-OCore%20%2F%20Text%20Analysis-cyan?style=flat-square"/>
  <img src="https://img.shields.io/badge/Interface-GUI%20%28Tkinter%29-blueviolet?style=flat-square"/>
  <img src="https://img.shields.io/badge/No%20Dependencies-Stdlib%20Only-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0-cyan?style=flat-square"/>
</p>

> **ODecipher** is a dark-themed GUI text sleuth and cryptanalysis suite — 27 operations across transform, encode/decode, cryptanalysis, text cleaning, and analysis, with live input stats, Caesar brute-force scoring, pattern detection, and session history export.

---

## 📌 Overview

ODecipher applies text analysis and transformation operations through a Tkinter dark-themed GUI (1200×840). A sidebar controls the operation selector, quick-group shortcuts, actions, clipboard, and live stats. The main panel provides tabbed views for the operation workspace, Caesar brute-force results, session history, and an operation reference.

---

## 🖥️ Interface Tabs

| Tab | Contents |
|-----|---------|
| **SLEUTH** | Input textarea · Run operation button · Output textarea with Copy and Use-as-Input actions |
| **CAESAR BRUTE-FORCE** | All 25 shifts ranked by English likelihood score — best match highlighted — one-click copy of best result |
| **HISTORY** | Treeview of all session operations — timestamp, operation, input/output previews; click for full detail |
| **REFERENCE** | Built-in reference for every operation group |
| **ABOUT** | Tool info |

---

## ⚙️ Operations — 27 Total

### TRANSFORM
| Operation | Description |
|-----------|-------------|
| Reverse Text | Flip the entire text backwards |
| ROT13 | Shift each letter 13 positions — symmetric |
| UPPER case | Convert all letters to uppercase |
| lower case | Convert all letters to lowercase |
| Title Case | Capitalise first letter of each word |
| Swap Case | Toggle each letter's case |
| camelCase | First word lowercase, subsequent words capitalised |
| snake_case | Words joined with underscores, all lowercase |
| kebab-case | Words joined with hyphens, all lowercase |

### ENCODE / DECODE
| Operation | Description |
|-----------|-------------|
| Base64 Encode | RFC 4648 Base64 encoding |
| Base64 Decode | Base64 decode with auto-padding |
| URL Encode | Percent-encode all special characters |
| URL Decode | Decode percent-encoded strings |
| Hex Encode | Each byte as two hex digits |
| Hex Decode | Hex string back to text |

### CRYPTANALYSIS
| Operation | Description |
|-----------|-------------|
| Caesar Brute-Force | Tests all 25 shifts, ranks by English letter frequency score — best match highlighted in the dedicated tab |

### CLEAN
| Operation | Description |
|-----------|-------------|
| Strip whitespace | Remove leading/trailing spaces from every line |
| Remove blank lines | Delete empty lines |
| Remove duplicates | Keep only unique lines (first occurrence) |
| Sort lines | Alphabetical sort of all lines |
| Remove non-printable | Strip control and non-printable characters |

### ANALYSE
| Operation | Description |
|-----------|-------------|
| String Statistics | Character, word, and line count · Shannon entropy · UTF-8 byte size · top-10 character frequency bar chart |
| Pattern Detector | Regex search for 12 pattern types across the input text |
| Hash Identifier | Identify hash type from length and character set |

---

## 🔍 Pattern Detector

Searches for 12 pattern types simultaneously:

`Email` · `IPv4` · `IPv6` · `URL` · `MD5` · `SHA-1` · `SHA-256` · `Base64` · `Credit Card` · `Phone` · `JWT` · `Private Key (PEM header)`

---

## 🏷️ Hash Identifier

Identifies hash types from length and character set:

| Length | Type |
|--------|------|
| 32 | MD5 |
| 40 | SHA-1 |
| 56 | SHA-224 |
| 64 | SHA-256 |
| 96 | SHA-384 |
| 128 | SHA-512 |
| 60 (starts `$2`) | bcrypt |
| Starts `$6$` | SHA-512 crypt (Linux shadow) |
| Starts `$5$` / `$y$` | SHA-256 crypt / yescrypt |

---

## 📊 Live Input Stats

The sidebar updates live on every keystroke:

| Stat | Description |
|------|-------------|
| **Chars** | Total character count |
| **Words** | Word count |
| **Lines** | Line count |
| **Entropy** | Shannon entropy (bits/char) |

---

## 🎛️ Sidebar Controls

| Section | Controls |
|---------|---------|
| **OPERATION** | Dropdown selector with all 27 operations |
| **QUICK GROUPS** | One-click jump to first op of each group: Transform · Encode/Decode · Cryptanalysis · Clean · Analyse |
| **ACTIONS** | Run · Swap Input/Output · Clear All |
| **CLIPBOARD** | Paste to Input · Copy Output |
| **INPUT STATS** | Live Chars / Words / Lines / Entropy |
| **EXPORT HISTORY** | Export JSON · Export TXT · Clear History |

---

## 📤 Export

Session history exported via native file-save dialog:

| Format | Contents |
|--------|----------|
| **JSON** | Tool metadata, exported timestamp, list of all operations: timestamp, operation name, full input, full output |
| **TXT** | Human-readable log of all operations |

---

## ⚙️ Requirements

- **Linux or Windows** with a display
- **No Python installation needed** — runs as a standalone executable
- **No external dependencies** — Tkinter is part of the Python standard library

---

## 🚀 Usage

```bash
./ODecipher
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
