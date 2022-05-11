# IPv4, subsíťování, supersíťování
IP adresa
je to jedinečná adresa počítače v síti. S IP adresou se pracuje na 3 vrstvě modelu ISO/OSI a účastní se procesu směrování (routing)
IP adresa je rozdělena na dvě základní části
•	adresa sítě
•	adresa zařízení
Druhy IP adres
•	IPv4 (4Bajtová)
•	IPv6 (16Bajtová)

IP je datově orientovaný protokol, který je používán v sítích s směrování paketů (ethernet). Jde o protokol přepravující data bez záruky, tzn negarantuje doručení, zachování pořadí ani vyloučení duplicit, to je ponecháno vyšší vrstvě, kterou představuje protokol TCP
IPv4 poskytuje omezený  adresní prostor, teoreticky cca 4 miliardy adres
Třídy IPv4:
(definují jaká poměrná část z 4(16)bajtů je věnována adrese sítě nebo adrese zařízení)
•	Archaické rozdělení
o	třída A (první bajt v rozmezí 0-127) př.: 5.5.5.5
1bajt pro adresu sítě, 3bajty na adresu zařízení (128 sítí / 16mil zařízení)
o	třída B (první bajt v rozmezí 128-191) př.: 150.0.0.1
2bajty pro adresu sítě, 2bajty na adresu zařízení (64x256 sití / 256x256)
o	třída C (první bajt v rozmezí 192-223) př.: 199.10.10.1
3bajty pro sít, 1bajt pro zařízení (32x256x256 sítí, 256 zařízení)
o	třída D (multicastingové vysílání)
•	Současnost využívá CIDR rozdělení adresy sítě a zařízení
CIDR (Classless Inter Domain Routing)
Zde vstupuje do role síťová maska:
o	v desitkové soustavě: 255.255.0.0
o	v CIDR notaci: nejaká_ip_adresa/16 (maska obsahuje 16 jedniček, zbytek nuly)
Subsíťování
Podsíť (anglicky subnet, subnetwork) je v informatice označení pro samostatnou část počítačové sítě. Označením podsíť je obvykle míněna konkrétní (menší) vyčleněná část větší IP sítě. Pro určení rozsahu IP adres v dané podsíti slouží maska sítě. Rozdělení sítě na dvě nebo více menších podsítí je v angličtině označováno jak subnetting.
Supersíťování
Supernetting, je síť IP, který je vytvořena pro účely směrování (routování) z kombinace dvou nebo více síťí (podsítí taky) do větší sítě, Proces supernetu se nazývá supernetting. Supernetting v rámci Internetu slouží jako strategie, aby se zabránilo topologické fragmentaci prostoru adres IP pomocí hierarchického alokačního systému, který deleguje řízení segmentů adresního prostoru na regionální poskytovatele síťových služeb.


Vyhrazené IP:
•	rozsahy definované pro vnitřní síte
o	10.x.x.x
o	172.168.x.x až 172.192.x.x
o	192.168.x.x
•	adresy sítě a broadcasty
•	loopback adresa (127.x.x.x)
