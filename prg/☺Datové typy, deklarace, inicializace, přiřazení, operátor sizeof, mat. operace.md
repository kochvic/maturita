![](Aspose.Words.23f4a930-a5fb-444c-b074-bb2d774f641d.001.png)

**Datové typy**

Datový typ definuje v programování druh nebo význam hodnot, kterých smí nabývat proměnná. Datový typ je určen oborem hodnot a zároveň výpočetními **operacemi**, které lze s hodnotami tohoto typu provádět.

- 3/2=1 (int)
- 3.0/2=1.5 (float, double)
- “2”+”3”=”23” (String)
- 2+3=5 (int, float, double)
- ‘a’+’b’=195

Proměnné hodnotového datového typu si dokážeme jednoduše představit. Může se jednat např. o číslo nebo znak. V paměti je jednoduše uložena přímo hodnota a my k této hodnotě můžeme z programu přímo přistupovat. 

Např máme: int, long, float, double, char

**Deklarace**

Deklarace je v informatice zápis, kterým se v počítačovém programu zavádí jméno a zpravidla určuje jeho datový typ a další aspekty pro proměnné, funkce, konstanty apod. Překladač je tak informován o příslušném objektu.

Každou proměnou je před jejím použitím potřeba deklarovat, to znamená, že je nutné ji pojmenovat a určit její typ.

Proměnné deklarujeme takto :

int   i, j;  // 2 proměnné typu int 

char  c, ch; // 2 proměnné typu char

float f;     // 1 proměnná typu float

int i;   // globální proměnná

main()   // funkce main - zde začíná program

{        // začátek bloku

`  `int j;   // lokální proměnná

}        // konec bloku 

***Globální proměnná*** - takto definované proměnné mají platnost od místa definice do konce souboru.

***Lokální proměnná*** - takto definované proměnné mají platnost pouze uvnitř funkce nebo programové struktury (switch, for, while) ve které jsou definovány

**Inicializace**

**Inicializace proměnných**

V oblasti programování se setkáváme s pojmem "inicializace proměnných"

Při deklaraci proměnnou vytváříme a při inicializaci do ni dosazujeme počáteční hodnotu. Například v jazyce Java:

int x; //pouze deklarace

int y = 2000; //inicializace

int y = 5000;//deklarace s inicializací

**Přiřazení**

Příkaz **přiřazení** se vyskytuje ve většině [imperativních](https://cs.wikipedia.org/wiki/Imperativn%C3%AD_programov%C3%A1n%C3%AD "Imperativní programování") [programovacích jazyků](https://cs.wikipedia.org/wiki/Programovac%C3%AD_jazyk "Programovací jazyk"). Způsobí nastavení či změnu hodnoty nějaké [proměnné](https://cs.wikipedia.org/wiki/Prom%C4%9Bnn%C3%A1 "Proměnná").

Přiřazení se nejčastěji zapisuje pomocí [rovnítka](https://cs.wikipedia.org/wiki/Rovn%C3%ADtko "Rovnítko"): “ Cíl = výraz ” (L-hodnota = výraz)

Cíl (který se podle konvence uvádí vlevo od přiřazení) může být pouze taková konstrukce, u které interpreter nebo překladač daného programovacího jazyka zná, kam bude hodnota uložena. Cíl tedy může být popsán přímo jménem (identifikátor) proměnné nebo objektového atributu či tzv. vlastnosti (ve vyšších programovacích jazycích) a nebo (u těch nižších) registrem s výrazem, který nějak určuje cílovou [adresu](https://cs.wikipedia.org/wiki/Adresa_\(programov%C3%A1n%C3%AD\) "Adresa (programování)"), na kterou má být příslušná hodnota uložena.

**Operátor sizeof**

**sizeof Operátor** poskytuje velikost úložiště (v bajtech), která je vyžadována pro uložení objektu typu operandu. Tento operátor vám umožní vyhnout se zadání velikosti dat závislých na počítači v programech.

sizeof(int) -> velikost datového typu int na dané platformě

sizeof(promenna) -> vrátí velikost proměnné s identifikátorem promenna

int buffer\* = (int\*)calloc(100, sizeof(int));

**Matematické operace**

- /
- +
- -
- \*
- % (modulo)

Booleova algebra

- ==
- !=
- <
- >
- <=
- >=
- && (and)
- || (or)

Knihovnu Math.h/ Math.java

- pow
- sqrt
- sin, cos, tan (v radiánech)
- abs
- round



