# Solar DIY ISO / Solar DIY ISO

[English](#english) | [Polski](#polski)

---

<a name="english"></a>
## 🇺🇸 English

Solar DIY ISO is a custom installer image that allows you to run **Solar DIY EMS** on your **own device**.

This ISO is built on **Ubuntu 24.04.4 LTS Server**.

Solar DIY EMS is based on the Solar Cube EMS solution ([solarcube.io](https://solarcube.io)).
When following Solar Cube documentation, replace these URLs as follows:

- `https://solarcube.local` → `https://solardiy.local`
- `https://solarcube.local:5443` → `https://solardiy.local:5443`

### 💾 Download
The link below is masked and configured to start the browser download directly.

- **ISO download:** [Download ISO](https://roygard-my.sharepoint.com/:u:/g/personal/rafal_solarcube_io/IQAASs6CcIz3R6QdQtlSOwgyAevzRHeOiVP2rAf5yO-9SAw?e=w2v57V&download=1)
- **Version:** `0.1.0`
- **Filename example:** `solar-diy-v0.1.0.iso`
- **Format:** ISO
- **SHA256 checksum:** `cf3c3bef31847a5f9bdbfa73561586dd66177bcbcf2d1a421ceaccc7434f7241`

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
   - Linux:
     ```bash
     sha256sum solar-diy-v0.1.0.iso
     ```
   - macOS:
     ```bash
     shasum -a 256 solar-diy-v0.1.0.iso
     ```
   - Windows PowerShell:
     ```powershell
     Get-FileHash .\solar-diy-v0.1.0.iso -Algorithm SHA256
     ```
3. **Prepare a USB drive** (minimum 8 GB; all existing data will be erased).
4. **Write ISO to USB** (detailed by OS):
   - **Windows (Rufus):**
     1. Download and open [Rufus](https://rufus.ie).
     2. Insert USB drive.
     3. In **Device**, select your USB drive.
     4. Click **SELECT** and choose `solar-diy-v0.1.0.iso`.
     5. Keep default settings (GPT/UEFI unless your hardware requires otherwise).
     6. Click **START** and confirm USB erase.
     7. Wait until status is **READY**.
   - **Linux (GUI: balenaEtcher):**
     1. Open balenaEtcher.
     2. Click **Flash from file** and select `solar-diy-v0.1.0.iso`.
     3. Click **Select target** and choose USB drive.
     4. Click **Flash** and wait for completion.
   - **Linux (CLI: `dd`):**
     1. Identify USB device (example): `lsblk`.
     2. Unmount USB partitions (example): `sudo umount /dev/sdX*`.
     3. Write image: `sudo dd if=solar-diy-v0.1.0.iso of=/dev/sdX bs=4M status=progress oflag=sync`.
     4. Flush buffers: `sync`.
     5. Safely remove USB.
   - **macOS (Terminal):**
     1. Find USB disk: `diskutil list`.
     2. Unmount disk: `diskutil unmountDisk /dev/diskN`.
     3. Write image: `sudo dd if=solar-diy-v0.1.0.iso of=/dev/rdiskN bs=4m`.
     4. Wait for command to finish, then run: `sync`.
     5. Eject USB: `diskutil eject /dev/diskN`.
5. **Insert USB** into the target machine.
6. **Open BIOS/UEFI** (`DEL`, `F2`, `F10`, or `ESC`, depending on device).
7. **Set USB as first boot device** and reboot.
8. **Start installer** and follow on-screen steps.
9. After installation, remove USB and boot from internal SSD.

---

<a name="polski"></a>
## 🇵🇱 Polski

Solar DIY ISO to niestandardowy obraz instalacyjny, który pozwala uruchomić **Solar DIY EMS** na **własnym urządzeniu**.

To ISO zostało zbudowane na bazie **Ubuntu 24.04.4 LTS Server**.

Solar DIY EMS działa na bazie rozwiązania Solar Cube EMS ([solarcube.io](https://solarcube.io)).
Korzystając z instrukcji Solar Cube, zamieniaj adresy URL według poniższych zasad:

- `https://solarcube.local` → `https://solardiy.local`
- `https://solarcube.local:5443` → `https://solardiy.local:5443`

### 💾 Pobieranie
Poniższy odnośnik jest ukryty pod etykietą i skonfigurowany tak, aby po kliknięciu od razu rozpocząć pobieranie w przeglądarce.

- **Pobieranie ISO:** [Pobierz ISO](https://roygard-my.sharepoint.com/:u:/g/personal/rafal_solarcube_io/IQAASs6CcIz3R6QdQtlSOwgyAevzRHeOiVP2rAf5yO-9SAw?e=w2v57V&download=1)
- **Wersja:** `0.1.0`
- **Przykładowa nazwa pliku:** `solar-diy-v0.1.0.iso`
- **Format:** ISO
- **Suma kontrolna SHA256:** `cf3c3bef31847a5f9bdbfa73561586dd66177bcbcf2d1a421ceaccc7434f7241`

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
   - Linux:
     ```bash
     sha256sum solar-diy-v0.1.0.iso
     ```
   - macOS:
     ```bash
     shasum -a 256 solar-diy-v0.1.0.iso
     ```
   - Windows PowerShell:
     ```powershell
     Get-FileHash .\solar-diy-v0.1.0.iso -Algorithm SHA256
     ```
3. **Przygotuj pendrive USB** (minimum 8 GB; wszystkie dane zostaną usunięte).
4. **Wgraj ISO na USB** (dokładnie dla każdego systemu):
   - **Windows (Rufus):**
     1. Pobierz i uruchom [Rufus](https://rufus.ie).
     2. Podłącz pendrive USB.
     3. W polu **Device** wybierz swój nośnik USB.
     4. Kliknij **SELECT** i wskaż plik `solar-diy-v0.1.0.iso`.
     5. Pozostaw domyślne ustawienia (GPT/UEFI, chyba że sprzęt wymaga innych).
     6. Kliknij **START** i potwierdź wyczyszczenie USB.
     7. Poczekaj na status **READY**.
   - **Linux (GUI: balenaEtcher):**
     1. Uruchom balenaEtcher.
     2. Kliknij **Flash from file** i wybierz `solar-diy-v0.1.0.iso`.
     3. Kliknij **Select target** i wybierz pendrive.
     4. Kliknij **Flash** i poczekaj na zakończenie.
   - **Linux (CLI: `dd`):**
     1. Zidentyfikuj urządzenie USB (np.): `lsblk`.
     2. Odmontuj partycje USB (np.): `sudo umount /dev/sdX*`.
     3. Nagraj obraz: `sudo dd if=solar-diy-v0.1.0.iso of=/dev/sdX bs=4M status=progress oflag=sync`.
     4. Opróżnij bufory: `sync`.
     5. Bezpiecznie odłącz pendrive.
   - **macOS (Terminal):**
     1. Znajdź dysk USB: `diskutil list`.
     2. Odmontuj dysk: `diskutil unmountDisk /dev/diskN`.
     3. Nagraj obraz: `sudo dd if=solar-diy-v0.1.0.iso of=/dev/rdiskN bs=4m`.
     4. Poczekaj na zakończenie polecenia, następnie wykonaj: `sync`.
     5. Wysuń USB: `diskutil eject /dev/diskN`.
5. **Podłącz USB** do urządzenia docelowego.
6. **Wejdź do BIOS/UEFI** (`DEL`, `F2`, `F10` lub `ESC` — zależnie od sprzętu).
7. **Ustaw bootowanie z USB** jako pierwsze i uruchom ponownie komputer.
8. **Uruchom instalator** i postępuj zgodnie z instrukcjami na ekranie.
9. Po zakończeniu instalacji wyjmij USB i uruchom system z dysku SSD.
