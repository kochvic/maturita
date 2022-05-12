# Složené datové typy (pole, struktura)

Datový typ definuje v programování druh nebo význam hodnot, kterých smí nabývat proměnná *(nebo konstanta)* a operací, které s proměnnou mohu provádět.
Datový typ je určen oborem hodnot a zároveň výpočetními operacemi, které lze s hodnotami tohoto typu provádět.
Součástí programovacího jazyka je definice základních datových typů. Pomocí těchto základních typů může ve většině jazyků programátor tvořit nové složené typy.

Složené Datové Typy
-	Složené datové typy obsahují více prvků:
	 * Homogenní jsou, když se skládají z prvků stejného typu (pole)
	 * Heterogenní jsou, když se skládají z prvků různého typu (struktura)

## Pole

Homogení složený datový typ
může být vícerozměrné (např. dvourozměrné označujeme jako matici),
jednotlivé prvky pole jsou dostupné pod číslem, které určuje jejich pořadí (index).

Nejčastější je konvence používaná v jazyce C, kde indexy začínají číslem 0.

Hlavní výhodou pole je možnost okamžitého přístupu ke kterékoli jeho položce.

Typy polí:
  - Statická pole
  - Dynamická pole
  - Kolekce (Lineární seznamy)
  - Statická pole

Při deklaraci se pevně definuje velikost pole. V průběhu programu se tato velikost **nemůže** měnit ani jinak modifikovat. Toto pole zaniká s ukončením programu

Syntaxe: (C/C++)

    datovy_typ identifikator[velikost]
    int pole[10]; //pole celých čísel s indexy 0-9
    double pole2[] = {3.14, 0.69, 1.11}; //pole reálných čísel s indexy 0-2
    char pole3[] = “Nazdar”; //pole znaků s indexy 0-6 (N,a,z,d,a,r,\0)

    Procházení polem
    int pole[10]
    for(int i=0; i<10; i++){
    pole[i] = rand();
    }

## Dynamická pole (Dynamicky alokovaná pole)
Stejně jako pole statická musí předem definovat určitý počet položek v poli s tou výjimkou, že kdykoliv můžeme toto pole uvolnit před fci free()

Syntaxe: (C/C++)

    int *pole;
    pole = (int*)malloc(sizeof(int)*10); // malloc(počet_bytu)
    pole = (int*)calloc(sizeof(int),10); // calloc(jak_velky, kolik)

malloc i calloc vrací ukazatel na void, je to z toho důvodu aby bylo možné alokovat prostor pro různé datové typy, ale je tedy potřeba explicitně přetypovat ukazatel na potřebný datový

    typ (v našem případě int)
    free(pole);
    Procházení polem:
    int *pole;
    pole = (int*)malloc(sizeof(int)*10); // malloc(počet_bytu)
    for(int i=0; i<10; i++){
    *(pole+i) = rand();
    }

## Kolekce
Nejblíže termínu pole z kolekcí jsou ArrayList, LinkedList, Vector. Tyto objekty jsou podobně jako pole homogenní s tou výjimkou, že není nutné dopředu definovat velikost kolekce. Nastavuje se sama dle potřeby. Problém je, že kolekce nemůže obsahovat primitivní datové typy jako int, double, float, char, boolean, aj.

Syntaxe: (Java)

    ArrayList<Integer> pole = new ArrayList<>();
    pole.add(1);
    pole.add(2);
    pole.add(0,0); //na pozici indexu 0 vloží 0
    pole.get(1); //vrátí 1
    Procházení polem:
    for(int cislo:pole){
    System.out.println(cislo);
    }

**Struktura**
Heterogení složený datový typ
Obdoba objektu v OOP

Syntaxe:

    struct identifikator{
    datovy_typ clen1;
    datovy_typ clen2;
    atd.
    } promenna1, promenna2;
    struct identifikator promenna3; //deklarace promenne3 ze struktury identifikator
    promenna3.clen1=”nevim”;

    často se struktura používá v kombinaci s typedef – jako definice nového datového typu

    typedef struct identifikator{
    datovy_typ clen1;
    datovy_typ clen2;
    atd.
    } nazevNovehoTypuNaZakladeStruktury;
    nazevNovehoTypuNaZakladeStruktury promenna3; //deklarace ze struktury identifikator
    promenna3.clen1=”nevim”;
