# pole a kolekce

## definice pole
* neuspořádaná posloupnost prvků stejného typu, prvky pole jsou uloženy v souvislém bloku paměti a pro přístup k nim slouží celočíselný index 
* pole deklarujeme zadáním typu jeho prvků

* příklad pole s hodnotou int s 10ti prvky
```
int[] intArray = new int[10];
```

## princip

## uložení v RAM
* data pole a kolekce se v paměti ukládají na haldě (__heap__). Pro přístup k nim je na zásobníku (__stack__) odkaz na dané pole nebo kolekci.

## rozdíl polí a kolekcí
* pole jsou užitečnější pro práci s pevným počtem objektů
* kolekce se na rozdíl od polí může dynamicky zvětšovat a zmenšovat podle potřeb aplikace, u některých kolekcí se může přiřadit klíč k libovolnému objektu aby se poté objekt mohl rychle načíst
* kolekce je třída, takže se při použití musí deklarovat instance

## výhody a nevýhody

## indexy
* index je označení itemu v poli, nebo kolekci
* pomocí indexů můžeme lehce najít danou hodnotu v poli

## 2D/3D pole
* pole mohou být i vícerozměrná
* dvourozměrné pole si můžeme představit jako tabulku

* deklarace dvourozměrného pole s 4mi řádky a 2mi sloupci
```
int[,] array = new int[4, 2];
```
* deklarace trojrozměrného pole
```
int[,,] array1 = new int[4, 2, 3];
```

## list
* kolekce objektů stejného typu, které lze volat pomocí indexu, do listu se dají za běhu programu přidávat, nebo také odstraňovat hodnoty
* metody a prvky třídy `List`

`Add()` - přidá nový prvek do listu

`Clear()` - vymaže všechny prvky

`Contains()` - vrátí `true`, pokud list obsahuje daný prvek

`CopyTo()` - umožňuje zkopírovat prvky z listu do pole

`IndexOf()` - vrátí index prvního výskytu daného prvku v listu

`Insert()` - vloží na daný index nový prvek (další posloupně)

`Remove()` - vymaže daný prvek

`RemoveAt()` - vymaže prvek na daném indexu 

## dictionary
* kolekce klíčů a hodnot stejného typu
* každý klíč musí být unikátní, také nesmí být null pokud je hodnota reference

* příklad stringového slovníku
```
Dictionary<string,string> states = new Dictionary<string,string>();
```
