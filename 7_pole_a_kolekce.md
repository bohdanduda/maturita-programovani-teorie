# pole a kolekce

## definice pole
* neuspoøádaná posloupnost prvkù stejného typu, prvky pole jsou uloženy v souvislém bloku pamìti a pro pøístup k nim slouží celoèíselný index 
* pole deklarujeme zadáním typu jeho prvkù

* pøíklad pole s hodnotou int s 10ti prvky
```
int[] intArray = new int[10];
```

## princip

## uložení v RAM

## rozdíl polí a kolekcí
* pole jsou užiteènìjší pro práci s pevným poètem objektù
* kolekce se na rozdíl od polí mùže dynamicky zvìtšovat a zmenšovat podle potøeb aplikace, u nìkterých kolekcí se mùže pøiøadit klíè k libovolnému objektu aby se poté objekt mohl rychle naèíst
* kolekce je tøída, takže se použití musí deklarovat instance

## výhody a nevýhody

## indexy
* index je oznaèení itemu v poli, nebo kolekci
* pomocí indexù mùžeme lehce najít danou hodnotu v poli

## 2D/3D pole
* pole mohou být i vícerozmìrná
* dvourozmìrné pole si mùžeme pøedstavit jako tabulku

* deklarace dvourozmìrného pole s 4mi øádky a 2mi sloupci
```
int[,] array = new int[4, 2];
```
* deklarace trojrozmìrného pole
```
int[,,] array1 = new int[4, 2, 3];
```

## list
* kolekce objektù které lze volat pomocí indexu, do listu se dají za bìhu programu pøidávat, nebo také odstraòovat hodnoty
* metody a prvky tøídy `List`

`Add()` - pøidá nový prvek do listu

`Clear()` - vymaže všechny prvky

`Contains()` - vrátí `true`, pokud list obsahuje daný prvek

`CopyTo()` - umožòuje zkopírovat prvky z listu do pole

`IndexOf()` - vrátí index prvního výskytu daného prvku v listu

`Insert()` - vloží na daný index nový prvek (další posloupnì)

`Remove()` - vymaže daný prvek

`RemoveAt()` - vymaže prvek na daném indexu 

## dictionary
* kolekce klíèù a hodnot stejného typu
* každý klíè musí být unikátní, také nesmí být null pokud je hodnota reference

* pøíklad stringového slovníku
```
Dictionary<string,string> states = new Dictionary<string,string>();
```