# FiveM / RedM Resource Manifest Converter

---

## 🇳🇱 Nederlands (Dutch Description)

Een snelle en betrouwbare Python CLI-tool (en standalone `.exe`) om verouderde FiveM/RedM resources volautomatisch om te zetten van het legacy `__resource.lua` formaat naar het moderne `fxmanifest.lua` formaat.

### 🚀 Kenmerken
* **Automatische Conversie**: Scant mappen recursief en zet `__resource.lua` direct om naar `fxmanifest.lua`.
* **Behoud van Logica**: Verwijdert oude manifest-versieregels en plaatst de moderne `fx_version` en `game` tags bovenaan, met behoud van al je bestaande scripts en instellingen.
* **Massa Updates**: Kan optioneel ook bestaande `fxmanifest.lua` bestanden updaten naar een nieuwere FX-versie (bijv. van *adamant* naar *cerulean*).
* **PyInstaller Proof**: Bevat een automatische stabiele fallback-modus voor omgevingen waar interactieve menu's niet worden ondersteund (zoals gecodeerde `.exe` bestanden).
* **Overzichtelijke Logs**: Maakt gebruik van duidelijke, gekleurde console-output via de `rich` library.

### 🛠️ Gebruik

#### Methode 1: Direct via Python runnen
1. Maak een map genaamd `resources` aan in de hoofdmap.
2. Plaats de FiveM/RedM resources die je wilt converteren in de `resources` map.
3. Start het script via je terminal:
   ```bash
   python "FIVEM ASSETS MANIFEST.py"
   ```

#### Methode 2: Standalone `.exe` gebruiken
Als je de executable (`FiveM_Asset_Converter.exe`) hebt gebouwd, plaats deze dan simpelweg naast je `resources` map en dubbelklik om de tool direct te starten!

---

## 🇬🇧 English (English Description)

A fast, reliable Python CLI tool (and standalone `.exe`) to automatically convert outdated FiveM/RedM resources from the legacy `__resource.lua` manifest format to the modern `fxmanifest.lua` format.

### 🚀 Features
* **Automatic Conversion**: Recursively scans directories and converts `__resource.lua` directly into `fxmanifest.lua`.
* **Logic Preservation**: Removes old manifest version lines and injects modern `fx_version` and `game` tags at the top, while keeping all your existing scripts, exports, and variables completely intact.
* **Bulk Updates**: Optionally updates existing `fxmanifest.lua` files to a newer FX version (e.g., from *adamant* to *cerulean*).
* **PyInstaller Ready**: Features an automatic, stable fallback text-mode for environments where interactive arrow-key menus are not supported (such as compiled `.exe` files).
* **Clean & Colored Logs**: Utilizes clear, color-coded console output powered by the `rich` library.

### 🛠️ How to Use

#### Method 1: Running directly with Python
1. Create a folder named `resources` in the root directory.
2. Place the FiveM/RedM resources you want to convert inside this `resources` folder.
3. Start the script via your terminal:
   ```bash
   python "FIVEM ASSETS MANIFEST.py"
   ```

#### Method 2: Using the standalone `.exe`
If you have generated the executable (`FiveM_Asset_Converter.exe`), simply move it next to your `resources` folder and double-click it to start converting instantly!

---

## 📁 Project Structure / Projectstructuur

Zorg dat de bestanden als volgt in je projectmap staan / Ensure your project files are organized as follows:

```text
📁 Your-Project-Folder/
├── 📁 resources/               # <-- Plaats hier je scripts / Place your scripts here
├── 📄 FIVEM ASSETS MANIFEST.py # Main script
├── 📄 converter.py             # Conversielogica / Conversion logic
├── 📄 logger.py                # Console logger helper
└── 📄 README.md                # Deze handleiding / This manual
```

## 💻 Compilation / Compileren naar .exe

Om het script om te bouwen tot een standalone applicatie die overal zonder Python werkt, gebruik je PyInstaller via de opdrachtprompt (`cmd`):

```bash
pyinstaller --onefile --console --name "FiveM_Asset_Converter" "FIVEM ASSETS MANIFEST.py"
```
Na het bouwen vind je jouw kant-en-klare executable (`FiveM_Asset_Converter.exe`) in de map **`dist/`**.

## ⚠️ Safety & Backups
* **NL**: Het script verwijdert na een succesvolle conversie het oude `__resource.lua` bestand om serverconflicten te voorkomen. Maak altijd een backup van je resources voordat je een massaconversie start!
* **EN**: After a successful conversion, the script deletes the legacy `__resource.lua` file to prevent manifest conflicts. It is highly recommended to make a backup of your resources before running a bulk conversion!
