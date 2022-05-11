# 8- Ukazatele
- Ukazatel ([anglicky](https://cs.wikipedia.org/wiki/Angli%C4%8Dtina) pointer) je v [informatice](https://cs.wikipedia.org/wiki/Informatika) označení pro [datový typ](https://cs.wikipedia.org/wiki/Datov%C3%BD_typ), který slouží k uložení [adresy](https://cs.wikipedia.org/wiki/Adresa_\(informatika\)) v [paměti počítače](https://cs.wikipedia.org/wiki/Opera%C4%8Dn%C3%AD_pam%C4%9B%C5%A5).
- Ukazatel slouží pro zpřístupnění [dat](https://cs.wikipedia.org/wiki/Data), která jsou na příslušné adrese v operační paměti uložena.
- Ukazatel používá většina [imperativních](https://cs.wikipedia.org/wiki/Imperativn%C3%AD_programov%C3%A1n%C3%AD) [programovacích jazyků](https://cs.wikipedia.org/wiki/Programovac%C3%AD_jazyk), jako např. [jazyk C](https://cs.wikipedia.org/wiki/C_\(programovac%C3%AD_jazyk\))/C++ a Pascal.
- V programovacích jazycích je syntaxí zápisu programu rozlišeno, zda se pracuje s hodnotou adresy ukazatele anebo s hodnotou datového prvku, na který ukazuje. V případě jazyk C/C++ je jedná o operátory \* a &
- Zvláště významný je tento datový typ v [jazyku C](https://cs.wikipedia.org/wiki/C_\(programovac%C3%AD_jazyk\)), který definuje i tzv. pointerovou aritmetiku, díky které lze např. provést výpočet adres různých prvků v [poli](https://cs.wikipedia.org/wiki/Pole_\(datov%C3%A1_struktura\)), nebo naopak z jejich adresy odvodit jejich index.
- Jazyk C téměř nerozlišuje mezi ukazatelem a polem protože nemá datový typ “řetezec” takže nahrazuje jej právě ukazatelem na jeho počátek. Jinými slovy s tím pracuje jako s polem znaku.
- V novějších programovacích jazycích, jako například [Java](https://cs.wikipedia.org/wiki/Java_\(programovac%C3%AD_jazyk\)) a [Python](https://cs.wikipedia.org/wiki/Python), jsou ukazatele nahrazeny [referencemi](https://cs.wikipedia.org/wiki/Reference_\(programov%C3%A1n%C3%AD\)) na [objekty](https://cs.wikipedia.org/wiki/Objektov%C4%9B_orientovan%C3%A9_programov%C3%A1n%C3%AD), jejichž použití není tolik náchylné k základním chybám.
## *Ukazatele v jazyce C/C++*
**deklarace**

- musíme uvést před identifikátorem proměnné operátor dereference \*

např: 

double \*c; //jedná se o deklaraci ukazatele na double

int \*cislo = &prom; //jedná se o deklaraci s inicializací ukazatele cislo na adresu 			proměnné prom

int\* nazev\_fce(double param){} //jedná se o návratový typ ukazatele na int

int \*cislo; //deklarace ukazatele na int

cislo = &prom; //nastavení hodnoty ukazatele na adresu proměnné prom

int \*idealni\_deklarace\_pointeru = null; //deklarace ukazatele na int, který neukazuje 						nikam

\*\*cislo //jedná se o ukazatel na ukazatele atd.

![](Aspose.Words.4149e9f6-1bde-4259-b46e-dc009b7a282f.001.png)

![](Aspose.Words.4149e9f6-1bde-4259-b46e-dc009b7a282f.002.png)

## Pointerová aritmetika
- Pointerová aritmetika definuje možné výpočetní operace s ukazateli.
- [Adresovatelnou](https://cs.wikipedia.org/wiki/Adresa_\(informatika\)) jednotkou ukazatele může být jeden [bajt](https://cs.wikipedia.org/wiki/Bajt) nebo jedno [slovo](https://cs.wikipedia.org/wiki/Slovo_\(pam%C4%9B%C5%A5ov%C3%A1_jednotka\)), ale nejčastěji ve [vyšších programovacích jazycích](https://cs.wikipedia.org/wiki/Programovac%C3%AD_jazyk) je adresovatelnou jednotkou ukazatele velikost [datového typu](https://cs.wikipedia.org/wiki/Datov%C3%BD_typ), který ukazatel adresuje.
- Adresy ukazatelů se kterými se provádí pointerová aritmetika se musí nacházet ve stejném adresovém prostoru (např. poli), jinak nemusí být výsledek operace definován.

int pole[100];

myFce(pole);

void myFce(int \*pole){

`  `//nemuzu napsat pole[5]

`  `\*(pole+5) = 10;

}

if(rect1==rect2) //???

if(rect1.isEquals(rect2)) //ok
2
