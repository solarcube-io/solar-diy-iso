# Solar DIY ISO Energy Management System

[English](#english) | [Polski](#polski)

---

<a name="english"></a>
## 🇺🇸 English

Solar DIY ISO is a custom installer image that allows you to run **Solar DIY EMS** on your **own device**.

This ISO is now based on **Ubuntu 26.04**.

Solar DIY EMS is based on the Solar Cube EMS solution ([solarcube.io](https://solarcube.io)).
When following Solar Cube documentation, replace these URLs as follows:

- `https://solarcube.local` → `https://solardiy.local`
- `https://solarcube.local:5443` → `https://solardiy.local:5443`

### 💾 Download
The link below is masked and configured to start the browser download directly.

- **ISO download:** [Download ISO](https://roygard-my.sharepoint.com/:u:/g/personal/rafal_solarcube_io/IQCU6BefO0dpQrrH5y4hBhZ8Aazbf9J-x_zD51JKHdfUunk?e=QkMes0&download=1)
- **Filename:** `solar_diy_20260428.iso`
- **Format:** ISO
- **SHA256 checksum:** `1fb2cb2b06f2e8a686f7062b179cc919a2da0a30b6aa66d9d6daf13bae189361`

### ⚠️ Important installation requirements
- The target device **must be connected to the Internet through Ethernet/LAN** during installation.
- Installation time is typically **about 30 minutes or longer**, depending on Internet connection speed.

### 🧰 Hardware requirements

| Component | Requirement |
|---|---|
| Firmware | UEFI (**required**) |
| TPM | TPM 2.0 (**required** — disk encryption) |
| CPU | x86_64, min. 2 cores (4 recommended) |
| RAM | Min. 6 GB (8 GB recommended) |
| Storage | Min. 128 GB (256 GB+ recommended) |
| WiFi | WiFi card |
| Ethernet | Min. 1x RJ45 port (2+ recommended) |
| DMI/SMBIOS | Required (physical hardware) |
| Secure Boot | Recommended (PCR 7 measurement) |
| USB installer media | 8 GB or larger |

### 🔧 BIOS/UEFI configuration (required)
Before starting installation, configure BIOS/UEFI as follows:
1. **Boot mode:** UEFI (disable Legacy/CSM).
2. **TPM:** Enable TPM 2.0.
3. **Secure Boot:** Enable if possible (recommended).
4. **Storage mode:** AHCI recommended (disable RAID/RST if unsupported).
5. **Boot order:** Set USB as first boot device.
6. **Network:** Connect Ethernet cable before starting installer.
7. Save changes and reboot.

### 🚀 USB installation guide
1. **Download** the ISO file `solar_diy_20260428.iso`.
2. **Verify checksum** (recommended):
   - Linux:
     ```bash
     sha256sum solar_diy_20260428.iso
     ```
   - macOS:
     ```bash
     shasum -a 256 solar_diy_20260428.iso
     ```
   - Windows PowerShell:
     ```powershell
     Get-FileHash .\solar_diy_20260428.iso -Algorithm SHA256
     ```
3. **Prepare a USB drive** (minimum 8 GB; all existing data will be erased).
4. **Write ISO to USB** (detailed by OS):
   - **Windows (Rufus):**
     1. Download and open [Rufus](https://rufus.ie).
     2. Insert USB drive.
     3. In **Device**, select your USB drive.
     4. Click **SELECT** and choose `solar_diy_20260428.iso`.
     5. Keep default settings (GPT/UEFI unless your hardware requires otherwise).
     6. Click **START** and confirm USB erase.
     7. Wait until status is **READY**.
   - **Linux (GUI: balenaEtcher):**
     1. Open balenaEtcher.
     2. Click **Flash from file** and select `solar_diy_20260428.iso`.
     3. Click **Select target** and choose USB drive.
     4. Click **Flash** and wait for completion.
   - **Linux (CLI: `dd`):**
     1. Identify USB device (example): `lsblk`.
     2. Unmount USB partitions (example): `sudo umount /dev/sdX*`.
     3. Write image: `sudo dd if=solar_diy_20260428.iso of=/dev/sdX bs=4M status=progress oflag=sync`.
     4. Flush buffers: `sync`.
     5. Safely remove USB.
   - **macOS (Terminal):**
     1. Find USB disk: `diskutil list`.
     2. Unmount disk: `diskutil unmountDisk /dev/diskN`.
     3. Write image: `sudo dd if=solar_diy_20260428.iso of=/dev/rdiskN bs=4m`.
     4. Wait for command to finish, then run: `sync`.
     5. Eject USB: `diskutil eject /dev/diskN`.
5. **Insert USB** into the target machine.
6. **Boot from USB** (via BIOS/UEFI boot menu).
7. **Run installer** and follow on-screen steps.
8. Keep Ethernet connected until installation is fully complete.
9. After installation, remove USB and boot from internal SSD.

---

<a name="polski"></a>
## 🇵🇱 Polski

Solar DIY ISO to niestandardowy obraz instalacyjny, który pozwala uruchomić **Solar DIY EMS** na **własnym urządzeniu**.

Ten obraz bazuje teraz na **Ubuntu 26.04**.

Solar DIY EMS działa na bazie rozwiązania Solar Cube EMS ([solarcube.io](https://solarcube.io)).
Korzystając z instrukcji Solar Cube, zamieniaj adresy URL według poniższych zasad:

- `https://solarcube.local` → `https://solardiy.local`
- `https://solarcube.local:5443` → `https://solardiy.local:5443`

### 💾 Pobieranie
Poniższy odnośnik jest ukryty pod etykietą i skonfigurowany tak, aby po kliknięciu od razu rozpocząć pobieranie w przeglądarce.

- **Pobieranie ISO:** [Pobierz ISO](https://roygard-my.sharepoint.com/:u:/g/personal/rafal_solarcube_io/IQCU6BefO0dpQrrH5y4hBhZ8Aazbf9J-x_zD51JKHdfUunk?e=QkMes0&download=1)
- **Nazwa pliku:** `solar_diy_20260428.iso`
- **Format:** ISO
- **Suma kontrolna SHA256:** `1fb2cb2b06f2e8a686f7062b179cc919a2da0a30b6aa66d9d6daf13bae189361`

### ⚠️ Ważne wymagania instalacyjne
- Urządzenie docelowe **musi być podłączone do Internetu przez Ethernet/LAN** podczas instalacji.
- Proces instalacji trwa zwykle **około 30 minut lub dłużej**, w zależności od szybkości łącza internetowego.

### 🧰 Wymagania sprzętowe

| Komponent | Wymaganie |
|---|---|
| Firmware | UEFI (**obowiązkowe**) |
| TPM | TPM 2.0 (**obowiązkowe** — szyfrowanie dysku) |
| CPU | x86_64, min. 2 rdzenie (zalecane 4) |
| RAM | Min. 6 GB (zalecane 8 GB) |
| Dysk | Min. 128 GB (zalecane 256 GB+) |
| WiFi | Karta WiFi |
| Ethernet | Min. 1 port RJ45 (zalecane 2+) |
| DMI/SMBIOS | Wymagane (sprzęt fizyczny) |
| Secure Boot | Zalecane (pomiar PCR 7) |
| Nośnik instalacyjny USB | 8 GB lub większy |

### 🔧 Konfiguracja BIOS/UEFI (wymagane)
Przed rozpoczęciem instalacji ustaw w BIOS/UEFI:
1. **Tryb bootowania:** UEFI (wyłącz Legacy/CSM).
2. **TPM:** włącz TPM 2.0.
3. **Secure Boot:** włącz, jeśli to możliwe (zalecane).
4. **Tryb kontrolera dysku:** zalecany AHCI (wyłącz RAID/RST, jeśli niewspierane).
5. **Kolejność bootowania:** ustaw USB jako pierwsze.
6. **Sieć:** podłącz kabel Ethernet przed uruchomieniem instalatora.
7. Zapisz zmiany i uruchom komputer ponownie.

### 🚀 Instrukcja wgrania ISO na USB i uruchomienia instalacji
1. **Pobierz** plik ISO `solar_diy_20260428.iso`.
2. **Zweryfikuj sumę kontrolną** (zalecane):
   - Linux:
     ```bash
     sha256sum solar_diy_20260428.iso
     ```
   - macOS:
     ```bash
     shasum -a 256 solar_diy_20260428.iso
     ```
   - Windows PowerShell:
     ```powershell
     Get-FileHash .\solar_diy_20260428.iso -Algorithm SHA256
     ```
3. **Przygotuj pendrive USB** (minimum 8 GB; wszystkie dane zostaną usunięte).
4. **Wgraj ISO na USB** (dokładnie dla każdego systemu):
   - **Windows (Rufus):**
     1. Pobierz i uruchom [Rufus](https://rufus.ie).
     2. Podłącz pendrive USB.
     3. W polu **Device** wybierz swój nośnik USB.
     4. Kliknij **SELECT** i wskaż plik `solar_diy_20260428.iso`.
     5. Pozostaw domyślne ustawienia (GPT/UEFI, chyba że sprzęt wymaga innych).
     6. Kliknij **START** i potwierdź wyczyszczenie USB.
     7. Poczekaj na status **READY**.
   - **Linux (GUI: balenaEtcher):**
     1. Uruchom balenaEtcher.
     2. Kliknij **Flash from file** i wybierz `solar_diy_20260428.iso`.
     3. Kliknij **Select target** i wybierz pendrive.
     4. Kliknij **Flash** i poczekaj na zakończenie.
   - **Linux (CLI: `dd`):**
     1. Zidentyfikuj urządzenie USB (np.): `lsblk`.
     2. Odmontuj partycje USB (np.): `sudo umount /dev/sdX*`.
     3. Nagraj obraz: `sudo dd if=solar_diy_20260428.iso of=/dev/sdX bs=4M status=progress oflag=sync`.
     4. Opróżnij bufory: `sync`.
     5. Bezpiecznie odłącz pendrive.
   - **macOS (Terminal):**
     1. Znajdź dysk USB: `diskutil list`.
     2. Odmontuj dysk: `diskutil unmountDisk /dev/diskN`.
     3. Nagraj obraz: `sudo dd if=solar_diy_20260428.iso of=/dev/rdiskN bs=4m`.
     4. Poczekaj na zakończenie polecenia, następnie wykonaj: `sync`.
     5. Wysuń USB: `diskutil eject /dev/diskN`.
5. **Podłącz USB** do urządzenia docelowego.
6. **Uruchom z USB** (menu bootowania BIOS/UEFI).
7. **Uruchom instalator** i postępuj zgodnie z instrukcjami na ekranie.
8. Utrzymuj połączenie Ethernet przez cały czas instalacji.
9. Po zakończeniu instalacji wyjmij USB i uruchom system z dysku SSD.
