# Solar DIY ISO / Solar DIY ISO

[English](#english) | [Polski](#polski)

---

<a name="english"></a>
## 🇺🇸 English

Solar DIY ISO is a custom installer image that allows you to run **Solar Cube EMS** on your **own device**.

This ISO is built on **Ubuntu 24.04.4 LTS Server**.

### 💾 Download
Because the file can be large, we recommend hosting it on a fast mirror (for example OneDrive).

- **ISO download:** `ADD_DOWNLOAD_LINK_HERE`
- **Version:** `0.1.0`
- **Format:** ISO
- **SHA256 checksum:** `ADD_SHA256_HERE`

### 🧰 Minimum hardware requirements
Based on the target configuration below, the minimum recommended hardware is:

- **CPU:** Intel N100 (or equivalent x86_64)
- **RAM:** 8 GB
- **Storage:** 256 GB SSD
- **Security:** TPM 2.0
- **USB installer media:** 8 GB or larger

### 🚀 USB installation guide
1. **Download** the Solar DIY ISO.
2. **Verify checksum** (recommended):
   - Linux/macOS:
     ```bash
     sha256sum solar-diy.iso
     ```
   - Windows PowerShell:
     ```powershell
     Get-FileHash .\solar-diy.iso -Algorithm SHA256
     ```
3. **Prepare a USB drive** (minimum 8 GB; all existing data will be erased).
4. **Write ISO to USB**:
   - **Windows:** [Rufus](https://rufus.ie)
   - **Linux/macOS:** balenaEtcher or `dd`
5. **Insert USB** into the target machine.
6. **Open BIOS/UEFI** (`DEL`, `F2`, `F10`, or `ESC`, depending on device).
7. **Set USB as first boot device** and reboot.
8. **Start installer** and follow on-screen steps.
9. After installation, remove USB and boot from internal SSD.

---

<a name="polski"></a>
## 🇵🇱 Polski

Solar DIY ISO to niestandardowy obraz instalacyjny, który pozwala uruchomić **Solar Cube EMS** na **własnym urządzeniu**.

To ISO zostało zbudowane na bazie **Ubuntu 24.04.4 LTS Server**.

### 💾 Pobieranie
Ze względu na rozmiar pliku zalecamy hosting na szybkim serwerze lustrzanym (np. OneDrive).

- **Pobieranie ISO:** `TUTAJ_WSTAW_LINK_DO_POBRANIA`
- **Wersja:** `0.1.0`
- **Format:** ISO
- **Suma kontrolna SHA256:** `TUTAJ_WSTAW_SHA256`

### 🧰 Minimalne wymagania sprzętowe
Na bazie docelowej konfiguracji minimalnie rekomendowane są:

- **CPU:** Intel N100 (lub równoważny x86_64)
- **RAM:** 8 GB
- **Dysk:** SSD 256 GB
- **Bezpieczeństwo:** TPM 2.0
- **Nośnik instalacyjny USB:** 8 GB lub większy

### 🚀 Instrukcja wgrania ISO na USB i uruchomienia instalacji
1. **Pobierz** obraz Solar DIY ISO.
2. **Zweryfikuj sumę kontrolną** (zalecane):
   - Linux/macOS:
     ```bash
     sha256sum solar-diy.iso
     ```
   - Windows PowerShell:
     ```powershell
     Get-FileHash .\solar-diy.iso -Algorithm SHA256
     ```
3. **Przygotuj pendrive USB** (minimum 8 GB; wszystkie dane zostaną usunięte).
4. **Wgraj ISO na USB**:
   - **Windows:** [Rufus](https://rufus.ie)
   - **Linux/macOS:** balenaEtcher lub `dd`
5. **Podłącz USB** do urządzenia docelowego.
6. **Wejdź do BIOS/UEFI** (`DEL`, `F2`, `F10` lub `ESC` — zależnie od sprzętu).
7. **Ustaw bootowanie z USB** jako pierwsze i uruchom ponownie komputer.
8. **Uruchom instalator** i postępuj zgodnie z instrukcjami na ekranie.
9. Po zakończeniu instalacji wyjmij USB i uruchom system z dysku SSD.
