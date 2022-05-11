# GNU/Linux - instalace a správa aplikací, balíčkovací systémy, konfigurace síťového rozhraní
## Instalace správa aplikací  
- Způsoby, jak dostat SW do Linuxu:
    - Snap, Flatpak
    - Instalace balíčku z repozitářů
    - Instalace balíčků z jiných zdrojů
    - Instalátory (binární soubory)
    - Portable aplikace
    - Kompilace ze zdrojových kódů
    - Emulace

#### Snap, Flatpak

    Snap i flatpak je multidistibutorský systém aplikací. Snap je vyvíjen firmou Cannonical, zatím co flatpak je počin Fedory (RedHat)

    sudo apt install snapd
    #přkaz pro instalaci démona na správu aplikací pomocí snapu

    sudo systemctl snapd enable
    sudo systemctl snapd start
    #práce s demonem

    sudo snap install gimp
    #instalace Gimpu pomocí snapu

#### Instalace balíčku z repozitářů
**Repozitář** - úložiště balíčků (v dnešní době nejčastěji kdysi v Internetu) /etc/apt/source.list

    Výhody použití repozitářů:
        bezpečný software (za předpokladu, že používáte bezpečné repozitáře)
        “automatické” aktualizace - systém sám hlídá, zda-li vaše verze softwaru v systému je stejná jako je uložená v repozitáři.
        příjemná instalace bez hledání někde na Internetu
        bezobslužná instalace (s možností instalace pomocí skriptů)

#### Instalace z repozitářů - program Advance Package Tool (apt)

    sudo apt update
    #aktualizuje seznam aplikací v repozitáři

    sudo apt upgrade
    #aktualizuje systém (nenásilná aktualizace)

    sudo apt install gimp
    #instalace balíčku gimp	 

    sudo apt remove gimp
    #odstranění gimpu, ale zachování nastavení k němu přidružené

    sudo apt purge gimp
    #odstranění gimpu včetně nastavení

#### Instalace balíčku z jiného zdroje než repozitář
Méně bezpečná variata. Vše závysí na zdroji odkud jste získali onen balíček. Koncovka balíčku .deb (Debian) nebo .rpm (RedHat, Fedora)

    dpkg -i package.deb
    #nainstaluje do systému baliček package.deb

    dpkg -r package
    #pozor, při odstrneni baličku bez .deb

    dpkg –help / man dpkg

**Vzniká depency hell (peklo závyslostí) - možné řešení: sudo apt -f install**

#### Instálatory
Klasicky se spustí průvodce instalací (wizard) a provede se instalace, většinou do složky /opt

Soubory typu .sh, .bin, .run aj.

    Musíme k souboru přidat persmission Executable

     chmod +x xxxyyyzzz.run
     #nastaveni oprávnění pro spuštění

    ./xxxyyyzzz.run
    #spuštění aplikace

#### Portable aplikace  

- Portable aplikace se distribuuje bez nutnosti jakékoliv instalace, stačí pouze stáhnou a spustit.
- Vetšinou tyto programy mají koncovku .appimage
  * U nich pak stačí nastavit permission +X

#### Kompilace (pokročilejší technika)
    ./configure
    make
    make install

#### Emulace – Wine

- Emuluje se prostředí jiného operačního systému
  * Z větší části to jsou aplikace napsané pro Windows XP-11
  * *Ale né vždy funkční !*

## Konfigurace síťového rozhraní (NIC)
ifconfig, route, arp, ifdown, ifup - zastaralé příkazy
Příkaz ip:

    ip link (konfugurace síťového rozhraní)
    deaktivovat a aktivovat jednotlivá rozhraní
    přejmenovánat rozhraní 
    měnit konfiguraci rozhraní (MTU, TTL)
    ip addr
    Nastavovat IP adresu a masku rozhraní
    nezapomenout na to, že jedno rozhraní může mít více IP adres
    staticky/dynamicky (DHCP)
    ip addr add 192.168.1.1/24 dev eth0
    ip a a 192.168.1.1/24 dev eth0
    ip addr show
    ip a  
    ip route
    editace routovací tabulky
    0.0.0.0/0 default gateway
    staticky/dynamicky (OSPF, RIP)
    ip neigh
    editace ARP záznamů (MAC - IP)
    staticky/dynamicky (ARP, RARP)
