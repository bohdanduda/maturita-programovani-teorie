# základy OOP
## tøída
* datová struktura, která spojuje datové promìnné a funkce do jednoho celku
* instancím tøíd se øíka objekty
* tøída je pouze objektovı konstruktor, nebo "blueprint" pro vytvoøení objektu...
## instance
* promìnná libovolného typu obsaená ve tøídì nebo struktuøe
* slouí k ukládání dat objektu
* pole instancí pøedstavují data tøídy, která umoòují objektu udrovat jeho stav
## vlastnosti
* atributy, které charakterizují tøídy
* vlastnosti se chovají jako pole, na rozdíl od polí jsou však implementovány pomocí __accessorù__ (definují pøíkazy provádìné pøi pøístupu, nebo pøiøezení vlastnosti)
## metody
* metody jsou bloky kódù nebo pøíkazù v programu, které dávají uivateli monost opakovanì pouívat stejnı kód, co šetøí spotøebu pamìti, pùsobí jako úspora èasu a hlavnì zajišuje lepší èitelnost kódu
* syntnaxe deklarace metody:
```
<Access_Modifier> <return_type> <method_name>([<param_list>])
     public	       void	   Vypocitej  (int x, int y)
```
## zapouzdøení
* zapouzdøení je definováno jako zabalení dat do jedné jednotky, je to mechanismus, kterı spojuje kód a data, s nimi manipuluje
* pøi zapouzdøení jsou promìnné nebo data tøídy skryty pøed jakoukoli jinou tøídou a lze k nim pøistupovat pouze prostøednictvím nìkteré èlenské funkce vlastní tøídy, v ní jsou deklarovány

	https://www.geeksforgeeks.org/c-sharp-encapsulation/
## modifikátory pøístupu
* modifikátory pøístupu jsou klíèová slova pouívaná k urèení deklarované pøístupnosti èlena nebo typu
* `public` - kód je pøístupnı pro všechny tøídy
* `private` - kód je pøístupnı jen pro tøídu samotnou
* `protected` - kód je pøístupnı jen pro tøídu samotnou, nebo pro tøídu která je dìdièná
* `internal` - kód je pøístupnı pouze v rámci vlastní sestavy
## konstruktor
* metoda pouita k inicializaci objektù
* nemá ádnı návratovı typ
* mouhou pøijímat parametry, které jsou pouity k inicializaci polí
* mıe bıt pøetíen