# rekurze
## definice
* rekurze je programovac� technika, p�i n� je ur�it� procedura nebo funkce znovu vol�na d��ve, ne� je dokon�eno jej� p�edchoz� vol�n�
* pou�it� rekurze m��e u n�kter�ch �loh v�st ke stru�n�mu a matematicky elegantn�mu �e�en� (nap�. v�po�et faktori�lu)... nevede ale nutn� k �e�en� optim�ln�mu
## vztah rekurzivn�ho a iterativn�ho algoritmu
## p��klady rekurze
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
* Funkci ``FindFactorial()`` vol�me znova je�t� p�ed t�m, ne� byla dokon�ena, proto je p��klad __rekurzivn�__