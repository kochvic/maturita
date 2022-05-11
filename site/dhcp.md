# DHCP

## DHCP
- DHCP (Dynamic Host Configuration Protocol), jeho cílem je přiřazení unikátní IP adresy počítačům v síťi, ale i další věci jako například: masku podsítě, default gateway (výchozí brána) a DNS adresu
- Dokáže klientům vnutit chování podle určitých norem – „změnit“ MAC adresu, informovat ho o SMTP, POP, time a dalších serverech
- Nastavení určitých strojů staticky – PC poskytující určité služby:
  - *Web server, SMTP server, router*
- Usnadňují se služby, ale i vzdálené konfigurace jednotlivých serverů

- Klient připojený do neznámé sítě by musel znát topologii sítě, aby mohl komunikovat. Takový uživatel by si musel manuálně sehnat a konfigurovat dle síťovýho rozhraní, avšak může získat síťovou konfiguraci skrz DHCP. 
  - Klient rozesílá omezený broadcastu (není routovaný do jiné sítě) s packetem **DHCPDiscover** – identifikace danému DHCP (jméno, MAC adresu, …) ->
  - Server odpovídá packetem **DHCPOffer** – potvrzení komunikace ->
  - Následně probíhá komunikace klient-server. Klient posílá žádost o získáni nastavení **DHCPRequest** a server odpovídá packety **DHCPACK** (+ odpověď) či **DHCPNAK** ( - odpověď)
> Veškerá komunikace klienta probíhá na portu 68 (UDP) a serveru naslouchá na portu 67 (UDP)

- DHCP server se má vyskytovat na každé podsíti, aby byla možnost provést automatickou konfiguraci síťového rozhraní – předávací agent **(relay agent)**
  - GNU/Linux - ISC balíček implementuje i server DNS, kvalitně spravovaný opensource

## Instalace serveru
- Ubuntu – sudo apt-get install isc-dhcp-server *// instalace serveru*
- Poté získáte samotný program **dhcpd**, konfigurační soubor **dhcpd.conf** a databázový soubor **dhcpd.leases** *//bez toho nám DHCP server nerozjede*

## Seznam zapůjčených adres
- Seznam zapůjčených adres je v textovém souboru dhcpd.leases
- Cesta k souboru /var/lib/dhcp/dhcpd.leases
- Cesty se můžou lišit od distribuce – locate dhcpd.conf/.leases
- **Spuštění|zastavení|restart** DHCP serveru
  - sudo nano /etc/default/isc-dhcp-server
  - sudo service isc-dhcp-server **start|stop|restart**

## Relay agent
- Jak bylo řečeno DHCPDiscover není routovaný do jiné sítě
- Jak tedy centrálně zpravovat rozsáhlé sítě? Proč se na serveru tedy konfigurují různé subnety? Odpovědí jsou relay agenti.
- Relay agent nebo taky DHCP **relay server** se stará o předání žádosti k hlavnímu, centrálnímu DHCP serveru. Ke spuštění DHCP relay serveru potřebujeme nainstalovat balíček **isc-dhcp-relay** na stroj, který má sloužit jako relay agent (samozřejmě se musí vyskytovat v daném subnetu, který má být propojen s centrálním DHCP serverem
