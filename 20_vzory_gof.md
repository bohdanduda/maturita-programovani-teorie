# návrhové vzory gof
* Návrhové vzory poskytují reálná řešení běžných problémů s návrhem softwaru, které se vyskytují při práci s malými nebo podnikovými aplikacemi
* GoF - gang of four (Čtyři autoři této funkce)
* Návrhové vzory poskytují zobecněné řešení ve formě šablon, které lze aplikovat na reálné problémy a efektivně je řešit
## Tovární metoda (Factory Method)
__Vytvoří instanci několika odvozených tříd__
* Tovární metoda je vzor, který poskytuje rozhraní pro vytváření objektů v nadtřídě, ale umožňuje podtřídám měnit typ objektů, které budou vytvořeny.
* Vzor Tovární metoda navrhuje nahradit přímé volání konstrukce objektu (pomocí operátoru new) voláním speciální tovární metody
* Tovární metodu bychom měli použít pokud nastane situace, že na více místech vytvářímě stejný objekt
## Jedináček (Singleton)
__Třída, jejíž instance může existovat pouze jedna__
* Singleton je návrhový vzor, který umožňuje zajistit, aby třída měla pouze jednu instanci, a zároveň poskytuje globální přístupový bod k této instanci
* Tím ale porušuje pravidlo: Single Responsibility Principle
* Využijeme třeba v případě kdy chceme mít jednu instanci dostopnou všem klientům: databázový objekt, sdílený různými částmi programu
* Třída nemá parametry
* Implementace __Singletonu__:
```
private static readonly Singleton _instance = new();
        
public static Singleton GetSingletonInstance()
{
    return _instance;
}
```
* Vytvoříme privátnní statickou readonly instanci třídy, kterou rovnou inicializujeme
* Poté implemetujeme veřejnou statickou metodu, která vrací danou instanci
* Instance se nikdy nepřepíše, od startu programu do konce, bude obsahovat instanci třídy Singleton
* Pro přístup k instanci použijeme metodu __GetSingletonInstance__

## Příkaz (Command)
__Zapouzdření požadavku na příkaz jako objektu__
* Návrhový vzor Command je návrhový vzor __chování__, který z požadavku vytvoří samostatný objekt obsahující všechny informace o požadavku.
* To umožňuje např. parametrizovat klienty s různými požadavky, řadit požadavky do fronty nebo je zaznamenávat a podporovat operace, které lze zrušit
* Vzor se skládá ze 4 částí (tříd): __třída Invoker__ - třída která vyvolá nějakou metodu; __Command třída/rozhraní__ - třída, nebo rozhraní, v které je definovaná metoda Commandu; __kontrétní třídy Commandu__ - třídy které zpracovávají požadavky a dědí z rozhraní __commandu__; a nakonec __reciever třída__ - obsahuje logiku aplikace
* V normálním případě bychom použili na zpracování požadavku rovnou třídu __reciever__, v případě použítí vzoru Command její metody a data "extrahujeme" do konkrétní třídy commandů, kde se zpracují.

https://code-maze.com/command/
## Pozorovatel (Observer)
 __Způsob oznamování změn v řadě tříd__
* Observer je návrhový vzor __chování__, který umožňuje definovat mechanismus odběru pro upozornění více objektů na všechny události, které se stanou s objektem, který pozorují
* Vzor se dělí na 2 části: objekt který je sledován - __Observable__ a objekt který ho sleduje __Observer__
* Příklad jednoduché implementace observeru:
 ```
 Alarm alarm = new();
alarm.Subscribe(new FireStation());
alarm.Dispose();
alarm.Dispose();
alarm.Dispose();
alarm.Dispose();
alarm.Dispose();

// Objekt, který sledujeme
// Observable "odesílá" sledovanou hodnotu v našem případě int 
public class Alarm : IObservable<int>, IDisposable
{
    List<IObserver<int>> watchers = new();

    // Metody Subscribe a Dispose se vygenerují po podědění z rozhraní

    public IDisposable Subscribe(IObserver<int> observer)
    {
        watchers.Add(observer);
        return this;
    }

    int i = 0;

    public void Dispose()
    {
        if (i > 3)
        {
            watchers.ForEach(x => x.OnCompleted());
            return;
        }

        watchers.ForEach(x => x.OnNext(i++));
    }
}

// Objekt, který sleduje sledovaný objekt
// Observer sleduje hledanou hodnotu - int
public class FireStation : IObserver<int>
{
    // Metody se vygenerují po podědění z rozhraní

    public void Alert(Alarm value)
    {
        Console.WriteLine($"{nameof(FireStation)} RESPONDING!");
    }

    public void OnCompleted()
    {
        Console.WriteLine($"{nameof(FireStation)} COMPLETE!");
    }

    public void OnError(Exception error)
    {
        Console.WriteLine($"{nameof(FireStation)} ERROR!");
    }

    public void OnNext(int value)
    {
        Console.WriteLine($"{nameof(FireStation)} next: {value}");
    }
}
 ```
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
