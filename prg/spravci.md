# Správci rozložení (FlowPane, GridPane, VBox, aj.)

**Co je správce rozložení:**
objekt (kontejner) který předem definovaným způsobe se stará o **uspořádání** objektů k sobě přidružených.

```java
XXXPane.getChildren.add(objekt)
```
**JavaFX = Stage –> Scena –> RootPane (správce rozložení) –> Pane (správci rozložení)**

![](Aspose.Words.f96474f9-1a95-4199-83d3-caa3be162652.001.png)

- **FlowPane –** Skládá uzly za sebou tak, jak jsou přidávány do panelu, buď horizontálně nebo vertikálně. Na nový řádek se nezalamuje, pokud se nevejde na řádek lze zmenšit(minWidth). Umožnuje nastavení velikosti mezer mezi prvky (Hgap, Vgap). Může se nastavit pozice prvků (setAlignment()). Při horizontálním nastavení lze nastavit zarovnání řádky (setRowValigment()).

- **HBox/VBox** – Lze skládat prvky do jedné řady buď horizontálně (HBox), nebo vertikálně (VBox).

- **BorderPane** – Většinou základ aplikace. Prostor se dělí na pět oblastí. Horní(top) a spodní(bottom) má pevnou výšku a pohyblivou šířku. Levý(left) a pravý(right) má pevnou šířku a pohyblivou výšku. Střed(center) vyplňuje zbylí prostor. Funkce pro ovládaní borderpane: setLeft, setCenter, setTop, setBottom, setRight.

![](Aspose.Words.f96474f9-1a95-4199-83d3-caa3be162652.002.png)

- **AnchorPane** – Lze kotvit prvky ke stranám panelu (top, right, bottom, left). K jedné pozici se může kotvit více prvků a jeden prvek lze kotvit na více míst.

- **TitlePane –** Je to pravidelná mřížka, která má preferovaný počet řádků a sloupců. Orientaci. Rozestupy(Hgap, Vgap) Dále má preferovanou velikost(setPrefTileWidth) a Zarovnání dílu(setTileAlignment). Potomkům můžeme nastavit vlastní zarovnání a okraje.

- **GridPane –** Je nejsložitější, protože má nepravidelnou mřížku a uzly mohou zabírat několik řádků nebo sloupců. Nastavuje se pomocí setAlignment (zarovnání), setVgap/setHgap (odsazení), setPadding(new Insets(5,5,5,5)) – okraje. Metody pro vkládání: add(node, column,row,colspan,rowspan)
```Java
addRow()
addColumn()
```
- **StackPane –** Uzly se ukládají na sebe jako balíček karet. Používají se k vytvoření složitých objektů (nápis na obrázku). U potomků je možné nastavit zarovnání a okraje. Snaží se zvětšit prvky na jejich maxSize.

- **TitledPane a Accordion –** TitledPane slouží jako rozbalovací panel a Accordion jako seskupení. Do Accordion lze vložit libovolné množství TitledPane – getPanes().addAll(…).

TitledPane není klasický panel. Lze nastavit jen jednoho potomka, ale může to být další panel. Nikdy se nenastavuje výška.

- **Bez layoutu – Pane –** Nemá žádný layoutovací algoritmus, prvky do něj vkládáme a pozicujeme jsou absolutními souřadnicemi.

**Všechny Node mají metody**

relocate (x, y) – preferovaný způsob umístění
setLayoutX (x)/setLayoutY(y)
setTranslateX(s) – posunutí x o s
setTranslateY(s) – posunutí y o s

Souřadnice se vždy nastavují vzhledem k pravému hornímu rohu rodiče.

Jeden daný konkrétní Node, může patřit pouze jednomu panelu (správci rozmístění)
