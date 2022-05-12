# Funkce, předávání parametrů
Jedná se o podprogram. Podprogram nějaká ucelená část programu (dekompozice do podprogramů)

Výhody
  -	usnadnit orientaci v kódu
  -	snadná udržitelnost kódu
  -	update
Nevýhoda:
  -	zpomaluje běh programu

Typy podprogramů:
-	procedury (nemá návratovou hodnotu)
-	funkce (má návratovou hodnotu)

Né všechny problémy musí vracet nějakou hodnotu – je potřeba mít i procedury - má funkce, které vracejí prázdnou hodnotu (void)

Syntaxe:

    návratová_hodnota název_fce (seznam_parametrů){ tělo_fce }

	návratova hodnota pro proceduru je void
    nazev_fce musí splňovat stejné požadavky jako pro název proměnné

(nesmí začítan číslem, nesmí obsahovat speciální znaky vyjma _, vyhnout se kličovým slovům, NE diaktritika, interpunkce a prázdné znaky)

-	seznam_parametrů 0 až N
  -	povinný (př.: void mojeFce(double a){})
  -	nepovinný (př.: void mojeFce(double a=0){})

vs. přetěžování funkcí
-	tělo_fce jsou to příkazy, které se vykonají po zavolání fce. Fce pokud nevrací typ void musí obsahovat return.
-	parametry vs. argumenty - jedná se prakticky o totéž.
  o	V případě, že píšete definici funkce, tak pracujete s parametry.
  o	V případě, že voláte nějakou funkci, tak jí předáváte argumenty.
např:
“procedura”

          void fce1(double a, double b){
            System.out.println(a+b);
          }
          ...
          fce1(3, 2.1);  //volání fce
          fuknci
          double fce2(double a, double b){
            return a+b;
          }
          ...
          double v = fce2(3, 2.1);  //volání fce


### Parametr Funkce
Parametr funkce je označení pro vstupní data funkce v programování. Jedná se o základní metodu, jak předat naše data do podprogramu (další metody jsou např. použití globálních proměnných)
Parametry předané hodnotou

Do funkce je předaná kopie dat z místa odkud došlo k volání podprogramu.
-	většinou předávat pouze primitivní datový typy (int, char, boolean, double, aj.)
-	změna takto předaných dat uvnitř funkce nemá žádný vliv na okolní kód
-	tyto proměnné ukončením fce zanikají

Příklad:

      int sum(int a, int b){
        int v=0;
        a*=10; //op-operátor => a = a*10  
        System.out.println(a +” ”+b+” ”+v); // 50 8 0
        return a+b; //50+8
      }
      ...
      int a=5,b=8;
      int v = sum(a,b); // a=5, b=8
      printf(“%i %i %i”,a, b, v); // 5 8 58

Parametry předané odkazem (referencí)
do funkce je předán ukazatel (refetence) odkazující na data z místa odkud došlo k volání programu.
Syntaxe se liší s programovacím jazykem.
-	pozor objekty, pole a další struktury není možné předat jinak než odkazem
-	změna takto předaných dat uvnitř funkce má zásadní vliv na okolní kód
-	tyto proměnné existují dále i po ukončení podprogramu (jediné co zaniká je právě ten ukazatel/reference)

Příklad:

      int sum(int *a, int b){
        int v=0;
        *a*=10; //op-operátor => a = a*10  
        printf(“%i %i %i”,a, b, v); 50, 8 0
        return *a+b; //50+8
      }
      ...
      int a=5,b=8;
      int v = sum(&a,b); // a=5, b=8
      printf(“%i %i %i”,a, b, v); //50 8 58
      *******************************************
      Rectangle rect = new Rectangle(200, 100);
      double result = Geom.perimeter(rect);
      …
      public static double perimeter(Rectangle r){
        return r.getWidth()*2+r.getHeigth()*2;
      }
