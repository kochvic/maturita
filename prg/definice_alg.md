# Definice algoritmů, formy zápisu, asymptotická složitost

### Definice algoritmů
**Algoritmus** je posloupnost konečných kroků, který vede k žádanému cíli
- Vlastnosti algoritmu:
    - Konečnost
    - Determinovanost
    - Obecnost
    - Universálnost
    - Efektivita
    - Resultativnost

Pojem algoritmu se nejčastěji objevuje při programovaní, kdy se jím myslí teoretický princip řešení problému
Z předchozích aktivit nám vyplynuly některé podmínky, které musí pracovní postup splňovat, abychom ho prohásili za algoritmus:
    1. Musí být popsáný. Jinak se nemáme o čem bavit.
    2. Musí nám dávat nějaký výsledek. Jinak se vlastně nemáme proč o něm bavit.
    3. Musí být složen z instrukcí tak základních, že je vykonavatel umí provést bez dalšách otázek či přemýšlení. Nejde říct "slož čepici", to by mohlo dopadnout všelijak. Pokud vykonavatel rozumí pojmům jako "na výšku" či "vodorovné osy" lze možná říct "otoč papír přitiskni ke stolu". A to pořád něco předpokládá např. že vykonavatel pozná kratší stranu papíru (a samotný papír).
    4. V každém okamžiku musí být postupem dané, kterou instrukcí se bude pokračovat. Nesmí to zaviset na svobodém rozhodnutí vykonavatele. Postup se také nesmí "zaseknout" kvůli neočekávaným okolnostem. Vždy musí být jasné, co dělat dál (nebo že je konec).

### Formy zápisu
  - Klasický v mateřském jazyce - slovní
  - Vývojové diagramy (strukturogramy) - grafická
  - Pseudojazyky (programovací jazyky)

**Vývojové diagramy**
  - Provedení
  - Mezní značky
  - Větvení
  - Cyklu
  - I/O

**Asyptotická složitost**
Asymptotická složitost je nástrojem k porovnávání efektivity algoritmů. Složitost vyjadřuje, jak roste náročnost algoritmu (doba výpočtu nebo potřebná poměť) s roustoucím množstvím vstupních dat. Především se složitost počítá tzv. asymptotický a během "výpočtu" se zanedbávájí nepodstatné členy (např. aditivní a multiplikativní konstanty).

**Typy asymtotické složitosti seřazené od nejlepší k nejhorší**
  1. **Konstatní** složitost *(Landauova notace = 0(1))*
  2. **Logaritmická** složitost, *O(log n)*
  3. **Lineární** složitost, *O(n)*
  4. **Lineárně logaritmická** složitost, *O(n.log n)*
  5. **Kvadratická** složitost, *O(n^2)*
  6. **Exponenciální** složitost, *O (k^n)*
  7. **Faktoriální** složitost, *O(n!)*
