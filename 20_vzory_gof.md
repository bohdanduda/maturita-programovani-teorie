# navrhované vzory gof
* Návrhové vzory poskytují reálná øešení bìžných problémù s návrhem softwaru, které se vyskytují pøi práci s malými nebo podnikovými aplikacemi
* GoF - gang of four (Ètyøi autoøi této funkce)
* Návrhové vzory poskytují zobecnìné øešení ve formì šablon, které lze aplikovat na reálné problémy a efektivnì je øešit
## Tovární metoda (Factory Method)
__Vytvoøí instanci nìkolika odvozených tøíd__
* Tovární metoda je návrhový vzor, který poskytuje rozhraní pro vytváøení objektù v nadtøídì, ale umožòuje podtøídám mìnit typ objektù, které budou vytvoøeny.
* Vzor Tovární metoda navrhuje nahradit pøímé volání konstrukce objektu (pomocí operátoru new) voláním speciální tovární metody
## Jedináèek (Singleton)
__Tøída, jejíž instance mùže existovat pouze jedna__
* Singleton je návrhový vzor, který umožòuje zajistit, aby tøída mìla pouze jednu instanci, a zároveò poskytuje globální pøístupový bod k této instanci
* Tím ale porušuje pravidlo: Single Responsibility Principle
* Využijeme tøeba v pøípadì kdy chceme mít jednu instanci dostopnou všem klientùm: databázový objekt, sdílený rùznými èástmi programu
## Pøíkaz (Command)
__Zapouzdøení požadavku na pøíkaz jako objektu__
* Návrhový vzor Command je návrhový __vzor chování__, který z požadavku vytvoøí samostatný objekt obsahující všechny informace o požadavku.
* To umožòuje napø. parametrizovat klienty s rùznými požadavky, øadit požadavky do fronty nebo je zaznamenávat a podporovat operace, které lze zrušit
## Pozorovatel (Observer)
 __Zpùsob oznamování zmìn v øadì tøíd__
* Observer je návrhový vzor chování, který umožòuje definovat mechanismus odbìru pro upozornìní více objektù na všechny události, které se stanou s objektem, který pozorují
## Iterator
__Postupný pøístup k prvkùm kolekce__
Iterátor je návrhový vzor chování, který umožòuje procházet prvky kolekce, aniž by byla odhalena její základní reprezentace (seznam, zásobník, strom atd.)
## State
__Zmìna chování objektu pøi zmìnì jeho stavu__
* Stav je návrhový vzor chování, který umožòuje objektu zmìnit své chování, když se zmìní jeho vnitøní stav. Vypadá to, jako by objekt zmìnil svou tøídu.
## Decorator
__Dynamické pøidávání odpovìdností k objektùm__
* Dekorátor je strukturální návrhový vzor, který umožòuje pøipojit k objektùm nové chování umístìním tìchto objektù do speciálních obalových objektù, které obsahují chování.
## Memento
__Zachycení a obnovení vnitøního stavu objektu__
* Memento je návrhový vzor chování, který umožòuje uložit a obnovit pøedchozí stav objektu, aniž by byly odhaleny podrobnosti jeho implementace
## Adapter
__Shoda rozhraní rùzných tøíd__
* Adaptér je konstrukèní vzor, který pøevádí rùzdné typy rozhraní na jiné, podle oèekávání. Tento návrhový vzor umožòuje spolupráci tøíd, které by jinak nemohly fungovat kvùli nekompatibilním rozhraním

### https://refactoring.guru/design-patterns
### https://www.dofactory.com/net/design-patterns