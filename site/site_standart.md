# Počítačové sítě - síťové standardy
ISO – Internation standart organization

IEEE – Institut of Electrical and Electronics Engineers
## IEEE 802.3 Ethernet (odkazovat se na otázku 11, 12)
- nejrozšířenější
- sběrnicová, **hvězdicové** topologii
- koaxiální kabel, **TP, optická vlákna**
- vznikají zde kolize (kolizní domény)
- částečné řešení kolizí je CSMA/CD

**Kolize**

kolize je stav, kdy dva počítače se snaží současně komunikovat (skákání do řeči)

**Kolizní doména**

v jaké oblasti může docházet ke kolizím. Hub rozšiřuje kolizní doménu. Switch (Router) kolizní doménu přerušují.


**CSMA (Carrie Sense Multiple Access)**

dochází k naslouchání na lince, jestli je používána ke komunikace nebo ne. V případě, že linka volná, tak zahájí komunikaci. Problém je, pokud naslouchá více stojů, poté začnou naráz komunikovat = dojde ke kolizi (čím více je strojů v kolizní doméně, tím častěji dochází ke kolizi)

**CD (collise detection)**

pokud dojde ke kolizi, tak je detekována a všem zúčastněným stanicím je poslána zpráva o tom, že došlo ke kolizi a zastaví vysílání.

Opětovné vysílání nastává za náhodný.

- Fast Ethernet (100BaseT)
- Gigabitový Ethernet (1000BaseTX)
- 10Gigabitový Ethernet (10GBaseT)

první číslo	= značí přenosovou rychlost (např: 100Mb/s) 100megabitů/sekunda

base		= přenos v základním pásmu

označení vodiče= T (kroucenou dvojlinku), F,L(optické vlákno)

## IEEE 802.5 Token ring
- podstatně méně používaná (téměř zaniklá)
- jedině kruhová topologie
- TP, optika (FDDI)
- nevznikají žádné kolize (důvodem speciálního druhu komunikace)
- používá metodu token passing (předávání tokenu)

Problémy tohoto standardu:

- porušení kruhu (lokalizace závady)
- ztráta token
- stoupající počet zařízení zapojených do kruhu
- 2 vodiče na jedno zařízení

## IEEE 802.11 Bezdrátové sítě (viz otázka 16)
