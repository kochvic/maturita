# Počítačové sítě - pasivní a aktivní prvky sítě
**Propojovací pasivní prvky**

Pro realizaci sítě je důležité propojit stanice. Při vybírání vhodného vodiče informace je potřeba sladit jeho vlastnosti s vlastnostmi propojovaných zařízení (stanice, switche, routry aj.)

**Parametry kabelů**

Podle těchto parametrů charakterizujeme jednotlivé typy kabelů.

- **Přenosová rychlost:** jedná se o rychlost přenosu dat, která se uvádí Mb/s, u menších sítí je přenosová rychlost 10 - 100 Mb/s a u rychlejších sítí je to až v Gb/s.
- **Útlum:** útlum je míra zeslabení signálu při průchodu kabelem, uvádí se v dB.
- **Odolnost vůči elektromagnetickému rušení**
- **Impedance:** je to odpor, které kabel představuje pro připojené zařízení, impedance kabelu i zařízení by měli být shodné, uvádí se ohmech.
- **Přeslech:** vzájemné ovlivnění více vodičů mezi sebou. Měří se obvykle pro každou dvojici vodičů a udává se v dB.

**Druhy kabelů**

Koaxiální kabel

Kroucená dvojlinka

Optický kabel

**Koaxiální kabel**

Je to nejstarší typ kabelu používaný v počítačových sítích a měl velký vliv na rozvoj počítačových sítí. (LAN) Základem je měděný vodič který je obalen plastovou izolací a ta je opletena stíněním. Vše je ve vnějším obalu který je z plastu.

**Druhy:**

**Tlustý koaxiální kabel (10 mm) -** špatně se s ním manipuluje, má dobré elektrické vlastnosti.

**Tenký koaxiální kabel –** Manipuluje se s ním lépe než s tlustým kabelem ale má horší elektrické vlastnosti.

**Konektory:**

**BNC –** slouží k připojení ke stanici

**T-Konektor**

**Terminátor –** Zabraňuje odrazům signálu na volném konci

Nejrozšířenější kabely jsou ethernetovské které mají impendanci 50 ohmů.

Nejčastěji se používají pro zapojení počítačů do sběrnicové topologie. V počítačových sítích se už ale moc nepoužívají jsou hlavně v kabelových televizích.

**Kroucená dvojlinka**

Nejrozšířenější kabel v lokálních sítích.

Skládá se ze čtyř dvojic zkroucených vodičů, uložených v izolačním obalu.

Díky vzájemnému zkroucení vodičů ve dvojicích je snížena možnost ovlivnit jeden vodič druhým.

**Kategorie:**

**Kategorie 1 –** Není určen k datovým přenosům, používá se třeba u telefonních rozvod. Přenosová rychlost do 1Mbit/s. Vhodné např. pro analogové rozvody, ISDN atd.

**Kategorie 2 –** Určeno pro přenos dat s maximální šířkou pásma 1,5 MHz. Používá se pro digitální přenos zvuku hlavně pro rozvody IBM Token ring. Přenosová rychlost 4Mbit/s.

**Kategorie 3 –** Určeno pro rozvod dat a hlasu šířkou pásma 16 MHz a přenosovou rychlostí do 10 Mbit/s. Využívá datových přenosů 10Base-T Ethernet.

**Kategorie 4 –** Určeno pro přenos dat v síti Token ring se šířkou pásma 20Mhz a přenosovou rychlostí do 16Mbit/s.

**Kategorie 5 –** Pracuje v šířce pásma do 100MHz. Přenosová rychlost do 100Mbit/s, při využití všech vláken(8) až 1 Gbit/s. Nyní je nahrazen standardem 5E.

**Kategorie 5E –** Vyžaduje nové způsoby měření parametrů a v některých parametrech je přísnější. Cílem je provozovat 1 Gbit/s.

**Kategorie 6 –** Šířka pásma je 250 Mhz. Využívá se pro ultrarychlé páteřní aplikace v oblasti lokálních sítí. Nejpopulárnější kabeláž pro nově budované rozvody.

**Kategorie 6a –** Šířka pásma 500MHz. Používá se pro zvláště rychlé páteřní aplikace v lokálních sítích. Využívá se i pro 10GBASE-T Ethernet (10 Gbit/s)

