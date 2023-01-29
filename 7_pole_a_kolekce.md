# pole a kolekce

## definice pole
* neuspo��dan� posloupnost prvk� stejn�ho typu, prvky pole jsou ulo�eny v souvisl�m bloku pam�ti a pro p��stup k nim slou�� celo��seln� index 
* pole deklarujeme zad�n�m typu jeho prvk�

* p��klad pole s hodnotou int s 10ti prvky
```
int[] intArray = new int[10];
```

## princip

## ulo�en� v RAM

## rozd�l pol� a kolekc�
* pole jsou u�ite�n�j�� pro pr�ci s pevn�m po�tem objekt�
* kolekce se na rozd�l od pol� m��e dynamicky zv�t�ovat a zmen�ovat podle pot�eb aplikace, u n�kter�ch kolekc� se m��e p�i�adit kl�� k libovoln�mu objektu aby se pot� objekt mohl rychle na��st
* kolekce je t��da, tak�e se pou�it� mus� deklarovat instance

## v�hody a nev�hody

## indexy
* index je ozna�en� itemu v poli, nebo kolekci
* pomoc� index� m��eme lehce naj�t danou hodnotu v poli

## 2D/3D pole
* pole mohou b�t i v�cerozm�rn�
* dvourozm�rn� pole si m��eme p�edstavit jako tabulku

* deklarace dvourozm�rn�ho pole s 4mi ��dky a 2mi sloupci
```
int[,] array = new int[4, 2];
```
* deklarace trojrozm�rn�ho pole
```
int[,,] array1 = new int[4, 2, 3];
```

## list
* kolekce objekt� kter� lze volat pomoc� indexu, do listu se daj� za b�hu programu p�id�vat, nebo tak� odstra�ovat hodnoty
* metody a prvky t��dy `List`

`Add()` - p�id� nov� prvek do listu

`Clear()` - vyma�e v�echny prvky

`Contains()` - vr�t� `true`, pokud list obsahuje dan� prvek

`CopyTo()` - umo��uje zkop�rovat prvky z listu do pole

`IndexOf()` - vr�t� index prvn�ho v�skytu dan�ho prvku v listu

`Insert()` - vlo�� na dan� index nov� prvek (dal�� posloupn�)

`Remove()` - vyma�e dan� prvek

`RemoveAt()` - vyma�e prvek na dan�m indexu 

## dictionary
* kolekce kl��� a hodnot stejn�ho typu
* ka�d� kl�� mus� b�t unik�tn�, tak� nesm� b�t null pokud je hodnota reference

* p��klad stringov�ho slovn�ku
```
Dictionary<string,string> states = new Dictionary<string,string>();
```