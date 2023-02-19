# rekurze
## definice
* rekurze je programovací technika, při níž je určitá procedura nebo funkce znovu volána dříve, než je dokončeno její předchozí volání
* použití rekurze může u některých úloh vést ke stručnému a matematicky elegantnímu řešení (např. výpočet faktoriálu)... nevede ale nutně k řešení optimálnímu
## vztah rekurzivního a iterativního algoritmu
* každý rekurzivní algoritmus jde napsat podle iterativního a naopak, pro každý jsou ale lepší různé algoritmy
* rekurzivní algoritmus musí mít vždycky koncovou podmínku, jinak dojde k __stack overflow__ - to znamená že algoritmus pokračuje furt dokola, než dojde k přehlcení paměti zásobníku
* rozdíl je, že iterativní algoritmus počítá výsledek _Zdola nahoru_ zatímco rekurzivní naopak
* __Výhody rekurzivního__: jednoduchost a přehlednost.
* __Nevýhody rekurzivního__: časová náročnost, způsobena zbytečným opakováním výpočtu
* přirozeně rekurzivní algoritmus je např. Quick Sort.
### Quick Sort
* Je to nejrychlejší algoritmus na řazení a v praxi se používá k třídění prvků. Funguje dobře jak na velkých, tak na malých polích a je paměťově nenáročný.
* Funguje tak, že označí jeden prvek v poli jako pivot, poté se přesune na konec pole a to se rozdělí na dvě půlky. Obě půlky se poté rekurzivně seřadí.
## příklady rekurze
* Výpočet faktoriálu rekurzivně:
```
public int FindFactorialRecursive(int inputNumber)
{
    if (inputNumber == 0)
    {
	return 1;
    }
    return inputNumber * FindFactorialRecursive(inputNumber - 1);
}
```
* Funkci ``FindFactorial()`` voláme znova ještě před tím, než byla dokončena, proto je příklad __rekurzivní__

* Výpočet faktoriálu iterativně:
```
public int FindFactorialIterative(int inputNumber)
{
    int factorial = 1;
    for (int i = 1; i <= inputNumber; i++)
    {
	factorial = factorial * i;
    }
    return factorial;
}
```
## Doplňky
* Procházení stromové struktury souborového systému - frontou, nebo zásobníkem
