# GNU/Linux - historie, vývoj, distribuce, kernel

## Historie, Vývoj
- V roce **1983**, **Rochard Stallman** zakládá **GNU projekt**
  * U kterého bylo cílem udělat **"Volný UNIX"**
- V roce **1991**, vzniká  **"Linux"**
   * Jeho cílem bylo vytvořit Open source systému Minix
      * *Minix byl založen na UNIXu*
  * Originálně mě se měl jmenovat "Freax"
      * *Ale Admin tehdějšího FTP serveru neměl jméno v oblivě a bez otázek a oznámení to přejmenoval na "Linux"*
      * Nejdříve vyšel s proprientální licencí s limitací na komerční použití
- V roce **1992** to bylo vydané pod GPL licencí
  * Potom co GNU projekt byl v použitelné podobě, tak **potřeboval Kernel**. V tu chvilku přichází **Linus Torvalds**, se svým školním projektem "Linux"
  * A z toho vznikl celý systém dnes známý jako "GNU/Linux"
  * A od této doby začali vznikat první distribuce
      * *Slackware, Yggdrasil*

## Distribuce
Co je to Linuxová distrubuce?
  - **Linuxová distribuce** je operační systém vytvořený z softwarove kolekce zahrnujici Linuxový kernel a téměř vždy systém pro správu balíčků.
    * Linuxový kernel
    * Balíčky *(GNU)*
      * Jesliže Linuxová distribuce využívá GNU nástroje nazýváme ji **"GNU/Linux."**
    * Správce balíčku *(Package manager)*
    * Desktop UI
      * GNOME
      * KDE Plasma
      * Cinnamon
      * MATE

- Díky širokým možností úprav je možné vytvořit Linuxovou distribuci pro každé použití
  * *(embedded zařízení, přes automobily, telefony, rakoteplany i servery a desktop)*
- V enterprise *(podnikové)* prostředí existují 3 hlavní hráči:
    * Red Hat
    * SUSE
    * Oracle
- Desktopové prostředí je pro nižší nároky jednodušší
    * Arch Linux
    * Ubuntu
    * Debian
    * OpenSUSE
    * Mate

### Debian
  - Debian byl vytvořen v roce **1993**, **Ian Mrdock**em
  - Jméno bylo vytovřené kombinací jeho jména a jeho ženy *(která ses s ním rovezdla)*
  - První release byl v roce **1996** a měla code name "Buzz"
    * A od té doby každý release má code name z filmu *Toy Story*
  - V roce **1998** vzníka **apt *(advanced packge tool)***, *ale bylo to vyvíjeno pod jménem "Deity"*
  - Nejznámější "dítě" Debianu je **Ubuntu**
      * Ubuntu mělo první release v roce **2004**
      * O Ubuntu se stará britská společnosti **Canonical**
      * Má "semi-annual" release
        * *jednou za 6 měsíců nebo dvakrát do roka*
      * Release jsou pojmenová podle zvířát + slovo se stejným písmenem *(
Jammy Jellyfish)*
      * Ubuntu bylo první distribuce, která napomohla GNU/Linux přiblížit k standartnímu uživately
      * Ubuntu provází svým životem spoustu kontrovezní
        * *Kvůli vydaní closed source softwaru*
        * *Samotný Richard Stallman říká, že Ubuntu je spyware*
        * *Nepodpora jiného DE než GNOME*
          * Proto vznikly různé "verze" Ubuntu
              * Kubuntu
              * Xubuntu
              * Zubuntu
              * Lubuntu
        * Ale stejnak je nejvíce populární distribuce   

### Redhat
  - V roce **1994, Mark Ewing a Bob Young ** vytváří distribuci Redhat
  - Redhat je známý hodně pro svojí bezpěčnost a spolehlivost
  - Redhat se stará o open-source operační systém
    * Ale vydělavají na
      * Předplatném pro své klienty
        * Což zahrnuje Red Hat support, diagnostiku atd.
  - Dneska má zisky v řádech millonů
  - Před třemi lety byla získaná společností IBM *(International Business Machines Corporation)*
  - Redhat pomohl k výtvoru hodně distribucí k podnikové práci
    * RHEL
    * CentOS
    * Fedora
      * Velmi dobře funguje i jako Desktop
      * A Fedoru používá Linus Torvalds
  - Používá **RPM** *(Rapid Package Manager/RPM Package Manager)* nebo **YUM** *(Yellowdog Updater, Modified)* jako správce balíčků
    |Debian|Redhat|
    |--|--|
    | dpkg| rpm|
    | yum | apt|
    | dnf| aptitude cli|

### Arch Linux, Gentoo
  - Originální myšlenka byla zamířena na jednoduchost, výkon a minimalistiku
  - **Gentoo** (2000)
  - **Arch** (2002)
    * Používá na správce balíčku "pacman"
    * A přivlastnilo si "rolling-release" model
      * *Většinou žádné velké vydání, spíš malé aktualizace více častěji*
## Kernel
