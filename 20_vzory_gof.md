# návrhové vzory gof
* Návrhové vzory poskytují reálná řešení běžných problémů s návrhem softwaru, které se vyskytují při práci s malými nebo podnikovými aplikacemi
* GoF - gang of four (Čtyři autoři této funkce)
* Návrhové vzory poskytují zobecněné řešení ve formě šablon, které lze aplikovat na reálné problémy a efektivně je řešit
## Tovární metoda (Factory Method)
__Vytvoří instanci několika odvozených tříd__
* Tovární metoda je návrhový vzor, který poskytuje rozhraní pro vytváření objektů v nadtřídě, ale umožňuje podtřídám měnit typ objektů, které budou vytvořeny.
* Vzor Tovární metoda navrhuje nahradit přímé volání konstrukce objektu (pomocí operátoru new) voláním speciální tovární metody
## Jedináček (Singleton)
__Třída, jejíž instance může existovat pouze jedna__
* Singleton je návrhový vzor, který umožňuje zajistit, aby třída měla pouze jednu instanci, a zároveň poskytuje globální přístupový bod k této instanci
* Tím ale porušuje pravidlo: Single Responsibility Principle
* Využijeme třeba v případě kdy chceme mít jednu instanci dostopnou všem klientům: databázový objekt, sdílený různými částmi programu
## Příkaz (Command)
__Zapouzdření požadavku na příkaz jako objektu__
* Návrhový vzor Command je návrhový __vzor chování__, který z požadavku vytvoří samostatný objekt obsahující všechny informace o požadavku.
* To umožňuje např. parametrizovat klienty s různými požadavky, řadit požadavky do fronty nebo je zaznamenávat a podporovat operace, které lze zrušit
## Pozorovatel (Observer)
 __Způsob oznamování změn v řadě tříd__
* Observer je návrhový vzor chování, který umožňuje definovat mechanismus odběru pro upozornění více objektů na všechny události, které se stanou s objektem, který pozorují
## Iterator
__Postupný přístup k prvkům kolekce__
Iterátor je návrhový vzor chování, který umožňuje procházet prvky kolekce, aniž by byla odhalena její základní reprezentace (seznam, zásobník, strom atd.)
## State
__Změna chování objektu při změně jeho stavu__
* Stav je návrhový vzor chování, který umožňuje objektu změnit své chování, když se změní jeho vnitřní stav. Vypadá to, jako by objekt změnil svou třídu.
## Decorator
__Dynamické přidávání odpovědností k objektům__
* Dekorátor je strukturální návrhový vzor, který umožňuje připojit k objektům nové chování umístěním těchto objektů do speciálních obalových objektů, které obsahují chování.
## Memento
__Zachycení a obnovení vnitřního stavu objektu__
* Memento je návrhový vzor chování, který umožňuje uložit a obnovit předchozí stav objektu, aniž by byly odhaleny podrobnosti jeho implementace
## Adapter
__Shoda rozhraní různých tříd__
* Adaptér je konstrukční vzor, který převádí růzdné typy rozhraní na jiné, podle očekávání. Tento návrhový vzor umožňuje spolupráci tříd, které by jinak nemohly fungovat kvůli nekompatibilním rozhraním

### https://refactoring.guru/design-patterns
### https://www.dofactory.com/net/design-patterns
