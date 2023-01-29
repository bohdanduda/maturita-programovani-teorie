# rekurze
## definice
* rekurze je programovací technika, pøi níž je urèitá procedura nebo funkce znovu volána døíve, než je dokonèeno její pøedchozí volání
* použití rekurze mùže u nìkterých úloh vést ke struènému a matematicky elegantnímu øešení (napø. výpoèet faktoriálu)... nevede ale nutnì k øešení optimálnímu
## vztah rekurzivního a iterativního algoritmu
## pøíklady rekurze
```
public int FindFactorial(int inputNumber)
{
	if(inputNumber == 1)
	{
		return inputNumber;
	}
	return inputNumber * FindFactorial(inputNumber-1);
}
```
* Funkci ``FindFactorial()`` voláme znova ještì pøed tím, než byla dokonèena, proto je pøíklad __rekurzivní__