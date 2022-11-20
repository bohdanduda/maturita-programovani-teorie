#procedury, funkce
## Parametry
* dělí se na hodnotové `struct` a odkazové `class`
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


