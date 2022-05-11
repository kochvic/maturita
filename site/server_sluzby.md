# Serverové služby (AD/LDAP, webový server, SOL server)
## AD (LDAP)
- **(AD) Active Directory** je v informatice název adresářových služeb **LDAP** implementované firmou Microsoft pro řadu systémů Windows NT
- **Active Directory** byla představena ve **Windows 2000** jako nástupce Domény Windows, který umožňoval pro centrální uchování informací využít stromovou strukturu databáze
- Adresářová služba **Active Directory** je rozšiřitelná a škálovatelná adresářová služba, která umožňuje efektivně uspořádat síťové prostředky. Kromě informací o objektech v počítačové síti *(uživatelské účty, počítače, tiskárny)* umožňuje používat stromovou strukturu objektů, nastavovat globálně systémové politiky, instalovat programy na počítače nebo aplikovat kritické aktualizace v celé organizační structure

- **Logická**
  - Organizační jednotky - podskupiny domén
  - Domény - skupiny počítačů sdílejících společnou adresářovou databázi
  - Stromy domén - jedna nebo více domén sdílejících souvislý obor názvů
  - Lesy domén - jeden nebo více stromů domén sdílejících společné adresářové informace
- **Fyzická**
  - Podsítě - síťová skupina se specifickým rozsahem adres IP a masky podsítě
  - Sítě - jedna nebo více podsítí

## **Webový server**
- Pojmu webový server se rozumí buď počítači který vyřizuje požadavky HTTP nebo počítačovému programu (démonovi)
- Nejpoužívanějším serverem vůbec je **Apache HTTP server** a pak následuje nginx (engine x)
- Jednotlivé webové servery se mohou v různých jednotlivostech značně lišit. Přesto mají několik společných vlastností.
- Každý webový server je připojen k počítačové síti a přijímá požadavky ve tvaru HTTP. Tyto požadavky vyřizuje a počítači, který požadavek vznesl, vrací odpověď. Odpověď obvykle představuje nějaký HTML dokument. Může to být, ale i dokument v jiném formátu – text, obrázek, apod…
## **FTP Server**
- FTP (File Transer Protocol) je standardní síťový protokol pro přenos souborů mezi počítači pomocí počítačové sítě. Využívý protokol TCP z rodiny TCP/IP a není závislý na používaném operačním systému.
- Využívá porty 21 pro přenos příkazů FTP a port 20 pro samotný přenos žádaných souborů

## **SQL server**
- Zkráceně: je to relační databázový a analytický systém, který slouží pro ukládání a vracení dat, které jsou požadovány jinými softwarovými aplikacemi. Microsoft má už několik desítek verzí SQL serveru které jsou zaměřeny na různé práce a rozsáhlosti prací od malých strojů po velké mašiny
- První SQL server se objevil v roce 1989
