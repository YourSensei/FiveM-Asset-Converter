# FiveM / RedM Resource Manifest Converter

Een snelle en betrouwbare Python CLI-tool (en standalone `.exe`) om verouderde FiveM/RedM resources volautomatisch om te zetten van het legacy `__resource.lua` formaat naar het moderne `fxmanifest.lua` formaat.

---

## 🚀 Kenmerken

* **Automatische Conversie**: Scant mappen recursief en zet `__resource.lua` direct om naar `fxmanifest.lua`.
* **Behoud van Logica**: Verwijdert oude manifest-versieregels en plaatst de moderne `fx_version` en `game` tags bovenaan, met behoud van al je bestaande scripts en instellingen.
* **Massa Updates**: Kan optioneel ook bestaande `fxmanifest.lua` bestanden updaten naar een nieuwere FX-versie (bijv. van *adamant* naar *cerulean*).
* **PyInstaller Proof**: Bevat een automatische stabiele fallback-modus voor omgevingen waar interactieve menu's niet worden ondersteund (zoals gecodeerde `.exe` bestanden).
* **Overzichtelijke Logs**: Maakt gebruik van duidelijke, gekleurde console-output via de `rich` library.

---

## 📁 Project Structuur

Zorg dat de bestanden als volgt in je projectmap staan:

```text
📁 Jouw-Project-Map/
├── 📁 resources/               # <-- Plaats hier de om te zetten FiveM/RedM scripts
├── 📄 FIVEM ASSETS MANIFEST.py # Main script
├── 📄 converter.py             # Conversielogica (Changer klasse)
├── 📄 logger.py                # Console logger helper
└── 📄 README.md                # Deze handleiding
```

---

## 💻 Installatie & Vereisten

Als je het script direct via Python wilt draaien, installeer dan eerst de benodigde afhankelijkheden:

```bash
pip install questionary rich
```

---

## 🛠️ Gebruik

### Methode 1: Direct via Python runnen
1. Maak een map genaamd `resources` aan in de hoofdmap.
2. Plaats de FiveM/RedM resources die je wilt converteren in de `resources` map.
3. Start het script via je terminal:
   ```bash
   python "FIVEM ASSETS MANIFEST.py"
   ```

### Methode 2: Compileren naar een los `.exe` bestand
Om het script om te bouwen tot een standalone applicatie die overal zonder Python werkt, gebruik je PyInstaller:

```bash
pyinstaller --onefile --console --name "FiveM_Asset_Converter" "FIVEM ASSETS MANIFEST.py"
```
Na het bouwen vind je jouw kant-en-klare executable (`FiveM_Asset_Converter.exe`) in de nieuw aangemaakte map **`dist/`**. Plaats deze simpelweg naast je `resources` map en dubbelklik om te starten!

---

## ⚙️ Ondersteunde Opties

Tijdens het opstarten kun je de volgende instellingen kiezen:
* **FX Versions**: `adamant` | `bodacious` | `cerulean`
* **Target Games**: `gta5` (FiveM) | `rdr3` (RedM) | `common` (Beide)

---

## ⚠️ Veiligheid & Backups
*Het script verwijdert na een succesvolle conversie het oude `__resource.lua` bestand om conflicten binnen de FXServer te voorkomen. Het is altijd aanbevolen om een backup van je resources te maken voordat je een massaconversie start.*
