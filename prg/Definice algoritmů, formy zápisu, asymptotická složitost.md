`             `![](Aspose.Words.c89d2542-c82b-43e6-bc35-5f7fbf1fce77.001.png)

**Definice algoritmů**

**Algoritmus** je posloupnost konečných kroků, která vede k žádanému cíli.

Vlastnosti algoritmu:

- Konečnost
- Determinovanost
- Obecnost
- Universálnost
- Efektivita
- Resultativnost

Pojem **algoritmu** se nejčastěji objevuje při programování, kdy se jím myslí teoretický princip řešení problému 

Z předchozích aktivit nám vyplynuly některé podmínky, které musí pracovní postup splňovat, abychom ho prohlásili za algoritmus:

1. Musí být popsaný. Jinak se nemáme o čem bavit.
1. Musí nám dávat nějaký výsledek. Jinak se vlastně nemáme proč o něm bavit.
1. Musí být složen z instrukcí tak základních, že je vykonavatel umí provést bez dalších otázek či přemýšlení. Nejde říct „slož čepici“, to by mohlo dopadnout všelijak. Pokud vykonavatel rozumí pojmům jako „na výšku“ či „vodorovná osa“, lze možná říct „otoč papír na výšku a přelož podle vodorovné osy“. Možná je ale nutné říct dokonce „otoč papír kratší stranou k sobě, vezmi nejvzdálenější okraj, přilož na nejbližší okraj a papír přitiskni ke stolu.“ A to pořád něco předpokládá, např. že vykonavatel pozná kratší stranu papíru (a samotný papír).
1. V každém okamžiku musí být postupem dané, kterou instrukcí se bude pokračovat. Nesmí to záviset na svobodném rozhodnutí vykonavatele. Postup se také nesmí „zaseknout“ kvůli neočekávaným okolnostem. Vždy musí být jasné, co dělat dál (nebo že je konec).

**Formy zápisu**

- Klasický v mateřském jazyce - slovní
- Vývojové diagramy (strukturogramy) - grafická
- Pseudojazyky (programovací jazyky)

Vývojové diagramy

- Provedeni
- Mezní značky
- Větvení
- Cyklu
- I/O

![](Aspose.Words.c89d2542-c82b-43e6-bc35-5f7fbf1fce77.002.png)![](Aspose.Words.c89d2542-c82b-43e6-bc35-5f7fbf1fce77.003.png)

**Asymptotická složitost**

Asymptotická složitost je nástrojem k porovnávání efektivity algoritmů. Složitost vyjadřuje, jak roste náročnost algoritmu (doba výpočtu nebo potřebná paměť) s rostoucím množstvím vstupních dat. Především se složitost počítá tzv. asymptoticky a během "výpočtu" se zanedbávají nepodstatné členy (např. aditivní a multiplikativní konstanty).

![](Aspose.Words.c89d2542-c82b-43e6-bc35-5f7fbf1fce77.004.png)

Typy asymtotické složitosti seřazené od nejlepší k nejhorší:

1. Konstantní (Landauova notace = O(1))
1. Logaritmicka složitost O(log n)
1. Lineární složitost O(n)
1. Lineárně logaritmická O(n.log n)
1. Kvadratická složitost O(n2)
1. Exponenciální složitost O(kn)
1. Faktoriální složitost O(n!)
