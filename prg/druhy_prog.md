# Druhy programovacích jazyků, syntaxe, sémantika, zdrojový kód, kompilátor

## Druhy programovacích jazyků
Programovací jazyk je prostředk pro zápis algoritmů, jež mohou být provedeny na počítači. Zápis algoritmu ve zvoleném programovacím jazyce se nazývá program.

### Druhy programovacích jazyků
  - Nižší vs. Vyšší
    - Assemblem **vs** C#,Java,Python
  - Kompilované vs Interpretované
    - C#, Java, C/C++ **vs** PHP, Python, Java
  - Funkcionální vs Procedurální vs Inperativ/Imperativní
    - Lisp vs Prolog **vs** C/C++, C#, Java, JavaScript, PHP
  - Dle užití
    - Web: HTML, PHP, JavaScript
    - Grafika: Python, C++
    - Hry: C++
  - Značkovací vs Programovací
    - HTML, XML **vs** Cokoliv předchozího
  - Nové vs Zastaralé
    - JavaScript, Ruby, Lua **vs** Pascal, Basicm Fortran

**Python**
V praxi se hodí například pro **psaní skriptů** pro urychlení repetitivní činnosti, ať už mezi vědci, výzkumníky nebo běžnými programátory. Využívá se hojně pro **analýzu dat, zpracování obrazu, zvuku**

### Syntaxe
**Syntaxe** = způsob jak se příkazy zapisují *(odhalí kompilátor)*
**Sémantika** = vypovídá o významu daného příkazu

      iv (podmínka) = syntaktická chyba - neznám příkaz iv

      if (age<18)
        System.out.println("Plnoletý");
      prom/0

V informatice je **syntaxe** programovacího jazyka soubor pravidel, která definují kombinaci symbolů, které jsou považovány za správně strukturovaný dokument nebo část v tomto jazyce
To platí jak pro programovací jazyky, kde dokument představuje **zdrojový kod**, tak pro značkovací jazyky, kde dokument představuje **data**
**Syntaxe jazyka defunuje jeho povrchovou formu**
Textové programovací jazyky jsou založeny na **posloupnosti znaků**, zatímco vizualní programovací jazyky jsou založeny na **prostorovém uspořádání** a spojení mezi symboly *(které mohou výt textové nebo grafické)*. Dokumenty, které jsou syntakticky neplatné, obsahují syntaktickou chybu.

### Sémantika

**Sémantika programovacích** jazyků je v teorii programovacích jazyků obor zabývající se důsledným **matematickým popisem** významu programovacího jazyka. Zhodnocuje **význam syntakticky platných řetězců** v daném programovacím jazyce, včetně jejich výpočtu. V případě ohodnocování **syntakticky neplatných řetězců**, není výpočet proveden. **Sémantika** popisuje **procesy**, které řídí počítač při **vykonávání programu** v daném **programovacím jazyce**. Například tím, že popisuje **vztah mezi vstupem a výstupem programu**, nebo popisem jak **program poběží na určité platformě**, tedy vytvořením modelu výpočtu.
Dělí se na:
  - **Statickou**
    - Sémantika programovacích jazyků je v teorii programovacích jazyků obor zabývající se důsledným matematickým popisem významu programovacího jazyka. Zhodnocuje význam syntakticky platných řetězců v daném programovacím jazyce, včetně jejich výpočtu. V případě ohodnocování syntakticky neplatných řetězců, není výpočet proveden. Sémantika popisuje procesy, které řídí počítač při vykonávání programu v daném programovacím jazyce. Například tím, že popisuje vztah mezi vstupem a výstupem programu, nebo popisem jak program poběží na určité platformě, tedy vytvořením modelu výpočtu.
  - **Dynamickou**
    - Dynamická sémantika je řešena přímo za běhu programu. Dynamicky typované jazyky jsou významné v jednotlivých jazykových konstrukcí. Jaký úkon se má provést, když je v programu napsán daný příkaz nebo priorita operátorů. Dynamická sémantika je obzvlášť náročná u programovacích jazyků s rekurzivním voláním podprogramů, proto je nutné vést evidenci o volání téhož podprogramu. Z kterého se vytváří aktivační záznamy pro jednotlivá volání podprogramů a jejich následné ukládání do zásobníku.

### Zdrojový kod (Source code)
**Zdrojový kó**d *(zdrojový text slangově zdroják, anglicky source code)* je v informatice označení zápisu **počítačového programu** nebo jeho části v nějakém programovacím jazyce. Kompletní zdrojový kód softwarového projektu je obvykle uložen v **jednom nebo více textových souborech**. Zdrojový kód může být buď přímo prováděn *(interpretován)* interpretem nebo přeložen kompilátorem, který z něj vytvoří **spustitelný soubor** *(případně doplněný knihovnami)* obsahující **strojový kód**, který může operační systém zavést do paměti a spustit, takže je prováděn procesorem počítače. Běžný uživatel počítače obvykle se zdrojovým kódem **nepřijde do styku**.
**Zdrojový kód** obvykle programátor zapisuje pomocí **textového editoru**, ale může být též generován **specializovaným programem**. Textový editor může být součástí vývojového prostředí **(IDE)**, které programátorovi tvorbu zdrojového kódu **usnadňuje** a poskytuje mu další podporu: **zvýraznění syntaxe, vyznačení syntaktických chyb, nápověda, seznamy funkcí, příklady, přímý přístup k navazujícím nástrojům** *(vyvolání kompilátoru, možnost krokování a sledování průběhu programu pomocí debuggeru, vytváření souborů pro řízení překladu (Makefile), zpracování dokumentace a podobně)*.
Samotný **zdrojový kód** nelze přímo využít. Je potřeba ho buď nechat přímo provádět interpreterem nebo je možné ho nejprve překladačem přeložit do cílového strojového kódu procesoru a poté ho nechat přímo procesorem vykonávat. **Zdrojové kódy** se obvykle s jednotlivými programy **nedistribuují** a běžný uživatel s nimi nepřijde do styku. Zvláštním případem je **open source software**, kde je **dostupnost zdrojových kódů obvyklá**. Umožňuje pokročilým uživatelům programy upravovat a zdrojové kódy přímo využívat *(viz distribuce Linuxu a speciálně Gentoo Linux)*.
