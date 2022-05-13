# JavaFX Node — Label, Button, TogeleButton, Textfield, aj.

Node-prvek kde je převážná část UI uložena v balíčku **javafx.scene.control**
Lze jim nastavovat vzhled pomocí CSS, integrovaná podpora animací, transformací, efektů apod.

### Label
Popisek, označení, jedná se o needitovatelný text který má 3 konstruktory
•	pro prázdný popisek
•	popisek s jednoduchým textem (setText()/getText())
•	ikonou a textem (setGraphics() / getGraphics())
se dá rotovat, posunout, zvětšit, změnit animaci, a dá se zabalit text (wrapping).
setAligement() - nemá bez wrappingu smysl
Pro manuální dělení řádků použít node Text.
### Button
Bezestavové tlačítko, kde jeho třída Button umožnuje zpracovat akci (onAction()), když uživatel klepce na tlačítko.
Button má 3 konstruktory stejné jako Label.
Primární funkcí každého tlačítka je vytvoření akce po kliknutí. Připojení rukojetí události přes metodu setOnAction(), je možné ho také stylovat pomocí CSS interně i externě (setStyleClass nebo setStyle).
### ToggleButton / CheckBox / RadioButton
Přepinací tlačítko, může být vybrán nebo zrušen. Dvě nebo více přepínacích tlačítek lze kombinovat do jedné skupiny (ToggleGroup), kde lze vybrat pouze jedno tlačítko nebo kde není požadován žádný výběr.
Na ToggleButton se dají vázat stejné události jako na Button.
TextField
třída TextField implementuje ovladací prvek UI, který přijímá a zobrazuje zadávaní textu.
Poskytuje funkce pro příjem textu od uživatele (getText() /setText())
Konstruktor může být prázdný nebo může obsahovat String jako vzor textu v TextFieldu.
ComboBox