**Kategorie 7 –** Šířka pásma do 600 - 700 MHz. Kabel je plně stíněný - každý pár je stíněn zvlášť Al fólií a kabel sám má ještě celkový štít. Tato „plně stíněná“ konstrukce má ale za následek větší váhu, větší vnější průměr a menší ohebnost kabelu než UTP nebo STP. Používá se pro přenosy plné šířky videa, teleradiologii. V současné době se provádí první pokusy s tímto standardem.

**Nestíněná - UTP** (Unshielded TP) – zkroucené páry uloženy do plastické izolace.

**Stíněná - STP** (Shielded TP) – kolem párů je kovové opletení, které zvyšuje ochranu proti vnějšímu elektromagnetickému rušení.

V běžných provozech se používá nestíněná dvojlinka, stíněná se používá pouze tam, kde je vyšší úroveň elektromagnetického rušení.

Kroucená dvojlinka se používá především pro zapojení stanic do hvězdy přes switch.

Pro připojení k PC slouží dvojlinka s konektorem RJ-45, přenos dat až 1000 Mb/s

Přímé nebo křížené zapojení standardu A či B

B = bílo-oranžová, oranžová, bílo-zelená, modrá, bílo-modrá, zelená, bílo-hnědá, hnědá

A = prohodit zelené a oranžové barvy

**Optický kabel**

Je tvořen jedním nebo více optickými vlákny, které jsou spolu uloženy ve vnějším obalu.

Data jsou přenášena světelnými impulsy v průsvitných vláknech.

Při vedení světelného signálu se využívá jevu úplný odraz, ke kterému dochází na rozhraní jádra a pláště.

**Druhy vláken:**

**Mnohovidová -** při průchodu vláknem je světelná energie rozdělena na více paprsků, na konec kabelu dojdou jednotlivé vidy s časovým odstupem, což vede ke zkreslení signálu. Tyto kabely jsou levnější, ale mají horší optické vlastnosti. – Jejich jádro má průměr 50, 62.5 nebo 100 mikrometrů. Výhodou mnohovidových vláken je relativně nízká cena, velká numerická apertura a možnost buzení luminiscenční diodou (LED).

**Jednovidová –** prochází pouze jeden paprsek bez lomů. Jádro o velmi malém průměru (8-10 mikromů), lepší optické vlastnosti, vyšší přenosová kapacita, přenášejí na větší vzdálenost (až 5km), ale jsou dražší.

**Konektory:**

ST konektor, SC konektor

Přenosová rychlost optických kabelů se pohybuje až k mnoha gigabitům za sekundu. Umožňují přenos signálu na velké vzdálenosti. Odolnost vůči elektromagnetickému rušení, nízké ztráty a vysoká přenosová rychlost.

Realizace optické sítě je finančně nákladná a technicky náročná.

**Síťové karty**

Slouží ke komunikaci počítače a kabelu podle pravidel která jsou daná síťovým standardem.

Převádí data z podoby které rozumí počítač, tak aby mohla být přenesena médiu.

Dnes jsou síťové karty součástí základní desky PC.

Jsou tedy integrované v základní desce, nebo do sběrnice PCI.

Nejrozšířenější přenosová technologie je Ethernet.

**MAC adresa**

6Byte = 48bitová

K tomu, aby bylo možné uzel v síti jednoznačně identifikovat, je potřeba přidělit mu určité označení. MAC adresa, musí být především jednoznačná v rámci sítě, která umožňuje přímou komunikaci počítačů. V rámci sítí po celém světě, které mohou být navzájem propojeny, by neměla nastat situace, kdy se vyskytnou dva či větší počet počítačů se shodnými adresami. Pokud by se vyskytly počítače se stejnými MAC adresami v různých, navzájem oddělených sítích, problém by nevznikl. Komplikace by nastaly při duplicitě MAC adres v rámci jedné sítě, ovšem vzhledem k tomu, že uživatelé mohou svůj počítač přenést a připojit do jiné sítě, je lepší jednoznačnost adres dodržet v rámci celého světa. Jednoznačnosti je pak dosaženo tím, že MAC adresa je uložena již při výrobě pevně do paměti ROM síťového adaptéru, přičemž každému adaptéru je přidělena adresa odlišná od adres všech ostatních vyrobených adaptérů.
