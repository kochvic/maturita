# GNU/Linux - správa uživatelů, procesů a nastavování oprávnění k souborům a složkám

## Správa uživatelů

Související soubory se správou uživatelů

    /etc/passwd (obsahuje záznamy o uživatelích)
    /etc/group (obsahuje skupiny uživatelů)
    /etc/shadow (obsahuje hesla uživatelů a jejich nastavení)
    /etc/skel (adresář s kostrou domovské složky nových uživatelů)

    /etc/passwd
    login:vymaskovane_heslo:UID:GID:info_o_uživateli:cesta_k_domovskému_adresáři:shell
    pepik:x:1001:1001:Josef Novák,15,777123456,:/home/pepik:/bin/bash

    /etc/group
    nazev_skupiny:GID:seznam_uživatelů
    root:0:pepik, lojzik, frantik

    /etc/shadow
    login:$cislo_hashovaci_funkce$sůl$heslo:kdy bylo naposledy zmeneno:kdy vyprsi platnost hesla::

#### Postup vzniku nového uživatele v případě čistě manuální práce
  - přidat záznam do /etc/passwd
  - vytvořit adresář, který bude sloužit jako domovská složka (mkdir)
  - do této složky nakopírovat adresář /etc/skel
  - *(volitelné)* vytvoření patřičné skupiny v /etc/group
  - vytvořit pro uživatele heslo *(passwd “login”)*

#### Vytvoření uživatele pomocí skriptu
  - **useradd** (nemá interaktivní rozhraní, nastavování informaci o uživateli pomocí přepínačů (argumentů))
    - sudo **useradd** -c “Josef Novak” -s /bin/bash -m /home/pepik pepik
  - **adduser** (má interaktivní rozhraní)
    - sudo **adduser** pepik

#### Odstranění uživatele pomocí skriptu

    userdel login (odstraní pouze uživatele)
    userdel –R login (odstraní uživatele včetně domovského adresáře)

## Oprávnění k souborům a složkám

ls –l (výpis obsahu aktuálního adresáře)

    ---------- pepik pepik …

-  1.pomlčka
   * definuje co je to zač (d=složka, -=soubor, b=blok dat, s=shell, l=link)
-  2.až 4. pomlčka
  * definuje oprávnění pro vlastníka souboru nebo složky (r w x)
-  5.až 7. pomlčka
  * definuje oprávnění pro skupinu
-  8.až 10. pomlčka
  * definuje oprávnění pro ostatní

**r = read** (čtení, procházení obsahu složky)
**w= write** (zápis, měnit obsah složky)
**x=execute** (spustit, složka se může nacházet v cestě)

#### Nastavování oprávnění
    chmod (pomocí BCD kódu)  
    rwx r-- --- => 111 100 000 => 740
    chmod 740 ~/text.txt

    chmod (pomocí přepínačů)
    chmod komu+/-jaké_oprávněni soubor/složka (u=user, g=group, o=other, nic=pro všechny| +/- | r w x)
    chmod o+r ~/text.txt (nastavení povolení pro ostatní ke čtení)  
    chmod +x ~/script.sh (všem nastavím oprávnění pro spuštění)

#### Nastavení vlastníka a primárni skupiny
    chown lojzik ~/text.txt (změna vlastníka souboru nebo adresáře - jako root)
    chgrp users ~/test.txt (změna skupiny souboru nebo adresáře - jako root)

## Správa procesů
ps - příkaz pro vypsaní aktuálně spuštěných procesů (ps –A (výpis všech procesů v systému)) 
jobs - příkaz vypíše aktivní úlohy
kill - příkaz pro komunikaci s procesy (kill -SIGSIGNAL PID, kill –9 13587, kill –kill 13587)
fg - příkaz pro přepnutí procesu na popředí (fg cislo_ulohy)
bg - příkaz pro přepnutí procesu na popředí (bg cislo_ulohy)
příkaz& - rovnou se pustí na pozadí
