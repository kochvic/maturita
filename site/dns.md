## **DNS**
- DNS (Domain name system) nejdůležitější a přitom nejvíc zapomenutá část našeho internetu, bez DNS by internet jak ho známe neexistoval
- DNS server slouží k překladu doménových jmen na IP adresy a naopak
- Internet je celosvětový systém propojených počítačových síťí, ve kterých mezi sebou počítače komunikují pomocí rodiny protokolů TCP/IP
- DNS nemá pro malé lokální sítě příliš velký význam - často se používá DNS provider
- Není možné si pamatovat desítky IP adres stránek, které denně navštěvujeme, proto je tu DNS server = přeloží naší URL ([www.seznam.cz](http://www.seznam.cz)) do IP adresy, kterou potřebuje prohlížeč pro připojení
- Doména dokáže obsluhovat až 3 DNS servery
## **Funkčnost**
- DNS server naslouchá na **portu 53**
- Protokol DNS pracuje způsobem dotaz-odpověď čili klient-server
- Používá oba transportní protokoly UDP i TCP
- Týká se aplikační vrstvy, neřeší otázku vlastního přenosu paketu
- U dotazu na překlad (žádost o RR - resource record) dává přednost UDP
- Pokud je odpověď delší než 512B vloží se do UDP pouze část nepřesahující 512B a nastaví se TC bit že odpověd je neuplná. Klient si může kompletní odpověď vyžádat protokolem TCP
## **Resolver = „rozkladač“**
- Jedná se o součást OS, kterou mohou všechny aplikace použít k rozkladu doménových jmen na IP adresy (prakticky se jedná o klientskou část ke službě DNS)
- Jednotlivé aplikace se tam nemusí obtěžovat s implementací protokolu -> pouze zadají požadavek na zjištění IP adresy
- V Linuxu je možné systémový resolver konfigurovat v souboru **/etc/resolv.conf** *//v tomto souboru nalezneme IP adresy DNS serveru, na které budou směrovány dotazy*
- Syntaxe souboru:
  - nameserver IPadresa
  - nameserver 5.5.5.5
## **Druhy DNS serverů**
- Existuje mnoho typů, avšak záleží na funkci a na postavení v hierarchii DNS
- Primární
  - je hlavním typem DNS systému, obsahuje informace o spravovaných doménách
- Sekundární
  - záložní systém, který pracuje v případě výpadku primárního serveru. Automaticky synchronizuje údaje z primárního serveru
- DNS cache server
  - nejjednodušší jednotka v DNS síti. DNS cache neobsahuje žádné informace o doménách. Pouze vyřizuje dotazy uživatelů a ještě si pamatuje všechny odpovědi

## **Konfigurace DNS**
- Existuje hodně alternativních implementací DNS serverů, ale server BIND je nejpoužívanější
- Jedná se o robustní systém, kvalitně spravovaný a udržovaný, navíc obsažen v každé mainstreamové distribuci.
- Jeho konfigurace je obvykle uložena v souboru **/etc/bind/named.conf** a opět se jedná o prostý textový dokument obsahující sadu příkazů od sebe oddělenými středníkem
- Příkazy:
  - ***logging** - konfiguruje ukládání informací o běhu serveru; **options** - umožňuje nastavit globální vlastnosti serveru; **zone** - definuje vlastnosti zony; **acl** - konfiguruje pravidla přístupu (seznam IP); **key** - specifikuje nastavení pro autorizaci a autentizaci; **trusted-keys** definuje kliče DNSSEC, které jsou považovány za důvěryhodné; **server** - umožňuje nastavit vlastnosti vzdálených serverů; **controls** - nastavuje použití utility rndc; **include** - vkládá do konfigurace další soubor*

# **Nastavení zóny**
- Rozdíl mezi autoritativními servery a neautorativními servery (cache) je v nastavení zón. Autoritativní DNS servery mají vždy nastavenou alespoň jednu zónu
- Soubory s nastavením zóny jsou vždy zvlášť od nastavení DNS serveru, ve zvláštním souboru pro danou zónu
- Soubory je dobré ukládat tam, kde máme nastavení DNS (/etc/bind)
- Pojmenování je libovolné, avšak je zažitý formát pojmenování souboru pro snaží orientování se v konfiguraci.
  - Např: db.petr.local

# **Nastavení v named.conf**
- Aby DNS server začal distribuovat záznamy z tohoto zónového souboru, musíte jej zařadit do nastavení Bindu, tzn. vložit do souboru **/etc/bind/named.conf** následující:
  - zone 	„petr.local“{

type master;

file „/etc/bind/db.petr.local“;

}

- Je zde specifikován nejen soubor, ale také typ "master", který určuje váš DNS server jako primární vzhledem k tomuto zónovému souboru

# **Kontrola nastavení a restart služby**
- Před restartem Bindu je vhodné konfiguraci prověřit automatizovaným nástrojem a vyhnout se tak situaci, kdy server znovu nenastartuje kvůli chybě v definici zóny -> čímž by nastal výpadek
- Bind obsahuje nástroj named-checkconf, který stačí bez parametrů spustit: **named-checkconf**
- Dle unixové tradice, pokud tento příkaz nevrátí žádný text, znamená to, že nastavení Bindu je v pořádku, a vy jej můžete v klidu restartovat: **service bind9 restart**
- Nastavení serveru můžeme otestovat příkazem **dig**
  - dig petr.local @1.2.3.4
# **Sekundární DNS**
- Přenos dat zóny (tzv. zónový transfer, zone transfer) je třeba na primárním serveru autorizovat, což můžete provést specifikací příslušné IP adresy u direktivy allow-transfer:
  - Zone	 „petr.local“{

type master;

file „/etc/bind/db.petr.local“;

allow-transfer {@4.3.2.1;}

}

- Následně je třeba na sekundárním serveru vytvořit specifikaci zóny typu slave se specifikací primárního (master) serveru
  - Zone	 „petr.local“{

type slave;

file „/var/cache/bind/db.petr.local“;

masters {@1.2.3.4;}

}
