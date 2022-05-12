# Základní datové typy, deklarace, inicializace, přiřazení, operátor sizeof, mat. operace
## Základní datové typy
Datový typ definuje v programování druh nebo význam hodnot, kterých smí nabývat proměnná. Datový typ je určen oborem hodnot a zároveň výpočetními operacemi, které lze s hodnotami tohoto typu provádět.

    3/2=1         (int)
    3.0/2=1.5     (float, double)
    “2”+”3”=”23”  (String)
    2+3=5         (int, float, double)
    ‘a’+’b’=195

## Deklarace
Deklarace je v informatice zápis, kterým se v počítačovém programu zavádí jméno a zpravidla určuje jeho datový typ a další aspkety pro proměnné, funkce, konstanty apod. Překladač je tak informován o příslušnému objektu
**Každou proměnou jep řed jejím použitím potřeba deklarovat, to znamená, že je nutné jí pojmenovat a určit její typ.**
Proměnné deklarujeme

    int   i, j;  // 2 proměnné typu int
    char  c, ch; // 2 proměnné typu char
    float f;     // 1 proměnná typu float

    int i;   // globální proměnná
    main()   // funkce main - zde začíná program
    {        // začátek bloku
    int j;   // lokální proměnná
    }        // konec bloku

**Globální proměnná**
Takto definované proměnné mají plastnost od místa definice do konce souboru
**Lokalní proměnná**
Takto definované proměnné mají platnost pouze uvnitř funkce nebo programové struktury (switch, for, while) ve které jsou definovány

## Inicializace
**Inicializace proměnných**
V oblasti programování se setkáváme s pojmem "inicializace proměnných"
Při deklaraci proměnnou vytváříme a při inicializaci do ni dosazujeme počáteční hodnotu.

Například v jazyce Java:

    int x;          //pouze deklarace
    int y = 2000;   //inicializace
    int y = 5000;   //deklarace s inicializací

## Přiřazení
Příkaz přiřazení se vyskytuje ve většině imperativních programovacích jazyků. Způsobí nastavení či změnu hodnoty nějaké proměnné.
Přiřazení se nejčastěji zapisuje pomocí rovnítka: “ Cíl = výraz ” (L-hodnota = výraz)

Cíl (který se podle konvence uvádí vlevo od přiřazení) může být pouze taková konstrukce, u které interpreter nebo překladač daného programovacího jazyka zná, kam bude hodnota uložena. Cíl tedy může být popsán přímo jménem (identifikátor) proměnné nebo objektového atributu či tzv. vlastnosti (ve vyšších programovacích jazycích) a nebo (u těch nižších) registrem s výrazem, který nějak určuje cílovou adresu, na kterou má být příslušná hodnota uložena.

## Operátor sizeof
sizeof Operátor poskytuje velikost úložiště (v bajtech), která je vyžadována pro uložení objektu typu operandu. Tento operátor vám umožní vyhnout se zadání velikosti dat závislých na počítači v programech.

    sizeof(int) -> velikost datového typu int na dané platformě
    sizeof(promenna) -> vrátí velikost proměnné s identifikátorem promenna
    int buffer* = (int*)calloc(100, sizeof(int));

## Matematické operace

  	/
  	+
  	-
  	*
  	% (modulo)
    Booleova algebra
    	==
    	!=
    	<
    	>
    	<=
    	>=
    	&& (and)
    	|| (or)
    Knihovnu Math.h/ Math.java
    	pow
    	sqrt
    	sin, cos, tan (v radiánech)
    	abs
    	round
