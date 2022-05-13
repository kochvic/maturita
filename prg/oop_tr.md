# OOP - třída, objekt a programovací jazyk

###	Třída:

Třída je předpis objektu a podle ní se objekt vytváří. Třída definuje společné vlastnosti vytvářených objektů.

Ve třídě se deklarují stavy uložené v datových polích, tj. co si objekt pamatuje, a metody, tj. co bude moci objekt vykonávat a jak.

- představuje skupinu objektů, které nesou stejné vlastnosti
- např. všechny objekty ve třídě Person mají vlastnost name, ale tato vlastnost má pro různé lidi jinou hodnotu – lidé mají různá jména

###	Objekt:
**Objekt je základní prvek OOP programu**. Má vlastnosti a poskytuje operace. Objekt má vnitřní stav, který jej popisuje a odlišuje od ostatních. Vnitřní stav se ukládá do datových polí jako záznam či proměnné různého typu. Objekt je vytvářen konstruktorem.

- je jeden konkrétní jedinec příslušné třídy
- např. objekt panProfesor typu Person má vlastnost name s hodnotou „Jan Novák“
- objekt může být buď proměnná nebo metoda
- objekt vytvoříme pomocí volaní **metody konstruktoru**


### ?????????
Dodělat: implementace – slovem class, jak se jmenuje soubor podle třídy Auto.java – class Auto, anonymní třídy – v třídě může být další třída, ale nesmí být veřejná, třída obsahuje datové členy (popisují objekt atd.), metody (manipulují s objektem, set/get metody) a konstruktory (co to je, jaké jsou pravidla, class Auto {public Auto(){} / public Auto(String z){} }

objekt je instance třídy, nový objekt vznikne kódem Auto a = new Auto(); Auto a; - reference a až v momentě, když zavolám konstruktor vznikne nové auto
