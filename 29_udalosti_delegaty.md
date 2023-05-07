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
* Observer je návrhový vzor __chování__, který umožňuje definovat mechanismus odběru pro upozornění více objektů na všechny události, které se stanou s objektem, který pozorují
* Vzor se dělí na 2 části: objekt který je sledován - __Observable__ a objekt který ho sleduje __Observer__
* Příklad využití: sledování zabití ve hře - sledujeme objekt, který když nabyde nějaké hodnoty, tak observer spustí danou událost
## Lambda funkce
* zkrácený zápis metody
## anonymní funkce/objekty
* Anonymní objekt je účinná možnost jak zapozdřit read-only parametry do jednoho objektu, bez toho, abysme museli specifikovat jeho typ.
* Anonymní objekt vytvoríme specifikováním `new` operátoru v inicializaci objektu
* Příklad implementace anonymního objektu: `var anonymousObject = new { Amount = 420, Message = "Blaze it!" };`
* Parametry vypíšeme jako kdybysme je vypisovaly z normálního objektu: `Console.WriteLine($"Amount: {anonymousObject.Amnout} Message: {anonymousObject.Message} ");`
## dynamické typy (var, dynamic)
* Dynamický typ je datový typ proměnné, u kterého nemusíme specifikovat co je žač... typ var nebo dynamic sám pozná podle hodnoty proměnné co je zač.
* Rozdíl mezi var a dynamic je takový že při spuštění __musí být proměnná var inicializována__. __Dynamic nemusí__.
