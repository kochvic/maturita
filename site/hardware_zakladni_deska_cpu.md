# Hardware - Základní deska, CPU

## Co je to hardware?
Jsou to vlastně všechny fyzický komponenty do počítače.
## Jaký jsou komponenty?
### Napájecí zdroj
  Nejdůlěžitější je vlastně **Napájecí zdroj**\
  Napájecí zdroj počítače *(PSU - Power Supply Unit)* je zařízení, sloužíci ke zpracování střídavého napětí dodávaného ze sítě.

    V různých zemích jsou různé rozpětí Vatů.
          1. v Americe, Japonsku a Taiwanu jsou 100-127V/50hz
          2. Ve zbytku světa 230V/50hz
Některé zdroje mají přepínač pro změnu vstupní napětí mezi **230V** a **115V**, ostatní se automaticky přizpůsobí jakémukoliv napětí v tomto rozsahu\
Ke zpracování střídavého napětí dodávaného ze sítě | na ústalené, malé, stejnosměrné napětí\
3 napajeci vetve *(+3,3V, 5V, 12 V)*   
  - Servery *(skutečné servery, ne doma postavené)* jedou jen na 12V, menší napětí se mění na desce *(kvůli účinnosti)*

80 Plus
  - Severoamerické sdružení prosazující vyšščí energetickou účinnost počítačových strojů *(PSU)*
      * Bronze (85)
      * Silver (87)
      * Gold (90)

### Počítačová skříň (Case)
- Skříň je důležitá abychom jsme měli kam to dát, mít to naskádané na sobě vedle monitoru to není úplně idealní. *(ale nějací fanatici to dělají)*
- Základem je plocha pro uložení **základní desky** patřičného rozměru.
- Obvykle je skříň univerzální pro jeden typ základní desky, například **ATX** *(Advanced Technology Extended)* a jeho varianty (**micro ATX, ATX, DTX, mini ATX, flex ATX**)
- **Rozměry** základní desky odpovídají rozmístění upevňovací lišty pro rozšiřujíci karty.
- Skříňe se vyrábějí v rozných velikostech vyhotovených pro různé typy základnách desek. Z hlediska použití se skříňe dělí na dva základní typy
    * Naležato (Desktop)
    * "Nastojato" (Tower)
    * "Vedle monitoru" (Open Bench)

### Procesor (CPU)
- Procesor *(Central Processing Unit, zkratka CPU)* je v informatice **základní součást počítače**, která vykonává strojový kód spuštěného počítačového programu
- Procesor je v současnosti velmi složitý **sekvenčí integrovaný obvod umístěný na základní desce počítače**.
- Hlavní veličiny
    * Frekvence (4 Ghz)
    * Počet jader
    * Technologie 4nm
    * Energetická náročnost CPU
    * Socket
    * Cache L1 až L3
    * Stupně integrace (APU)
    * Heatsink, Heatpipe chlazení CPU

### Grafická karta
- Grafická karta je součastí počítače a stará se o **zobrazení obrazu na monitoru, grafické výpočty** atd.
- Připojena je vetšinou přes **PCI-Express slot**. *(Může být i integrována na základní desce nebo v procesoru)*
- Většinou se jedná o nejnutnější čipy, výjimečně se přidává vlastní paměť.
- Grafiky bez vlastní paměti se přestaly prodávat, dříve něž jsem se narodil.
- Jediné místo, kde to člověk dnes uvidí je v mobilní GPU *(laptopy a notebooky)*, kde se sdílí RAM s GPU
- Narozdíl od CPU, které je určené pro zpracování všeobecných instrukcí GPU je vyrobeno pro zpracování paralerních pracovních náležitostí, což veed k špatné efektivitě všeobecných výpočtů.
- CUDA *(Compute Unified Device Architecture)*
  * **hardwarová a softwarová architektura**, která umožňuje na **vybraných GPU (NVIDIA)** spouštět programy napsané v jazycích C/C++, Fortran nebo programy postavené na technologiích OpenCL, DirectCompute a jiných

### Paměť (RAM)
- RAM *(Random-Access memory, pamět s přímým přístupem)* je typ **elektronické paměti**, která umožňuje přístup k **libovolné části** v konstatním ščase bez ohledu na její fyzické umístění.
- Proto je doslovný překlad anglického "**random**" v podobě "paměť s náhodným přístupem" zavádějící a je vhodnější používat český termín **paměť s přímým přístupem (nebo libovolným přístupem)**.
- Druhy RAM
  * SDRAM
    * DDR1, DDR2, DDR3, DDR4 *(standart aktualně)*, DDR5
  * Grafické
    * GDDR3, GDDR4, GDDR5, GDDR6

### Pevný disk
- Pevný disk (zkratka HDD, anglicky hard disk drive) je zařízení, které se používá v **počítačích a ve spotřební elektronice** slouží k **dočasnému** nebo **trvalému uchovávání většího množství** pomocí **magnetické indukce**

|  | HDD (SATA/IDE(PATA))      | SSD (SATA) | NVMe M.2 |
| --- | --- | ------- | ---- |
| **Mínusy** | Pomalý, Náchylné nárazy, Spotřeba, Magnety | Omezený počet zápisů |   Omezený počet zapisů, cena |
| **Plusy** |  Super Kč/GB, Životnost | Rychlý, Nízká spotřeba | Rychlost, Nízka spotřeba |

### Základní deska
- Základní deska (motherboard, mainboard) je **základním hardware počítačů**
- Hlavním účelem je **propojit jednotlivé součástky počítače do fungujícího celku a poskytnout jim elektrické napájení**
- Postupem času se funkce základní desky rozšírovala v tom, že sama začínala **obsahovat** některé **součástky počítače**, které se do ní dříve musely zapojovat zvlášť.

### CD/DVD/BD mechanika
- V součastné době jsou **CD, DVD A BD** mechaniky pro počítač volitelná komponenta, bet které jste schopni počítač používat
- Dříve se tyto mechaniky používali hlavně pro
    * instalaci programů
    * instalace operačního systému
    * poslech hudby či sledovaní serialů/filmů
- Dnešní době vysokorychlostního internetu se používají spíše už je na vypalovaní a zálohu fotek a různých dat, které chcete mít zálohované mimo počítač na pevném médiu
