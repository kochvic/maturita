# GNU/Linux - historie, vývoj, distribuce, kernel

## Historie
- V roce **1983**, **Rochard Stallman** zakládá **GNU projekt**
  * U kterého bylo cílem udělat **"Volný UNIX"**
- V roce **1991**, vzniklo spojení mezi **GNU projektem a Linuxem**
  * Potom co GNU projekt byl v použitelné podobě, tak **potřeboval Kernel**. V tu chvilku přichází **Linus Torvalds**, se svým školním projektem "Linux"
      * Jeho cílem bylo vytvořit Open source systému Minix
        * *Minix byl založen na UNIXu*
      * Originálně mě se měl jmenovat "Freax"
        * *Ale Admin tehdějšího FTP serveru neměl jméno v oblivě a bez otázek a oznámení to přejmenoval na "Linux"*
      * Nejdříve vyšel s proprientální licencí s limitací na komerční použití
- V roce **1992** to bylo vydané pod GPL licencí
  * A z toho vznikl celý systém dnes známý jako "GNU/Linux"
  * A od této doby začali vznikat první distribuce
      * *Slackware, Yggdrasil*

## Vývoj

## Distribuce
Co je to Linuxová distrubuce?
  - Distribuce je kompletní operační systém, který je založen na Linuxovém kernelu
  - Která obsahu
    * Linuxový kernel
    * Balíčky *(GNU)*
    * Správce balíčku *(Package manager)*
    * Desktop UI
      * GNOME
      * KDE Plasma
      * Cinnamon
      * MATE

Dneska je více jak 1000 distribucí, která jsou všechny vytvořené pro různé prostředí *(Enterprise vs Normalní použití)*
- Rozdělení
  - Server
  - Desktop
  - Mobile
  - Embedded device

### Debian
  - Debian byl vytvořen v roce **1993**, **Ian Mrdock**em
  - Jméno bylo vytovřené kombinací jeho jména a jeho ženy *(která ses s ním rovezdla)*
  - První release byl v roce **1996** a měla code name "Buzz"
    * A od té doby každý release má code name z filmu *Toy Story*
  - V roce **1998** vzníka **apt *(advanced packge tool)***, *ale bylo to vyvíjeno pod jménem "Deity"*
  - Dneska je Debian velmi populární distribuce a je velmi často používaná na serverech, ale dá se taky použít jako distribuce pro normalní užití
    * *Je minimalní a stabilní*
  - Nejznámější "dítě" Debianu je **Ubuntu**
      * Ubuntu mělo první release v rocek **2004**
      * O Ubuntu se stará britská společnosti **Canonical**
      * Má "semi-annual" release
        * *jednou za 6 měsíců nebo dvakrát do roka*
      * Release jsou pojmenová podle zvířát + slovo se stejným písmenem *(
Jammy Jellyfish)*
      * Ubuntu bylo první distribuce, která napomohla GNU/Linux přiblížit k standartnímu uživately
      * Poslední dobou je kontrovezní
        * *Kvůli vydaní closed source softwaru*
        * *Samotný Richard Stallman říká, že Ubuntu je spyware*
        * Ale stejnak je nejvíce populární distribuce
      * Má hodně "verzí"
        * Kubuntu
        * Xubuntu
        * Zubuntu
        * Lubuntu
          * Tyto distribuce jsou velmi podobné Ubuntu ale liší se jen v GUI

### Redhat
  - V roce **1994, Mark Ewing** vytváří distribuci Redhat
  - Redhat je známý hodně pro svojí bezpěčnost a spolehlivost
  - Redhat se stará o open-source operační systém
    * Ale vydělavají na
      * Konzultacích o integrovaní
      * A přídavnými službami pro velké klienty
  - Dneska má zisky v řádech millonů
  - Nedávno byla získaná společností IBM *(International Business Machines Corporation)*
  - Redhat pomohl k výtvoru hodně distribucí k podnikové práci
    * RHEL
    * CentOS
    * Fedora
      * Velmi dobře funguje i jako Desktop
      * A Fedoru používá Linus Torvalds
  - Používá RPM nebo YUM jako správce balíčků

### Arch Linux, Gentoo
  - Originální myšlenka byla zamířena na jednoduchost, výkon a minimalistiku
  - **Gentoo** (2000)
  - **Arch** (2002)
    * Používá na správce balíčku "pacman"
    * A přivlastnilo si "rolling-release" model
      * *Většinou žádné velké vydání, spíš malé aktualizace více častěji*
## Kernel
