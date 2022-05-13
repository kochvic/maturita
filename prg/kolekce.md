# Kolekce v jazyce JAVA

Kolekce v jazyce Java patří hlavně **seznamy** a **množiny**. Hlavním rozdílem mezi seznamem a množinou je, že když vložíme prvek do množiny dvakrát, v množině bude stále jen jeden, zatímco do seznamu se prvek vloží jeden za druhý. Množina se chová jako standardní matematická množina, množiny jsou si rovny právě tehdy, mají-li stejné všechny prvky.

## Seznam

Deklarace
```java
List<Object> jmenoPromenne = new ArrayList<Object>();
```

Základní metody pro práci se seznamem jsou především:

- add
- remove
- contains
- iterator

Příklad
```java
cars.add(new Car("3G6 9909"));
for (Iterator<Car> i = cars.iterator(); i.hasNext();) {
    Car car = i.next();
    if (car.getLabel().contains("3G6 9909")) {
        i.remove();
    }
}
```
## Množiny

Deklarace
```java
Set<Object> jmenoPromenne = new HashSet<Object>();
```

Základní metody pro práci s množinami jsou především:

- add
- remove
- contains
- iterator

Příklad
```java
public Collection<Object> getSomething() {
    Collections.unmodifiableSet(promennaTypuMnozina);
}
```
