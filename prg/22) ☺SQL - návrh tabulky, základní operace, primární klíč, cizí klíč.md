**SQL - návrh tabulky, základní operace, primární klíč, cizí klíč**

- Co to je SQL - Strukturovaný dotazovací jazyk (Structured Query Language)
- RMD - relační model dat - ralacích
- Relace - podmnožina kartézského součinu (kartézský součin je operace na množinami, která vykonává uspořádané dvojice “každý s každým” nebo n-tice)
- A={1,2,3} B={a,b,c} AxB={1a,1b,1c,2a,2b,2c,3a,3b,3c}
- Tabulka seskupení relací - nám popisuje určité entity
- Skládá se ze sloupců, kterým říkáme atributy a volíme takové vlastnosti, které nás o dané entitě zajímají
- create database nazev if not exists / drop database nazev !!! Drop database
- Základním příkazem pro vytvoření databázové tabulky je příkaz 
- Normální formy
  - 0.NF - existence primárního klíce
  - 1.NF - atomické atributy
  - 2.NF - plne zavislosti všech atributu na primarnim klici (dekompozice tabulky)
  - 3.NF - transitivním uzávěru nad tabulkou (a->b b->c a->c)
- CREATE TABLE

create table user (

`  `id int auto\_increment;

`  `nick varchar(20) not null;

`  `mail varchar(80) unique;

`  `primary key id;

`  `) 

- **ALTER TABLE** – Úprava tabulky
- **DROP TABLE** – Smazání tabulky
- **Datové typy**: int, smallint, tinyint, float, datetime, date, varchar, text
- **Primární klíč** - slouží k tomu, aby byl každý záznam v každé tabulce jednoznačně označen a jednoduše k nalezení. Ve spolupráci s cizím klíčem umožňuje vzájemně propojit dvě tabulky a vytvořit mezi nimi relaci
- Databázový systém by měl být navržen a udržován tak, aby se primární klíč záznamu nemusel nikdy měnit
- Typickým příkladem primárního klíče je například katalogové číslo u výrobků
- V případě, že záznam neobsahuje žádný přirozený primární klíč, se obvykle za primární klíč vytvoří číslo, které záznamu přidělí automaticky sama databáze (auto\_increment)
- **Cizí klíč(foreign key)**: definuje v prostředí [relačních databází](https://cs.wikipedia.org/wiki/Rela%C4%8Dn%C3%AD_datab%C3%A1ze "Relační databáze") vztah mezi dvěma tabulkami, a to tak, že hodnota v určeném sloupci jedné tabulky musí existovat v jiném (primárním) klíči
- umožňuje definovat akce, které mají nastat při pokusu o změnu nebo mazání záznamů v cizí tabulce (on delete cascade on update cascade)
  - Casdace
  - Defaul
  - Null

- CRUD
  - insert into user (nick, mail) values (“Alois”, <aa@mail.cz>)
  - select \* from user | select nick, mail from user
  - update user set nick = “Boss” where id=12
  - delete from user where id=12
- Klausole
  - Where - vybírá konkrétní záznam nebo záznamy 
    např.: where name like martin, where id = 12, where coast<1000
    např.: like L%k – ludek, ludvik, luk, aj. 
    `	`like \_y% - bystrá, bystý, kyj (jakékoliv slovo, které obsahuje na druhé pozici “y”)
  - Order by XXX - řazení podle atributu XXX (přirozené řazení A-Z vzestupné)
    např.: order by coast
    order by XXX desc - sestupné řazení
  - Limit(Y), limit(X,Y) - limituje počet vypsaných záznamů
    Y - počet záznamů
    X – od kolikateho zaznamu
