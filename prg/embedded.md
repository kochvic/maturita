# Embedded systémy a Arduino

## Embedded systémy (vystavěné systémy)
Na rozdíl od všeobecně použitelného počítače (například osobního) jsou vestavěné systémy navrženy pro konkrétní činnosti. Některé také pracují v reálném čase, protože zpoždění činnosti nebo akce ovládané řídícím procesorem může mít fatální následky nebo poruchu činnosti včetně nebezpečných stavů (např. zastavení motoru letadla nebo naopak nezastavení motoru ve vlaku či automobilu).

U systémů vyráběných ve velkých sériích, jako například MP3 přehrávačů nebo mobilních telefonů, je většinou jedním z primárních cílů ve fázi návrhu nízká cena. Tvůrci těchto zařízení často používají hardware, který je přesně dostačující pro implementaci požadovaných funkcí. Například digitální přijímač DVB-S pro příjem satelitní televize zpracovává každou sekundu obrovská množství dat, ale zpracování je provedeno v zákaznickém integrovaném obvodu, který provádí pouze tuto jedinou činnost. Hlavní procesor pouze nastaví a spustí tento proces, případně zobrazuje menu, animace a podobně, k čemuž mu stačí jeho menší výpočetní výkon.

Při malých sériích nebo prototypech (emulátor) vestavěných systémů lze použít hardware osobního počítače a použít pouze konkrétní programy nebo nahradit původní operační systém operačním systémem pracujícím v reálném čase (RTOS).

Software určený pro vestavěné systémy je často označován jako firmware a je uložen v čipech ROM nebo Flash na rozdíl od programů v osobním počítači, které jsou uloženy na pevném disku. Tento software často počítá s omezenými prostředky zařízení – malá nebo žádná klávesnice, omezený nebo žádný displej, malé množství paměti RWM-RAM a podobně.

Řídicí systémy jsou vestavěny do zařízení, od nichž se očekává, že budou schopna pracovat léta bez chyb a v některých případech schopna zotavit se z poruchy. Proto bývají programy většinou vyvíjeny a testovány pečlivěji než programy pro osobní počítače a v návrhu se nepoužívají nespolehlivé mechanické součástky jako disky, přepínače, tlačítka. Zotavení z poruchy může využít například techniky watchdog timeru, který resetuje počítač, pokud program po jistou dobu neupozornil watchdog, že je v pořádku.

**Příklady**

- bankomat
- avionika – například autopilot, hardware a software pro řízení letu a další systémy integrované v letadlech a raketách
- mobilní telefony, jejich základnové stanice (BTS), telefonní ústředny
- řídicí jednotky spalovacích motorů (ECU) a systémy zabraňující blokování brzd (ABS) v automobilech
- domácí automatizace, například termostaty, klimatizace, zavlažovací systémy a zabezpečovací systémy
- kalkulačky
- vybavení domácnosti, například mikrovlnná trouba, pračka, myčka nádobí, televizory, DVD přehrávače, set-top boxy
- zdravotnické přístroje
- ruční počítače (PDA nebo průmyslové)
- herní konzole (PlayStation, Sega, Xbox, GameBoy, Nintendo 64, Nintendo DS)
- digitální náhrada potenciometrů (místo „točítka“ jsou pouze tlačítka přidat/ubrat)
- počítačové periferie jako routery, tiskárny, pevné disky, Wi-Fi karty, modemy, scannery jsou často řízeny vlastním vestavěným systémem a mají proto vlastní firmware

## Arduino

Arduino je otevřená platforma s grafickým vývojovým prostředím, které vychází z prostředí Wiring (podobný projekt jako Arduino, tedy deska s mikrokontrolerem a IDE) a Processing (prostředí pro výuku programování). Arduino bylo poprvé představeno v roce 2005. Může být použito k vytváření samostatných interaktivních zapojení nebo může být připojeno k software na počítači (např. Adobe Flash, Processing, Max/MSP, Pure Data, SuperCollider). Momentálně lze koupit verze, které jsou už zkompletované; schéma a návrh plošného spoje je dostupný pro ty, kteří si chtějí postavit Arduino sami.

Na rozdíl od Raspberry Pi není Arduino zamýšleno jako plnohodnotný stolní počítač. Řídící program je vyvíjen zvlášť (na stolním počítači) a do Arduina je posléze nahrán a spuštěn. Uvnitř Arduina je pak spuštěn jen tento program, který typicky obsahuje smyčku, která se neustále opakuje (Arduino neustále zjišťuje stav svého okolí a na změny reaguje). Díky tomu má nízkou spotřebu (je možné napájení malou baterií) a hodí se například pro řízení dronů, robotů a podobně.
