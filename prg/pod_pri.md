# Podmíněné příkazy

Slouží k **rozhodování** uvnitř programu. Větví program na dvě vzájemně vyloučené části.
Podmíněné příkazy fungují tak, že se vyhodnotí vstupní podmínka a pokud je **splněna (TRUE)** tak se vykoná určitá část programu.
**Typy podmíněných příkazů:**
-	Neúplné větvení (if)
-	Úplné větvení (if-else)
-	Násobné větvení (switch)
-	Ternární operátor

### Příkaz if - neúplná podmínka
Pokud je něco platné (podmínka splněna) tak provedu nějaké operace.
Syntaxe:

    if(podmínka) příkaz;
    if(podmínka) {
      Sada příkazů;
    };

### Příkaz if-else – úplná podmínka
Tvoření
if(podmínka) příkaz1; else příkaz2;
-	Jestliže je splněna podmínka, potom vykonej příkaz1 jinak vykonej příkaz2.
-	Druhou část ELSE je možné vynechat, pak to znamená, že při splnění podmínky je vykonaný příkaz1, jinak se neděje nic (neúplně větvení).

Konkrétní příklady:

    if(a>b) printf(“a vetší\n”); else printf(“b větší\n”);
Jako operátory je možné použít
-	< , > , >= , <= , libovolné číslo vyjma 0 je považováno za true
-	|| - or (nebo) logický součet - disjunkce
-	&& - and (a zároveň) logický součin - konjunkce
-	== ekvivalence
-	!= non-ekvivalence
-	! negace (bool sviti=true; if(!sviti) printf(“Nesvítí\n”);)


### Příkaz switch – násobná podmínka
Tvoření
switch(proměnná){ //proměnná by měla být ordinárního typu (int, char aj.)

    case hodnota1: příkaz1;
    break;
    case hodnota2: příkaz2;
    break;  
    default: příkazN;
    }

**break** - ukončuje provádění příkazu switch<br>
**default** – se provede pokud neodpovídá žádná hodnota u case
Není důležité zachovávat nějaké řazení v případě hodnot u case.
