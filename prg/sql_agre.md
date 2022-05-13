# SQL - agregační fce, spojení tabulek, poddotazy, skupiny (GROUP BY, HAVING, aj.)

##	Agregační funkce
-	jsou v SQL statistické funkce, pomocí kterých systém řízení báze dat umožňuje seskupit vybrané řádky dotazu
-	funkce – AVG, COUNT, MAX, MIN, SUM jsou jedny z nejpoužívanějších. Často totiž potřebujeme něco sečíst, zprůměrovat, určit minimální a maximální hodnotu.
-	Při výběru řádků z tabulky (nebo tabulek) většina databázových strojů relačních databází dovoluje výsledné řádky seskupit (agregovat) podle zadaného sloupce nebo výrazu z nich složeného pomocí syntaktické konstrukce GROUP BY
-	select count(*) as numOfCus, country from customers group by country  

## Spojení tabulek
-	**JOIN** je syntaktická konstrukce jazyka SQL. Slouží ke spojování výsledku dotazu SELECT ze dvou a více vstupních tabulek
-	**INNER JOIN** (join)
select autor.jmeno, autor.prijmeni, kniha.nazev from autor join kniha on autor.id=kniha.autor
-	**LEFT JOIN** nám umožnuje spojit tabulky takovým způsovem, kdy z levé (prvně jmenované) tabulky se použití i takové řádky, které nemají odpovídající hodnotu v tabulce druhé. Do požadovaných sloupců z připojované tabulky, kde nebyl žádný odpovídající řádek se doplní NULL.
-	**RIGHT JOIN** je obdobná varianta, ale s opačnou logikou. Všechny řádky z druhé tabulky budou zahrnuty, ikdyž nemaji odpovídající hodnotu v tabulce první. Ve ničem další se od LEFT JOIN neliší
-	**NATURAL JOIN** pokud si výraz přeložíme, dostaneme Přirozené spojení. To v kontextu MySQL databáze znamená, že se spojení využíjí sloupce které se k tomu "přirozeně nabízejí", tedy sloupce se stejným názvem
select kniha.nazev, vydani.isbn from knihy natural join vydani
-	**CROSS JOIN** Výsledkem takového spojení je kartézský součin

##	Poddotazy
-	Vnořené dotazy využijeme tam, kde potřebujeme získat nějaké informace na základě jiných údajů uložených v databázi
-	Jednoduché vnořené dotazy
  -	Za jednoduchý vnořený dotaz budeme považovat vnořený příkaz SELECT vracející nám jednu hodnotu.
  -	hodnotu si SQL server „zapamatuje“ a s ní pak porovnává všechny ostatní hodnoty v tabulce.
```sql
select jmeno, prijmeni from klient where id_klient in
(select id_klient from ucet where stav>1000000)
```
-	**GROUP BY**
  -	je syntaktická konstrukce jazyka SQL pro agregaci záznamů vybíraných pomocí příkazu SELECT.
-	**HAVING**
  -	Klauzule v SQL určuje, že SQL SELECT prohlášení musí vrátit pouze řádky, kde souhrnné hodnoty splňují stanovené podmínky .
```sql
select count(*) as numOfCus, country from customers group by country having numOfCus>0
```
