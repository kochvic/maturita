# JavaFX kontejnery (MenuBar, Menu, ContextMenu, TableView, WebView a.j.)

Menu neboli nabídka.
Sada Nodů (uzlů), která realizuje většinou horní lištu se základními, ale i pokročilými funkcemi aplikace.

## Uzly
### MenuBar
-	uzel, který vytváří lištu nabídky (kořenový node celé nabídky)
-	sám o sobě nemá žádnou fuknci, jenom vytváří prostředí pro další node z nabídky
### Menu
-	základní uzel, který umožňuje pod sebou seskupovat další uzly nabídky včetně sebe samého
-	pokud Menu obsahuje nějaké další uzly, dochází k jeho rozrolování (roletové menu)
-	je možné doplnit o mnemonic funkci (tj. jedno písmeno z nabídky je podtržené a kombinací kláves Alt+to písmenu vyvoláte tuto nabídku)
```java
setMnemonicParsing(true);
```
### MenuItem
-	jedna položka v Menu, není rolovatelná, jedná se o konkrétní operaci
-	defakto se jedná o ekvivalenci pro Button v nabídce
-	je možné definovat akcelerátory (klávesové zkratky)
```java
	menuItem.setAccelerator(KeyCombination.keyCombination(“Shift+Ctrl+F8”));
  ```
### SeparatorMenuItem
-	nemá žádnou funkci
-	je to pouze oddělovač nesouvisejících voleb
### CheckMenuItem / RadioMenuItem
-	obdoba RadioButtonu (1:N) a CheckBox (M:N)

Příklad:
```java
MenuBar mb = new MenuBar();
Menu m = new Menu(“File”);
MenuItem mi= new MenuItem(“Open”);
mi.setAccelerator(KeyCombination.keyCombination(“Ctrl+O”));
m.getItems().add(mi);
mb.getMenus().add(m);
```
Kontextové menu (PopUp menu)

Místo MenuBar používáme objekt typu ContextMenu.
Příklad:
```java
ContextMenu cm = new ContextMenu();
MenuItem mic = new MenuItem(“Clear”);
Menu mc = Menu(“Volby”);
MenuItem micv = MenuItem(“Add”);
mc.getItems().add(micv);
cm.getItems().addAll(mic, mc);
TextField display = new TextField();
display.setOnContextMenuRequested(new EventHander<ContextMenuEvent>(){
  public void handle(ContextMenuEvent e){
    contextMenu.show(display, e.getScreenX(), e.getScreenY());
  }
})
```
