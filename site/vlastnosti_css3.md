# Vlastnosti CSS3 - přehled, rozbor na příkladech
*ono jako dostaneme příklad na kterém to budeme rozebírat ale tady jsou nějaký chytáky na které se bude ptát*
**Přehled vlastností:**

**Border:radius** – umožňuje zaoblit objekt, nastavují se dvě hodnoty(horizontální a vertikální) nebo se každý roh objektu nastavuje sám(10px 20px 50px 45px), pokud se nastavují všechny 4 rohy zvlášť nastavují se v tomhle pořadí ( 1 – levý horní roh, 2 – pravý horní roh, 3 – pravý dolní roh a 4 – levý dolní roh).

**Box-shadow** – umožnuje posun stínu objektu, nastavují se 4 hodnoty. První hodnota slouží k nastavení posunu stínu horizontálně. Druhá hodnota slouží k nastavení posunu stínu vertikálně. Třetí hodnota slouží k nastavení okraje stínu. A poslední čtvrtá hodnota slouží k nastavení barvy stínu.

**Text-shadow –** umožňuje posun stínu u textu (zbytek je stejný jako u box-shadow)

**Transform:**

**1. translate** – slouží k nastavení 2D pohybu objektu po ose x(objekt se při kladné hodnotě posune doprava pokud je hodnota záporná posune se doleva) a y(objekt se posune při kladné hodnotě dolů a při záporné hodnotě se posune nahoru)

**2.scale** – slouží k zvětšení objektu(hodnota 1 je standartní velikost, hodnota 2 je dvojnásobná velikost a 0.5 je poloviční velikost

**3. rotate** – otočí objekt podle hodinových ručiček, hodnota se udává ve stupních.

**Opacity** – tato vlastnost má pouze jednu hodnotu <0,1> číslo nula je 100% průhlednost a číslo jedna je 0% průhlednost. Tento efekt se používá až na konečný stav objektu.

**RGBA** – je to funkce pro nastavení barev, píšou se čtyři hodnoty (20(červená), 50(zelená), 10(modrá) a 0.5(průhlednost))

HSL

**1.Hue(odstín)** – je to nastavení základních barev <0, 360> 0 a 360 je červená barva, 120 zelená a 240 modrá.

**2.Saturation(nasycení)** – určuje se v procentech 100% je maximální barevnost a 0% je minimální.

**3.Lightness(světlost)** – určuje se v procentech a 0% je tmavá, 100%  je světlá a 50% je průměr

**HSLA** – Stejné jako HSL jen je tam navíc A což znamená průhlednost

**Multiple columns** – pomocí funkce column-count rozdělí text do určitého počtu sloupců které se řadí vedle sebe
