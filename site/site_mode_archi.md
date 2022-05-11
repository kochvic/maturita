# Počítačové sítě - vrstvový model a architektura
Architektura na rozdíl od modelu obsahuje konkrétní protokoly. Protokol je komunikace mezi sousedními vrstvami na stejné úrovni

**Síťový model – ISO/OSI (7 vrstev) - referenční**

7) Aplikační

- definuje druh použití komunikace mezi uzly

6) Prezentační

- prezentaci dat (kódování UTF8, CP1250)

5) Relační

- udržování spojení mezi koncovým a zdrojovým uzlem

4) Transportní

- způsob doručení dat (spojovanou či nespojovanou službu, spolehlivou či nespolehlivou službu)

3) Síťová

- sestavování trasy dat - směrování

2) Linkovou

- zprostředkovává spojení sousedních bodů

1) Fyzická

- jakým způsobem interpretovat 0 a 1

**Síťová architektura – TCP/IP**

\4) Aplikační

- HTTP, HTTPS(19), DNS(18), DHCP(17), FTP, RDP, SSH, TELNET, aj.

\3) Transportní

- UDP, TCP

\2) Síťová

- IP (odkazovat na otázku 15), ARP, RARP, ICMP, IGMP

\1) Vrstva fyzického rozhraní

- Ethernet, TokenRing, ad.
