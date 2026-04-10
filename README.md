# Verschlüsseler

[![GUI Demo](screenshots/gui-demo.png)](screenshots/gui-demo.png)
*Modern Caesar Cipher Tool für Text- und Dateiverschlüsselung*

**Verschlüsseler** ist ein benutzerfreundliches Verschlüsselungsprogramm basierend auf dem Caesar-Chiffre-Algorithmus. Es verschiebt Buchstaben (a-z, 0-9) um einen festen Shift-Wert, wiederholt dies mehrfach und behält Nicht-Alphanumerikzeichen unverändert. Deterministische Schlüsselabgeleitung für sichere, reproduzierbare Verschlüsselung.

## 🚀 Features

- **Text-Verschlüsselung** – Einfacher Eingabebereich mit Live-Vorschau
- **Datei-Verarbeitung** – Drag & Drop oder Dateiauswahl (UTF-8 Textdateien)
- **Schlüssel-Generator** – Sichere, zufällige Schlüssel (alphanumerisch)
- **Schlüssel-Modus** – Shift & Wiederholungen aus Schlüssel abgeleitet
- **Moderne GUI** – Dunkles Theme, NavigationRail, Flet (Flutter)
- **CLI-Unterstützung** – `python verschluesseler.py --encrypt "Hallo"`
- **Portable EXE** – PyInstaller-ready (.spec inklusive)

| Modus | Standard | Schlüssel-abgeleitet |
|-------|----------|---------------------|
| **Shift** | 3 | `sum(ord(c)) % 36` |
| **Wdh.** | 10 | `(len(key) % 15) + 5` |

## 📱 GUI Demo

```
Text-Tab     | Datei-Tab      | Key-Gen       | Key-Text
-------------|---------------|---------------|----------
[Input]      | [Datei-Pfad]  | [Generieren]  | [Schlüssel]
[V/E]        | [Speichern]   | [Kopieren]    | [Input]
[Parameter]  | [Status]      |               | [V/E]
[Output]     |               |               | [Output]
```

## 🛠 Installation

```bash
# Klonen (falls Repo)
git clone <repo>
cd Verschluesseler

# Abhängigkeiten
pip install -r requirements.txt
```

**requirements.txt:**
```
flet>=0.24.0
```

## 🚀 Ausführen

### GUI (Standard)
```bash
python verschluesseler.py
```
*960x780px Fenster, zentriert, frameless.*

### CLI Beispiele
```bash
# Text
python verschluesseler.py --encrypt "Hallo Welt" --shift 5 --times 3
python verschluesseler.py --decrypt "k{nq{f{m|s"

# Datei
python verschluesseler.py --file geheim.txt --encrypt
python verschluesseler.py --file geheim.enc --decrypt --out entschluesselt.txt

# Demo
python verschluesseler.py --demo
```

### Portable EXE bauen
```bash
pip install pyinstaller
pyi-makespec --onefile --windowed --name Verschluesseler verschluesseler.spec
pyinstaller Verschluesseler.spec
```
*Ergebnis: `dist/Verschluesseler.exe` (standalone, kein Python nötig)*

## 📦 Installer (Windows)

Ordner `installer/`:
```bash
# Inno Setup (empfohlen)
"C:\Program Files (x86)\Inno Setup 6\ISCC.exe" verschluesseler.iss

# NSIS
makensis verschluesseler.nsi
```
*Erstellt Setup.exe im Projekt-Root.*

## 🔧 Entwicklung

- **Main**: `verschluesseler.py` (GUI + CLI)
- **File Dialog**: `file_dialog.py` (native Windows)
- **Test**: `test_final.py`
- **Build**: `build/` (PyInstaller Artefakte)
- **Status**: Fertig (TODO.md abgehakt)

### Screenshot-Ordner erstellen
```
screenshots/
├── gui-text.png
├── gui-file.png
└── cli-demo.png
```

## ⚠️ Hinweise

- **Nur Textdateien** (UTF-8); Binärdateien werden nicht unterstützt.
- **Sicherheit**: Caesar ist **nicht kryptographisch sicher** – nur für Lern-/Demo-Zwecke.
- **Plattform**: Windows-fokussiert (native Dialoge), läuft aber cross-platform.
- **Lizenzen**: MIT (falls nicht anders angegeben).

## 🙌 Danke

Entwickelt mit ❤️ using Flet, PyInstaller, Inno Setup.
_© 2024 – Open Source verfügbar._

---
**Fragen?** Schaue in `TODO.md` oder den Code. Viel Spaß beim Verschlüsseln! 🔐

