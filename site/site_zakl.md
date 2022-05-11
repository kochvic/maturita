# Počítačové sítě - základní pojmy a topologie

## Počítačová síť:
  - Je systém, který vzniká vzájemným propojením zařízení s cílem komunikace.
  - Základním důvodem pro vytvoření prvních sítí byla potřeba společného přístupu k datům a využití jiného počítače.
  - Síť se skládá
    - jednotlivých *(stanic)*
    - síťového hardwaru *(síťové karty, aktivní a pasivní síťové prvky)*  
    - síťového softwaru.
  - Osoba, která dohlíží na zapojení počítačové sítě je správce sítě. Má přehled i o uživatelích a jejích právech.
  - Jsou dva typy komunikace
    - **Klient / server**
      * Komunikace **klient-server**, server, který poskytuje ostatním stanicím služby jako jsou souborové, aplikační nebo databázové služby. Pracovní stanice, u které pracuje uživatel a využívá služeb které poskytuje server.
      * Základní rozdělení sítě jsou klient-server *(síť serverového typu, je to síť s centralizovanými prostředky, skládá se z hlavního počítače a pracovních stanic jejichž počet je závislý na výkonnosti serveru. Slouží ke správě sítě a uložení společných dat)*
    - **Peer-to-peer**
      * **Peer-to-peer** *(je to síť s distribuovanými prostředky a není určen server, všechny počítače si jsou rovny, využívá se jako jednoduchá pracovní síť obvykle kolem 10 stanic, pokud je množství počítačů větší, udržuje se špatně přehled o prostředcích které jsou k dispozici, hlavně datové soubory a programy. Všechny počítače musí zůstat zapnuty dokud poslední uživatel neukončí práci s příslušným sdíleným prostředkem.)*

- Rozdělení sítí dle velikosti:
  - **LAN** *(lokální síť – ve firmách a školách)*  
  - **MAN** *(městské sítě)*  
  - **WAN** *(rozsáhlé národní až celosvětové sítě – Internet)* sítě  



- **Výhody / Nevýhody**
  - **Výhody**
      - sdílení prostředků - data, tiskárny nebo programy (Výhody jsou úspora místa na disku, techniky)
      - Centralizovaná správa
      - Zálohování
      - Rychlá výměna informací
  - **Nevýhody**
      - Bezpečnost
      - Práce



### Topologie sítě:  
představují způsoby rozmístění a spoluprací počítačů zapojených v síti.  

- Jsou dva typy:
    1. topologie fyzická (způsob propojení stanic v síti)
    2. topologie logická (způsob komunikace v síti)  



**Topologie dělíme na**

Sběrnicová topologie:

(nejjednodušší a nejlevnější, každá stanice je připojena ke společnému kabelu který tvoří základ sítě. Výhody – nízká spotřeba kabelu a nízké náklady, porucha jedné stanice nemá vliv na ostatní. Nevýhody – koaxiální kabel je náchylný k mechanickému poškození, obtížná lokalizace závad, porucha na sběrnici vyřadí z funkce celou síť.)  

BNC konektory, T-konektory, Terminátory

    + levné
    + snadné přidání i odebrání stanic

    - nesnadlá lokalizace závady
    - pomalá a stará technologie
    - limit na počet stanic



Hvězdicová topologie:

propojuje stanice aktivním prvkem switch, její úkolem je směrovat data zaslaná z jedné stanice k ostatním. K propojení stanic switchem se používá kroucená dvojlinka. (T-konektor nebo terminator se nepoužívá!!)  

Výhody – menší náchylnost k poruchám kabeláže, snadná lokalizace závad, snadná konfigurace sítě, snadno +/- pokud stačí porty na switch.  

Nevýhody – větší spotřeba spojovacích kabelů, potřeba aktivního prvku (vyšší náklady)









Kruhová topologie:  

stanice jsou fyzicky propojené do kruhu, data se obvykle posílají stejným směrem. Komunikace je realizována metodou Token ring (token passing). Vysílat mohou stanice které vlastní token.  

    Výhody – Jednoduchá koncepce předávání zpráv, vyšší rychlost.  

    Nevýhody – Drahé síťové karty.







Stromová topologie / Hybridní topologie:

je tvořena kombinací hvězdicové a sběrnicové topologie. Jejím základem je páteřní vedení ke kterému se připojují další části. Páteřní vedení je segment sítě ke kterému jsou připojeny ostatní segmenty.  
