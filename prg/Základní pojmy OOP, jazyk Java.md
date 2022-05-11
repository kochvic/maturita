**9) Základní pojmy OOP, jazyk Java**


**Java**

- je [objektově orientovaný](https://cs.wikipedia.org/wiki/Objektov%C4%9B_orientovan%C3%A9_programov%C3%A1n%C3%AD) [programovací jazyk](https://cs.wikipedia.org/wiki/Programovac%C3%AD_jazyk)
- Je implementokompilovaný jazyk
- jde o jeden z nejpoužívanějších programovacích jazyků na světě
- díky své přenositelnosti je používán pro programy, které mají pracovat na různých systémech počínaje čipovými kartami, přes mobilní telefony a různá zabudovaní zařízení, aplikace počítače až po rozsáhlé systémy pracující na řade spolupracujících počítačů po celém světě

**Co je to OOP**

-objektově orientované programování je specifické programovací paradigma, které ho odlišilo od původního imperativního
-výkonný kód je v objektovém programování přidružen k datům (metody jsou zapouzdřeny v objektech), což umožňuje snadnější přenos kódu mezi různými projekty (abstrakce a zapouzdření)
-propojení umožnilo zavést dědičnost, ale kvůli zjednodušení si vyžádalo zavedení polymorfismu

Základní pojmy v objektově orientovaném programování jsou **dědičnost, zapouzdření, polymorfismus, třídy, objekty**, **proměnné**, **metody** a **konstruktory.**

**Dědičnost**
-je způsob, jak ustanovit vztah mezi objekty
-v třídové dědičnosti, kde jsou objekty definované třídami, mohou třídy zdědit atributy a chování od předem existujících tříd, které se nazývají rodičovské třídy
-výsledné třídy jsou nazývány potomky

**Zapouzdření**
-může být vysvětleno jako zabalení dat a metod do jedné komponenty
-umožňuje ukrytí atritbutů a metod v objektu pomocí stavby zdi, která brání kód proti nechtěným změnám

**Polymorfismus**
-vlastnost jazyka, která umožňuje:

- Jednomu objektu volat jednu metodu s různými parametry
- Objektům odvozeným z různých tříd volat tutéž metodu se stejným významem v kontextu jejich třídy
- Přetěžování operátorů neboli provedení rozdílné operace v závislosti na typu operandů
- Jedné funkci dovolit pracovat s argumenty různých typů

**Třída:** 
-definice objektů, které nesou stejné vlastnosti
-např. všechny objekty ve třídě *Person* mají vlastnost *name,* ale tato vlastnost má pro různé lidi jinou hodnotu – lidé mají různá jména

**Objekt:**
-objekt je instancí třídy
-je jeden konkrétní jedinec příslušné třídy
-např. objekt panProfesor typu Person má vlastnost name s hodnotou „Jan Novák“
` `-objekt může být buď **proměnná** nebo **metoda**

**Proměnná třídy:** 
-uchovává určitou informaci při běhu programu
-může nabývat informací, které se nazývají hodnota

**Metoda:** 
-je podprogram, který primárně pracuje s proměnnými mateřského objektu (instanční metoda)
-může mít další parametry (přetěžování metod – mají stejný název, ale liší se počtem nebo typem, podle zadané hodnoty se zavolá metoda)
-může ve svém kódu deklarovat lokální proměnné
-každá metoda se musí ve své třídě deklarovat

**Konstruktor:** 
-speciální metody volané při vytváření nových instancí dané třídy
-konstruktory lze volat jen ve spojení s operátorem *new* k vytvoření nové instance třídy
-jestliže konstruktor nevytvoříme, vytvoří se implicitní konstruktor
-musí se jmenovat totožně s názvem třídy

**JDK**
-Java Development Kit je produkt Oracle Corporation, který obsahuje soubor základních nástrojů pro vývoj aplikací pro platformu Java

**JRE**
-Java Runtime Enviroment umožňuje např. Hraní online her, chatování, kalkulaci hypotéčních úroků, zobrazování 3D obrázků a mnoho dalšího

**JVM**
-Java Virtual Machine je sada počítačových programů a datových struktur, který využívá modul virtuálního stroje ke spuštění dalších PC programů a skriptů vytvořených v jazyce java
