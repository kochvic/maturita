# Ukazatele a dynamická alokace paměti

# Ukazatele

•	Ukazatel (anglicky pointer) je v informatice označení pro datový typ, který slouží k uložení adresy v paměti počítače.
•	Ukazatel slouží pro zpřístupnění dat, která jsou na příslušné adrese v operační paměti uložena.
•	Ukazatel používá většina imperativních programovacích jazyků, jako např. jazyk C/C++ a Pascal.
•	V programovacích jazycích je syntaxí zápisu programu rozlišeno, zda se pracuje s hodnotou adresy ukazatele anebo s hodnotou datového prvku, na který ukazuje. V případě jazyk C/C++ je jedná o operátory * a &
•	Zvláště významný je tento datový typ v jazyku C, který definuje i tzv. pointerovou aritmetiku, díky které lze např. provést výpočet adres různých prvků v poli, nebo naopak z jejich adresy odvodit jejich index.
•	Jazyk C téměř nerozlišuje mezi ukazatelem a polem protože nemá datový typ “řetezec” takže nahrazuje jej právě ukazatelem na jeho počátek. Jinými slovy s tím pracuje jako s polem znaku.
•	V novějších programovacích jazycích, jako například Java a Python, jsou ukazatele nahrazeny referencemi na objekty, jejichž použití není tolik náchylné k základním chybám.



Předávání parametrů
 - podprogram má možnost bez ukazatelů komunikovat s kódem,
který ho zavolal pouze přes návratovou hodnotu a to není pro
velké množství problému dostačující
 -  s ukazateli můžete práci podprogramu předat i v parametrech
(například fce pro přehození obsahu dvou proměnných)

Předávání polí
  - jazyk C neumožňuje předat pole jako hodnotu – znamenalo by to
vytvořit kopie velkého množství dat.

Práce s pamětí
  - ukazatel má velikost pouze 4B (8B) a je jedno na jak velikou
adresní část ukazuje

## Deklarace ukazatele

    <datový_typ> *<indetifikátor>

Obecná deklarace se od deklarace proměnné liší pouze použítím hvězdičky před jménem proměnné.

    int a = 3;        //proměnná a se nastaví na hodnotu 3
    int *ua = &a;     //ukazatel ua se nastaví na adresu proměnné a

## Přistupovaní k datům

    int *au = 5;      //na adresu určenou ukazatelem au (proměnná a) se nastaví hodnota 5
    int ua = 3;       //chyba

Pokud chceme přistupovat k datům, na které ukazuje ukazatel, musíme použít operátor
    dereference *, jak je ukázáno na první řádce kódu výše.

V druhé řádce je sémantická chyba, kde místo hodnoty proměnné „a“ přepisujeme adresu
    uchovanou v ukazateli

# Dynamická alokace paměti

- Dynamická alokace paměti je v informatice souhrn funkcí používaných při programování pro dynamickou alokaci paměti, její správu a uvolňování.
- Správa paměti je prováděna programátorem ručně, nikoliv automaticky. Cílem je požádat jádro operačního systému o přidělení souvislého úseku operační paměti pro potřeby běžícího procesu nebo ji naopak operačnímu systému vrátit.
- Proces může paměť alokovat nebo vracet opakovaně. Po ukončení procesu je veškerá alokovaná paměť vrácena operačnímu systému k dalšímu použití.         

Lze používat **statické**, **automatické** i **dynamické** přidělování *(alokaci)* paměti.

- Staticky alokované proměnné jsou umístěny do hlavní paměti, velmi často přímo s výkonným kódem programu.
- Existují po celou dobu běhu programu, ať už jsou programem využity nebo ne. Automaticky alokované proměnné jsou alokovány do zásobníku a vznikají a zanikají z potřeby programu.
- Pro tyto proměnné platí, že velikost jejich alokace musí být v průběhu kompilování neměnná.
- Pokud potřebná velikost není známá do běhu programu *(v případě čtení velikosti z disku nebo od uživatele)*, potom použití fixní velikosti objektu není na místě.

Statické nebo automatické alokování paměti nemusí být vhodné pro všechny situace. Data z automaticky alokované paměti nepřetrvají přes vícenásobné volání funkce (respektive funkcí), zatímco statická data přetrvávají v paměti, ať už jsou programem využita nebo nevyužita. V mnoha případech tak záleží na programátorovi a jeho umu nakládat s alokací paměti.

Těmto problémům se lze vyhnout při použití dynamicky alokované paměti. Paměť je v tomto případě řízena mnohem příměji (ale pružněji), typicky alokováním z volného místa v paměti (halda).
