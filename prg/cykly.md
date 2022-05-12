# Cykly

Příkazy cyklu se používají k opakování těla cyklu vícekrát v závislosti na podmínce nebo předem daného počtu opakování.

### Cyklus For (C/C++, Javy, C#)
-	Cyklus s předem daným počtem opakování - cyklus se známým počtem iterací.
-	Řídicí proměnné cyklu (iterační proměnná) je přiřazena počáteční hodnota, která se zvyšuje/snižuje v každém iteraci cyklu o krok step a vyhodnocuje se iterační podmínka.
-	Pokud je iterační podmínka splněna (vyhodnocena jako true) provádí se další iterace
-	! Neměla by se v těle cyklu měnit hodnota iterační proměnné nebo význam podmínky

Syntaxe:

    for(pocatecni_nastaveni;iteracni_podminka;iteracni_krok) prikaz;
    for(pocatecni_nastaveni;iteracni_podminka;iteracni_krok) {prikaz1; prikaz2}

    for(int i=0; i<konec;i++) //v těle cyklu neměnit hodnotu i a proměnné konec

Foreach varianta cyklu (PHP) for(T t:pole) prochází celou strukturu (pole, kolekci) a v každé iteraci bere prvek struktury a přiřazuje jej do proměnné t (nemusíme pracovat s proměnnou zapsanou takto: t[index])

    for(;;)	nekonečný cyklus
    for(;i<konec;)


### Cyklus While
-	Tato varianta cyklu se nemusí provést ani jednou (0 až N iterací)
-	Podmíněný výraz se testuje vždy před průchodem cyklu.

Syntaxe:

    while(iteracni_podminka) prikaz;
    while(iteracni_podminka) {prikaz1; prikaz2}
•	Použití v případě kdy nevíme kolikrát bude program iterovat (vstupy od uživatele, čtení ze souboru aj.)

### Cykly Do
-	Tato varianta cyklu se provede minimálně jednou (1 až N iterací)
-	Podmíněný výraz se testuje na konci iterace cyklu.

Syntaxe:

    do prikaz; while(iteracni_podminka);
    do {prikaz1; prikaz2;} while(iteracni_podminka)

•	Použití v případě kdy nevíme kolikrát bude program iterovat (vstupy od uživatele, čtení ze souboru aj.)

### continue / braek
-	Použití v případě, že potřebujeme ukončit iteraci nebo celý cyklus (další iterace nemají smysl - našli jsem co jsem hledali, ukončíme danou iteraci protože pro daný prvek iterace nebude vykonávat žádnou akci)
-	**continue** - přerušení pouze dané iterace, cyklus pokračuje novou iterací
-	**break** - přerušení provádění celého cyklu
