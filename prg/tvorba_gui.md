# Tvorba GUI- principy JavaFX

GUI - grafické uživatelské rozhraní

#### Událostmi řízené programování vs. sekvenční programování
Sekvenční programování vykonává příkazy přesně podle pořadí jak jsou napsány ve zdrojovém kódu. Zatím co událostmi řízené programování provádí operace v závislosti jako uživatel vyvolává událost (pracuje s GUI)

V jave existují knihovny pro GUI: java.awt, javax.swing, javafx

JavaFX je knihovna pro tvorbu GUI
V současné verzi je JavaFX11 s cca 80 nody

**Výhody knihovny JavaFX**:
  -	Rychlejší, efektivnější zpracování (podpora OpenGl, DirectX, práce s vlákny pro více-jádrové CPU)
  -	Podpora gest
  -	Podpora některých multimediální formátů (MP3, WAV, FLV)
  -	Podpora 3D objektů
  -	Definování vzhledu aplikace pomocí CSS
  -	Scene Builder pro generování FXML dokumentu
  -	Podpora animací

**Složení JavaFX aplikace:**
1.	Stage (základní kořená třída, která definuje rám okna)
2.	Scene (třída scene, definuje jaké UI prvky budou obsaženy v Stage)
3.	Pane, Parent, Group (zprávci rozmístění pro UI prvky)
4.	Node (potomci třídy Node - konkrétní UI prvky jako například: Button, Label, Text, TextField, aj.)

**Jak vytvořit JavaFX aplikaci:**
1.	Musíme dědit ze třídy Application
2.	Implementovat metodu start(Stage primaryStage), popřípadě init()
3.	V hlavním těle programu zavolat metodu launch(args);

Nezapomenout v metodě start na konci zobrazit okno -> primaryStage.show()

**Životní cyklus aplikace:**
1.	Spuštění metodou launch()
2.	Vykonání kódu v metodě init()
3.	Vykonaní metody start()
4.	Vykreslení okna - spuštění vlánka pro GUI JavaFX
5.	Konec přichází s voláním metody exit()


```java
public class Main extends Application {

    @Override
    public void start(Stage primaryStage){
  Label lab = new Label("Hello world");
  StackPane sp = new StackPane();
  sp.getChildren().add(lab);
  Scene s = new Scene(sp, 400,300);
  primaryStage.setTitle("Hello World");
  primaryStage.setScene(s);
  primaryStage.show();
    }


    public static void main(String[] args) {
  launch(args);
    }
}//konec tridy
```
