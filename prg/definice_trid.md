# Definice tříd (instanční a statické datové členy, metody, zapouzdření, konstruktory)
## Instanční a statické proměnné a metody

### Instanční
•	Nemá žádné klíčové slovo
•	Většina metod a datových členů jsou instanční
•	Instanční znamená vztahující se k danému objektu
•	Např. Barva, velikost, hmotnost, a jiné vlastnosti, metody manipulující s těmito vlastnostmi (setColor, aj.)
•	Vznikají a stejně tak zanikají v okamžiku vytvoření/zrušení instance dané Třídy

### Statické
•	Klíčové slůvko je static
•	Jen velmi výjimečné použití
•	Statické znamená vztahující se k třídě
•	Existuje jedna jediná instance v celé aplikaci
•	Vzniká v okamžiku spuštění aplikace (zavedení aplikace do paměti)
•	Klasickým příkladem je třída Math
•	Např. Počet objektů dané třídy, main()


## Zapouzdření

Modifikátory přístupu určují přístup k proměnným, datovým polím, metodám a vlastnostem. Zapisují se zpravidla před daný prvek a využívá se:

- **public**

  * Umožňuje plný přístup odkudkoli.
  * Přístupné vše
  *	Dědí se


- **private**

  * Přístup je povolen pouze z dané třídy.
  * Nejvíce chráněnou metodu nebo datový člen. Volání nebo přístup k datovému členu má pouze ta třída ve které je tato metoda nebo datový člen definován
  *	Nedědí se
  *	private double vysledek;


- **protected**

  * Přístup je povolen pouze z dané třídy a tříy odvozené.
  * Jedná se o chráněnou metodu nebo datový člen přístupnou v rámci stejného balíčku
  * Dědí se

- **Self-defender** (nemá příznak zapouzdření)
  *	Obdoba protected


## Konstruktory

Konstruktor je speciální metoda, která slouží pro vytváření objektu třídy. Může nastavit výchozí stav objektu a implicitní *(předpokladaný)* konstruktor je vytvořen překladačem. Konstruktor vrací nově vytvořený objekt, který lze přiřadit do proměnné.

Parametry konstruktoru lze využít pro nastavení vnitřního stavu objektu.

```java
public Osoba (
  string jmeno, 
  string prijmeni,
  string email = "",
  string telefon = "",
  string titul = ""
  ) {
mJmeno = jmeno;
mPrijmeni = prijmeni;
mEmail = email;
mTelefon = telefon;
mOsobaTitul = titul;
}
```
