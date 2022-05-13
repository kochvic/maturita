# Vlákna

Vlákna slouží k paralelnímu (souběžnému) zpracování uvnitř aplikace.

Výhody:
-	v případě provádění náročných operací nebo “real time processů” potřebujeme, aby naše aplikace reagovala na podměty uživatele i těchto situací
-	využití více-jádrových CPU

Nevýhody:
-	problémy vyplývající z použití vláken (race condition, deadlock)

**Dva druhy paralelního zpracování:**
1.	 Na bázi procesů-současné provádění mezi více programy (PSS)

2.	Na bázi vláken-souběžné zpracování v rámci jednoho programu
-	 Vlákno je běžící část programu, více částí programu může běžet současně
 Vlákno se může nacházet ve 5 stavech:
1.	 Běžící-vlákno se provádí (curent)
2.	 Pozastavené-vlákno je pozastaveno, obnovení probíhá od doby pozastavení (sleep(ms), wait())
3.	Blokované- (jenom v případě synchronizace vláken)
nelze přistoupit ke zdroji, neboť jej používá jiné vlákno
	 Vlákno s vyšší prioritou obírá vlákno s nižší prioritou o zdroje
4.	Ready - vlákno připravené (čeká na CPU)
5.	Ukončené (vlákno dokončí svou činnost, nebo vyvoláním výjimky)

Priorita je celé číslo od 1 do 10, kde hodnota 10 má největší prioritu.
- Výchozí priorita vlákna je 5. 	

Máme dvě možnosti, jak vytvořit vlákno:
1.Dědit ze třídy Thread
2.Implementovat rozhraní Runnable

**Metody obsažené v Thread**
**run()** Vstupní bod vlákna (main pro vlákno) – vždy implementovat
**start()** Spouští vlákno
**sleep(ms)** Pozastavení vlákna (cas je parametrem metody v ms)
**getPriority()** Vrací prioritu aktuálního vlákna (setPriority())
**etName()** Vrací jméno vlákna (setName())
**isAlive()** Vrací true, pokud vlákno běží
**join()** -  čeká na to až se dceřiné vlákno spojí s hlavním vláknem (čeká na ukončení dceřiného vlákna)
**setDeamon(true/false)** - pustit vlákno jako démona (to znamená, že toto vlákno zaniká s vláknem, které ho vyvolalo)

**Odkaz na aktuální vlákno získáme voláním statické metody Thread.currentThread().**
- Vlákna spuštěná hlavním vláknem jsou vlákna vedlejší (dceřiná)
- Hlavní vlákno je prvním a posledním vláknem v životě aplikace.
 Hlavním problémem paralelismu je sdílení jednoho zdroje dvěma nebo více vlákny. (care condition)

Řešením je synchronizace vláken pomocí semaforu (monitor) a to v možnostech:  (narušuje paralelní zpracování)
- synchronizovaná metoda
př: void synchronized myMethod(){}

- synchronizovaný blok kódu
př: void myMethod(){
  synchronized(objekt){
    //nejaky kod
  }
}

- K řízení přístupu k metodě musíme metodu definovat s klíčovým slovem synchronized.
- Pastí v synchronizaci je deadlock. K deadlocku může dojít, pokud synchronizujeme podle více zdrojů a zároveň nedodržujeme stálé pořadí zámků (problém dvou písařů)
Problém dvou písařů:
Dva písaři - jeden papír, jedno pero
Vznik deadlock -> jeden písař vezme pero, druhý písař vezme papír, první písař čeká na papír a druhý na pero, ani jeden nemůže dokončit svůj úkol, protože si navzájem zadržují zdroje.
Ke komunikaci mezi vlákny používáme metody (ale pouze v synchronizovaném bloku nebo metodě):
- wait()
- notify()
- notifyAll()
Metoda wait pozastaví aktuální vlákno až do volání metody notify() nebo notifyAll() pro objekt, ke kterému patří zmíněná metoda wait().
Hlavním rozdílem mezi sleep() a wait() je, že wait() uvolňuje všechny objekty, které jsou aktuálním vláknem uzamknuty, zatímco sleep() tak nečiní.
