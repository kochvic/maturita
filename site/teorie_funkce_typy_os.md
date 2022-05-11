# Teorie OS - funkce OS, typy OS
- Opeční systém je zakldní software každého počítače, je to program, který nám umožňuje počítač ovládat, tvoří rohraní mezi programy a hardwarem, organizuje přístup a datům, spouštění aplikací, řídí jejich průběh a přiřazuje jim hardwarové prostředky *(přístup k CPU, místo v paměti, přístup k periferiím, k datům)*.

### Funkce
- Správa procesů
- Správa paměti
- Správa informací *(souborový systém)*
- Synchronizace
- Správa ovladačů atd.
  * Řídí a spravuje přístup ke zdrojovým vypočetního systému
  * Organizuje přistup k datům *(zamezení neoprávněného přístupu)*
  * Organizuje přistup k datům *(jejich přípravu, plánovaní a průbeh tak, aby byla zajištěna maximální efektivita jejich zpracovaní)*
  * Řídí zpracovaní úloh *(jejich přípravu, plánovaní a průběh tak, aby byla zajištěna maximální efektivita jejich zpracovaní)*
  * Podporuje komunikaci s uživatelem *(provádění uživatelem zadaných příkazů)*
  * **Rozhraní**: existují dvě formy
      * **GUI (Graphical user interface)**
      * **CLI (Command line interface)** (*textové rozhraní*)
        * MS-DOS
        * Většina GUI systému ale má možnost používaní CLI

### Typy OS
- Rozdělnení
    - Mobilní
      * Android, iOS
    - Desktopové
      * MS Windows
      * ChromeOS
      * MacOS
      * GNU/Linux
    - Komerční
      * MS Windows
    - Non license
      * GNU/Linux
      * MacOS
        * *I když MacOS je bez license, tak ale používaní mimo Applem vytvořeným hardwarem, porušuje Terms of service*
    -  OS Aktivních prvků sítě
      * Router OS
      * Cisco OS

### Vlastnosti

- MS-DOS
  * žádné prostředky ochrany souborů a disků
  * neumožňuje běh více procesů najednou
- Windows
  * Multitasking
    * možnost paralelního běhu několika procesů
- GNU/Linux
  * možnost zpracovávat požadávků
  * více uživatelů příhlášených do OS
  * všechno je soubor
  * Open-source
- MacOS
  * Dnešní době nemá nic specialního kromě značky Apple která je celosvětově známá
  * Menší podobnost s GNU/Linux *(Velmi malá podobnost)*

### Správa procesů
  - Stavy procesů
    * Aktivní
    * Čekající
    * Připraven
  - Nepreemtivní vs Preemtivní multitasking
  - Plánovaní CPU
    * Maximální využití CPU
    * Maximální odbavení úloh za jednotku času
    * Maximalní spravedlnost
  - FCFS, SJF, SRT, RR
    * FCFS - konvojový efekt
    * SJF - stárnutí
    * SRT - předchází stárnutí
    * RR - maximální spravedlnost, kdy nejhorší doba odezvy je definována jako (n-1)*q, kde n je počet procesů a q vypovída o rychlosti procesoru
  - Prioritní plánovaní

### Správa paměti
  - Úlohy správy paměti
    * Přidělovat paměť
    * Odebírat paměť
    * Chrání paměť
    * Udržovat informace o paměti
  - Vývoj
    * Přidělení jednoho souvislého bloku paměti
      * Limitování velikostí RAM
      * Neumožňuje multitasking (pouze jedna proces v paměti)
      * Plýtvá paměti
      * Nároky na provoz
        * mezní registr
        * 1/0 pokud je paměť volná či ne
    * Statické / dynamické rozdělnení po sekcí
      * Limitování velikostí RAM
      * Fragmentace (interní tak externí) - menší plýtvání paměti
      * Nároky na provoz (o každé sekci musím mít informaci, zda-li je obsazená nebo volná + 2x mezní registr a jeden relokační registr pro každou sekci)
    * Stránkování
      * Limitováno velikosti RAM
      * Interní fragmentace zůstala, ale odpadla externí a potřeba realokovat
    * Stránkování na žádost
      * Zavádí pojem virtuální paměť -> eliminuje limit velikosti RAM
    * Segmentace paměti
        * Rozdělení paměti na segmenty
          * Data
          * Data instrukcí
          * Zásobník (LIFO)

### Souborový systém          
  - Má za úkol uchovávat data na persistentím nevolatilním ve strukturované podobě
  - Soubor - data na disku, která k sobě svým významem patří
  - FS (File system)
    * Data (samotné informace)
    * Metadata
      * Informace o autorovi
      * Datumy vzniku
      * Změny
      * Atributy
      * Data omezení přístupu
  - Žurnál
    * Úsek disku, do kterého se zapisují činnosti s daty, pokud je činnost dokončena *(žurnál se vyčistí)*
  - Typy
    * FAT32 (MS, univerzalní)
      * Maximalní velikost souboru 4GB
    * NTFS (MS, pouze pro Windows)
      * ACL, EFS, diskové kvóty, transakce, symbolické linky
    * ext2, ext3, ext4, btrfs, lvm (GNU/Linux)
      * Snapshot, RAID
    * HFS, HFS+  
