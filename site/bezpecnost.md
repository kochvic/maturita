# Bezpečnost — malware, firewall, certifikáty, šifrování
Hrozby
    Odcizení identity
    Odcizení finančního charakteru
    Odcizení dat
    Využívání HW prostředků
    Narušení dostupnosti k datům (ransomware)
    Poškození HW nebo SW
    Ovlivnění třetí stranou

||  Odcizení identity|
|-|--|
||Zpřístupnění druhé osobě své elektronické ID. (Hesla, čipy, USB key, NFC)|Prostě odcizení finančního charakteru|Zvýšení bezpečnosti dat má většinou za následek snížení dostupnosti. |
|**Hrozby**|Škodlivý software v PC **(keylogger)**, **Brutal Force attack** / slovníkové útoky, **Phishing** (stránka vypadá jako známá stránka banky)
|**Řešení**| **Bezpečné heslo** (1 heslo na 1 službu, password manager), **Dvoufázové ověření**, Zjistit na jaké stránky se loguji **(HTTPS)**, Zavčasu hlásit ztrátu, **Šifrování komunikace** (WEB error, WPA, HTTPS, SSH)  

|| Odcizení finančního charakteru |
|-|--|
|**Hrozby**|Phishing, Spam, Vydírání (privátní data), Ransomware (zakriptuje data a chce úplatek)|
|**Řešení**| Zjistit s kým komunikujete, Šifrování|

|| Odcizení dat |
|-|--|
||Zvýšení bezpečnosti dat má většinou za následek snížení dostupnosti. |
|**Řešení**|     Heslování, šífrování |   

### Využívaní HW prostředků
Výkon Vašeho PC *(bot)* se podílí na nekalých praktikách - **DDOS útoky** *(zahlcení služby)*. **Botnety** - armáda PC pod cizí nadvládou. Za účelem těžby **kryptoměny**.

- Řešení z hlediska toho nestát se botem
  -  Mít základní pravidla práce na PC (vědět s jakými daty pracujete) pozor na vydavatele softwaru
  -  UAC, nebýt jako admin
  -  Antivirus

- Řešení z hlediska DDOS
  -  Dobrou konfigurací firewall
  -  **HoneyPot** *(vystupujete na Internetu pod 2 veřejnými IP. Z jedna IP je vyhrazená na komunikaci a druhá je tzv. Honeypot - návnada pro roboty - úpravě firewallových pravidel a dodatečné ochraně veřejných IP adres) (reputace IP)*

- Narušování dostupnosti k datům (ransomware)
  - **Zašifrování uživatelských dat typu .docx .pdf .jpg** (binární soubory většinou bývají nedotknuty = systém běží) je požadováno výkupné za vaše data. Hackerský kodex vyžaduje, aby po zaplacení byla data zpřístupněna.

Rizika:

    Přílohy v emailu
    Data na flashce
    Obecně soubory se škodlivým kódem

Ochrana:

    Kvalitní záloha dat
    Segmentace počítačové sítě



Poškození HW nebo SW

Malware = škodlivý software. Účelem takového programu je v principu pouze škodit (krádež informací, zhrzený zaměstnanec, naštvaný klient, pro zábavu - žertovné viry, dokázat si něco...)

Typy malwaru:

    Vir  

    potřebuje hostitelský soubor, replikuje sám sebe na další a další soubory

    Červ

    Nepotřebuje hostitele

    Samostatný program, který sám a bez asistence uživatele hledá skulinky v počítačové síti a váže se na různé pakety

    Trojský kůň

    Nešíří se a nereplikuje se na rozdíl od viru či červa v případě nasazení samotným uživatelem číhá na svůj okamžik útoku

    downloader, backdoor, zloděj hesel (password-stealing), dropper

    Spyware, Adware

    Scareware (straší klienta, že byl nakažen a donutí ho ke koupit další software)

    Keylogger (viz výše)

Ochrana:

    Antivir

    IT gramotnost

    Aktualizace (exploit)



Ovlivnění třetí stranou

     Ovlivňování dotyčného po psychické stránce, po stránce celosvětového názoru, po stránce jeho potřeb aj. (Spyware)

Rizika:

    Psychický teror

    Zkreslené představy

    Manipulace s osobou

Ochrana:

    ???
