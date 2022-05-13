# Zpracování událostí (MouseEvent, KeyEvent, ActionEvent, WindowEvent, aj.)

-	Událostně řízené programování - složitější (dobré mít tester)
-	obecně můžeme za událost označit interakci uživatele s GUI (např. klepnutí na myš, stisk klávesy na klávesnici, pohyb kurzorem, aj.
-	Událost v jazyce JavaFX je reprezentována objektem třídy javafx.event.Event nebo kteroukoliv její podtřídou.

Vlastnosti události:
-	Zdroj události (prvek GUI, který volá obslužný program)
-	Cíl události (předpokládejte že dojte ke klepnutí myši nad objektem Circle, tím pádem je objekt třídy Circle cílem události)
-	Typ události (definuje typ události)
-	když se v aplikaci vyskytne nějaká událost, zpravidla provádíte nějaké zpracování provedením kusu kódu,
-	část kódu, který je spuštěn v reakci na událost, je známý jako obslužný program události (komfortní metody) nebo událostní filtr

**Event (třida)** - Reprezentuje událost, její podtřídy reprezentují konkrétní typy událostí (WindowEvent, MouseEvent, KeyEvent aj.)
**EventTarget (rozhraní)** - Instance implementující toto rozhraní je cílem udalosti
**EventType (třída)** - Instance této třidy definuje typ události (MOUSE_PRESSED, KEY_RELEASED aj.)
**EventHandler (rozhraní)** - Instance tohoto rozhraní představuje obslužnou rutinu událost nebo událostní filtr. Jeho metoda handle() se volá při události, kterou byl zaznamenán.

Událostní filter
-	Procházení stromu UI prvků od kořene (Stage) až po cíl události (Node)
-	Zastavení procházení stromem můžeme provést přes metodu consume()
-	node.addEventFilter(EventType.XXXX, metoda) // napojeni obslužného programu na node
Událostní handler (komfortní medota)
-	Procházení stromu UI prvků od cíle události (Node) až po Stage
-	Zastavení procházení stromem můžeme provést přes metodu consume()
```java
	node.addEventHandler(EventType.XXXX, metoda) //napojení obslužného programu na node
	node.setOnMouseClicked(XXX) //komfortní metody
```

Př:

```java
Circle circle = new Circle (100, 100, 50);
EventHandler<MouseEvent> aHandler = e-> System.out.print("Mouse event type: " + e.getEventType());

circle.addEventFilter(MouseEvent.MOUSE_CLICKED, aHandler);
circle.addEventHandler(MouseEvent.MOUSE_CLICKED, aHandler);
circle.setOnMouseClicked(aHandler);
```
