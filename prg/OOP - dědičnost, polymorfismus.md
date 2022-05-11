**11) OOP - dědičnost, polymorfismus**

**Dědičnost:** 
-jedná se o jev, kdy vytváříme novou třídu na základě nějaké již existující
-takto vytvořená třída se označuje jako přímá podtřída (přímý potomek)
-původní třída se nazývá základní třída (rodičovská třída), nebo někdy také nadtřída třídy odvozené

- Klíčové slovo pro odvození dědičnosti - extends
- Jednoduchá dědičnost - můžeme dědit maximálně z jedné třídy
- Do potomka se **nedědí** datové členy a metody které jsou označeny jako private, konstruktory
- Datové členy a metody upravujeme nebo přidáváme nové
- Pokud chceme chování metody upravit - nesmíme změnit signaturu metody (@Override)
- Odkaz na rodiče - super.neco nebo konstruktor super()
- final – blokace modifikace chování metody i datového členu (konstanta)

**Polymorfismus:**
-funguje pouze u objektů odvozených tříd nebo v rámci implementace rozhraní
-odkaz na objekt odvozené třídy musí být uložen v proměnné typu přímé nebo nepřímé základní třídy

Pes alik = new Pes(); //OK

Zvire alik = new Pes(); //OK

Object alik = new Pes(); //OK


-metoda pro využití polymorfizmu musí být členem základní třídy (typu proměnné, kterou používáte) a také musí být členem třídy, které je daný objekt součástí (odkazuje na něj proměnná, kterou používáte)

- Abstraktní třída
- Není žádné klíčové slovo, nebo něco podobného
- Jediné co se musí zabezpečit, aby vše fungovalo aby byla stejná metoda, respektive její signatura ve všech zúčastněných třídách (v hierarchii dědičnosti nebo v implementaci rozhraní)


