# Události a delegáty
#### Události
* Nativní implementace Observera
* Sleduje objekt, když se změní jeho hodnota, zavolá _Handler_ metodu 

#### Delegáti
* delegát je v podstatě funkce v proměnné
* v instanci musí být klíčové slovo `delegate`
* instance delegátu textové funkce:
* ```public delegate string StringDelegate(string text)```
## delegáty Action/Func/Predicate
* __Action__ - univerzální delegát
* __Func__ - univerzální delegát, pro metody, které vrací hodnotu
* návratový typ u Func je vždy na konci
* delklarace func:
* ```Func<string, int, bool> func``` - funkce, který bere string, int a vrací bool
* __Predicate__ - vždy bere pouze jeden parametr a vrací boolean
## Observer
## Lambda funkce
* zkrácený zápis metody
## anonymní funkce/objekty

## dynamické typy (var, dynamic)
