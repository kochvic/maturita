# Vyjímky

-	 výjimky jsou způsob signalizace výjimečných stavů “vážných problémů” při provádění programu
-	 Výjimky často signalizují chybu a chyby by měli být v programu často výjimkou.
-	 Výjimka však nemusí vždy nutně znamenat chybu, ale může značit nějakou neobyčejnou událost, které je třeba věnovat pozornost.
-	Výjimka je objekt, který je vytvořen, pokud v programu dojde k nenormální situaci.
-	Tento objekt má datové členy obsahující informace o povaze vzniklého problému.

Výhody používání výjimek
-	oddělení zpracování chyby od běžného kódu
-	oznámení programátorovi, že může dojít k neočekávanému stavu
-	jedna z možností jak ukončit vlákno

Nevýhody
-	režie obsluhy výjimek

Rozdělení výjimek:
1. Výjimky kontrolované (? extends Exceptions)  - musí být obslouženy      	
2. Výjimky nekontrolované (Error, RuntimeException, aj.) - nemusí být obslouženy
příklady: **NullPointerException, ArrayOfBoundExceprion, ArgumentException, aj.**
- Otcem všech výjimek je třída Throwable

Způsoby ošetření výjimek:
-	propagovat výjimku - výjimku neošetřujeme jenom informujeme nadřazenou metodu o možnosti vzniku výjimky (throws)
void mojeSuperMetoda(double a, double b) throws MyException{}
-	obsloužit výjimku - přímo v metodě, kde vznikla (try, catch, finally)
-	**try** - blok dat try vymezuje prostor vzniku výjimky
-	**catch** - blok dat obsahující kód pro ošetření výjimky
-	**finally** - blok finally vymezuje kód, který se vždy provede bez ohledu na vznik výjimek
-	jeden blok try musí být následová minimálně jedním blokem catch

Př:
```java
try{
  file = new File(cesta);
  file.open();
}catch(FileNotFoundException e){
  System.out.println(e.getMessage);
}catch(IOException e){
  System.out.println(e.getMessage);
}catch(Exception e){
  System.out.println(e.getMessage);
}finally{
  if(file.isOpen()) file.close();
}
```
**Jak můžeme reagovat?**
-	 Napravit příčiny vzniku chybového stavu – např. znovu nechat načíst vstup
-	 Poskytnout za chybný vstup náhradu – např. implicitní hodnotu
-	 Operaci neprovést a sdělit chybu výše tím, že výjimku "propustíme" z metody

Výjimková pravidla:
-	Blok catch nenechávejme prázdný, přinejmenším vypišme System.err.println(e.getMessage()), e.printStackTrace() nebo jinou chybovou zprávu
-	Nelze-li reagovat na místě, propusťme výjimku výše

**Vytvoření vlastní výjimky**
1.	vytvoříme vlastní třídu výjimky, tak že dědíme ze třídy Exception
2.	vyvolání výjimky přes klíčové slovo throw

Př:
```java
class MyException extends Exception{
  public MyException(){
    super();
  }
  public MyException(String mess){
    super(mess);
  }
}
class MyApp{
  void myMethod(double a) throws MyException{
    if(stav) throw new MyException(“Neco se mega pokazilo.”); //vyvolani vlastní výjimky
 }
}
```
