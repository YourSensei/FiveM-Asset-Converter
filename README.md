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
1. Maak een map genaamd `resources` aan in de hoofdmap.
2. Plaats de FiveM/RedM resources die je wilt converteren in de `resources` map.
3. Start het script via je terminal (`python "FIVEM ASSETS MANIFEST.py"`) of dubbelklik op de `.exe` nadat je deze hebt gebouwd.

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
1. Create a folder named `resources` in the root directory.
2. Place the FiveM/RedM resources you want to convert inside this `resources` folder.
3. Start the script via your terminal (`python "FIVEM ASSETS MANIFEST.py"`) or double-click the `.exe` once it is compiled.

---

## 🇹🇷 Türkçe (Turkish Description)

Eski `__resource.lua` formatındaki FiveM/RedM scriptlerini otomatik olarak modern `fxmanifest.lua` formatına dönüştüren, hızlı ve güvenilir bir Python CLI aracı (ve bağımsız `.exe` programı).

### 🚀 Özellikler
* **Otomatik Dönüştürme**: Klasörleri derinlemesine tarar ve `__resource.lua` dosyalarını doğrudan `fxmanifest.lua` formatına çevirir.
* **Mantıksal Kod Koruması**: Eski manifest sürüm satırlarını kaldırır, en üste modern `fx_version` ve `game` etiketlerini ekler; mevcut script, export ve değişkenlerinizi ise tamamen korur.
* **Toplu Güncelleme**: İsteğe bağlı olarak mevcut `fxmanifest.lua` dosyalarını daha yeni bir FX sürümüne (örneğin *adamant*'tan *cerulean*'a) güncelleyebilir.
* **PyInstaller Uyumlu**: Derlenmiş `.exe` dosyaları gibi etkileşimli ok tuşu menülerini desteklemeyen ortamlarda, otomatik olarak kararlı bir sayısal seçim moduna geçer.
* **Renkli ve Net Loglar**: `rich` kütüphanesi sayesinde terminalde anlaşılır ve renk kodlu çıktılar sunar.

### 🛠️ Nasıl Kullanılır
1. Ana dizinde `resources` adında bir klasör oluşturun.
2. Dönüştürmek istediğiniz FiveM/RedM scriptlerini bu `resources` klasörünün içine yükleyin.
3. Terminal üzerinden betiği başlatın (`python "FIVEM ASSETS MANIFEST.py"`) veya derlediğiniz `.exe` dosyasına çift tıklayarak çalıştırın.

---

## 📁 Project Structure / Proje Yapısı

```text
📁 Your-Project-Folder/
├── 📁 resources/               # <-- Scripts buraya / Place your scripts here
├── 📄 FIVEM ASSETS MANIFEST.py # Main script
├── 📄 converter.py             # Dönüştürme mantığı / Conversion logic
├── 📄 logger.py                # Konsol log yardımcısı / Console logger helper
└── 📄 README.md                # Bu kılavuz / This manual
```

## 💻 Compilation / .exe Olarak Derleme

```bash
pyinstaller --onefile --console --name "FiveM_Asset_Converter" "FIVEM ASSETS MANIFEST.py"
```
Derleme bittikten sonra hazır haldeki executable (`FiveM_Asset_Converter.exe`) dosyasını **`dist/`** klasörünün içinde bulabilirsiniz.

## ⚠️ Safety & Backups
* **NL**: Het script verwijdert na een succesvolle conversie het oude `__resource.lua` bestand om serverconflicten te voorkomen. Maak altijd een backup van je resources voordat je een massaconversie start!
* **EN**: After a successful conversion, the script deletes the legacy `__resource.lua` file to prevent manifest conflicts. It is highly recommended to make a backup of your resources before running a bulk conversion!
* **TR**: Başarılı bir dönüştürmeden sonra, sunucu içi manifest çakışmalarını önlemek amacıyla eski `__resource.lua` dosyası silinir. Toplu dönüştürme yapmadan önce scriptlerinizin yedeğini almanız kesinlikle tavsiye edilir!
