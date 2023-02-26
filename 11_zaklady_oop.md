# základy OOP
## třída
* datová struktura, která spojuje datové proměnné a funkce do jednoho celku
* instancím tříd se říka objekty
* třída je pouze objektový konstruktor, nebo "blueprint" pro vytvoření objektu...
## instance
* proměnná libovolného typu obsažená ve třídě nebo struktuře
* slouží k ukládání dat objektu
* pole instancí představují data třídy, která umožňují objektu udržovat jeho stav
## vlastnosti
* atributy, které charakterizují třídy
* vlastnosti se chovají jako pole, na rozdíl od polí jsou však implementovány pomocí __accessorů__ (definují příkazy prováděné při přístupu, nebo přiřezení vlastnosti)
## metody
* metody jsou bloky kódů nebo příkazů v programu, které dávají uživateli možnost opakovaně používat stejný kód, což šetří spotřebu paměti, působí jako úspora času a hlavně zajišťuje lepší čitelnost kódu
* syntnaxe deklarace metody:
```
<Access_Modifier> <return_type> <method_name>([<param_list>])
     public	       void	   Vypocitej  (int x, int y)
```
## zapouzdření
* zapouzdření je definováno jako zabalení dat do jedné jednotky, je to mechanismus, který spojuje kód a data, s nimiž manipuluje
* při zapouzdření jsou proměnné nebo data třídy skryty před jakoukoli jinou třídou a lze k nim přistupovat pouze prostřednictvím některé členské funkce vlastní třídy, v níž jsou deklarovány
* Např. když v konstruktoru provazujeme vlastnosti třídy s parametry konstruktoru, dále už je nemůžeme měnit, jen číst

	https://www.geeksforgeeks.org/c-sharp-encapsulation/
## modifikátory přístupu
* modifikátory přístupu jsou klíčová slova používaná k určení deklarované přístupnosti člena nebo typu
* `public` - kód je přístupný pro všechny třídy
* `private` - kód je přístupný jen pro třídu samotnou
* `protected` - kód je přístupný jen pro třídu samotnou, nebo pro třídu která je dědičná
* `internal` - kód je přístupný pouze v rámci vlastní sestavy
## konstruktor
* metoda použita k inicializaci objektů
* nemá žádný návratový typ
* mouhou přijímat parametry, které jsou použity k inicializaci polí
* mýže být přetížen
