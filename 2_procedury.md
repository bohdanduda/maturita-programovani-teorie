# procedury, funkce
* Procedura a funkce neboli __metoda__ je blok kódu, který obsahuje řadu příkazů, které se spusí pouze, když je metoda zavolána. Pokud metoda očekává parametry, musíme je jí předat, jinak ke spuštění nedojde.
* Metody používáme nejčastěji k opakovanému použití kódu (jednou kód definujeme, mnohokrát ho použijeme).
* Každá aplikace má vygenerovanou metodu `Main`. Je volána __CLR__(Common Language Runtime) při spoštění programu.
## Parametry
* dělí se na hodnotové `struct` a odkazové `class`, nebo `interface`
* modifikátory `ref` a `out`
* `ref` indikuje že proměnná je reference, nebo alias pro jiný objekt. Proměnná s `ref` musí být inicializována
* `out` funguje podobně jako `ref` jen s tím rozdílem, že proměnná nemusí být inicializována. Volaná metoda je však nutná k přiřazení hodnoty před vrácením metody.

## Rozdíly
* procedura nic nevrací má návratový typ `void`
* funkce je stejná jako procedura, jen vrací nějakou hodnotu. Typ návratové hodnotu musíme uvést v hlavičce funkce.

* příklad procedury:
```
public void SayHello()
{
	Console.WriteLine("Hello");
}
```

* příklad funkce:

```
public int Count(int x, int y)
{
	int result = x + y;
	return result;
}
```
https://learn.microsoft.com/cs-cz/dotnet/csharp/programming-guide/classes-and-structs/methods
## Návratový typ
* Návratový typ funkce určí velikost a typ hodnoty vrácené funkcí a odpovídá specifikátoru typu
* Pokud funkce nemá návratový typ `void`, tak musí vždy vracet nějaký výsledek pomocí `return`
* příklady specifikátorů typu: `void`, `char`, `int`, `double`, `string` atd.
https://learn.microsoft.com/cs-cz/cpp/c-language/return-type?view=msvc-170
## Předávání parametrů do funkce (hodnotou, ref, out)
* Klíčová slova ref a out se v jazyce C# používají k předávání argumentů v rámci metody nebo funkce, obě označují, že __argument/parametr__ je předáván odkazem
* Ve výchozím nastavení jsou parametry předávány metodě hodnotou. Pomocí těchto klíčových slov (ref a out) můžeme předat parametr pomocí reference.
### REF
* Klíčové slovo ref předává argumenty pomocí reference. Znamená to, že všechny změny provedené v metodě s tímto argumentem se projeví v této proměnné, když se řízení vrátí do volající metody
### OUT
* Také jako u `REF` se předávají argumenty pomocí reference. Jediný rozdíl je, že `OUT` nevyžaduje inicialnizaci proměnné
* Podobá se také klíčovému slovu `in` jen s tím rozdílem, že `in` neumožňuje volané metodě měnit hodnotu argumentu
