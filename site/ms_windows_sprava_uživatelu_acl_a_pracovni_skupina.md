# MS Windows - správa uživatelů, ACL a pracovní skupina

**Windows rozlišuje oprávnění a práva**, oprávnění je možnost přistoupit k některému objektu vybraným způsobem a právo dovoluje provést nkterou systémovou akci. Nastavení oprávnění u konkrétního prostředku pro větší počet uživatelů může  být problematické, proto se zde nachází uplatnění skupina uživatelů

**Uživatelský účet**: Uživatel může být buď správce nebo standardní uživatel, administrátorský účet dovoluje provést změny které ovlivní ostatní uživatele (konfigurace systému, instalace softwaru apod.)

**Administrátorský účet**: Být adminem je určité privilegium, proto se přiděluje jednotlivým uživatelům s rozumem

*Nejvyšším oprávněním v rámci NTFS je takzvané úplné řízení, které uživatelům dovoluje měnit oprávnění, spouštět soubory, listovat složkami, upravovat soubory apod.*

**ACL** (seznam pro řízení přístupu) je v oblasti počítačové bezpečnosti seznam oprávnění připojený k nějakému objektu. Seznam určuje, kdo má povolení přistupovat k objektu a jaké operace s ním může provádět. V typickém ACL specifikuje každý záznam v seznamu uživatele a operaci. Například: Záznam v ACL [Pepa, smazat] pro soubor XYZ dává uživateli Pepa právo smazat soubor XYZ.

**Pracovní skupina**: Všechny počítače jsou rovnocenné, žádný z počítačů nemá kontrolu nad jiným počítačem, chceme-li se přihlásit do počítače pracovní skupiny, musíme v něm mít uživatelský účet

- Správa uživatelů
    - Defaultní uživatelé (administrator, guest, default account)
    - Nový uživatelé (při instalaci systému, mmc > správa místních uživatelů a skupin, microsoft account)
        * Informace o uživateli
        * Login
        * Celé jméno
        * Heslo (bezpečnosti)
        * Cesta k profilu
            * Appdata (%APPDATA%)  
            * UAC (user account control)
            * Obrázky, download, Oblíbené (IE, EDGE) 
        * Terminovat možnost přihlášení (které dny a časy)
Skupiny (ACL)
   - Využívají se pro definování sady pravidel na více uživatelů
   - Administrators, Users, aj.
ACL – access control list (skupiny, nebo uživatele)
   - Systém, který ovlivňuje přístup s souborům a složkám
  - Číst / Zapisovat / Měnit / číst a spouštět / úplné řízení
   - Složkou vs. Souborem
Pracovní skupina / Doména
   - WORKGROUP (defaultní název skupiny)
