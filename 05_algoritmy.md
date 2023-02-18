# Algoritmy
## vlastnosti
* Aby m�l algoritmus smysl, mus� b�t pln� srozumiteln� pro toho, kdo ho bude vykon�vat
* Proto by m�l spl�ovat n�sleduj�c� vlastnosti:
* __spr�vnost__ - v�stup algoritmu mus� b�t spr�vn�
* __rezultativnost__ - m�dy mus� p�in�st v�sledek (klidn� i hl�en� o chyb�) 
* __kone�nost__ - m�l by m�t jasn� stanoven� d�l�� f�ze kter� vedou z bodu A do bodu B 
* __hromadnost__ - algoritmus mus� b�t aplikovateln� na ur�itou skupinu �loh. Nikdy by nem�l �e�it jen jeden probl�m
* __determinovanost (jednozna�nost)__ - mus� b�t p�esn� dan�, co n�sleduje po spln�n� ur�it�ho kroku
* __opakovatelnost__ - p�i zad�n� stejn�ch vstupn�ch dat mus� algoritmus vr�tit op�t shodn� v�sledek
## vztah algoritm� a programovac�ch jazyk�
## v�po�et asymptotick� slo�itosti (funkce omikron, omega, theta)
* algoritmus je �e�en� na dan� probl�m, 
* funkce __omega__ - nejlep�� sc�n��
* funkce __theta__ - pr�m�rn� sc�n��
* funkce __omikron__ - nejhor�� sc�n��
## algoritmy v poli
### min/max
* p��klad hled�n� min/max hodnoty
```
int[] array1 = { 1, 2, 3, 4, 5, };

int max = array1[0];
int min = array1[0];

for (int i = 1; i < array1.Length; i++)
{
    if (array1[i] > max)
    {
        max = array1[i];
    }

    if (array1[i] < min)
    {
        min = array1[i];
    }
}
```
* nebo pou��t funkci `Max()` a `Min()` :relaxed:
#### <hr>
### oto�en� (reverse array)
* p��klad algoritmu oto�en�
```
static void Main(string[] args)
{
    int[] array = { 1, 2, 3, 4, 5, };
    int arrayLenght = array.Length;

    for (int i = 0; i < arrayLenght/2; i++)
    {
        Swap(array, i, arrayLenght - i - 1);
    }   
}

public static void Swap(int[] array, int x, int y)
{
    int temporary = array[x];
    array[x] = array[y];
    array[y] = temporary;
}
```
#### <hr>
### vkl�d�n�
* p��klad algoritmu vkl�d�n�
```
int x = 23;
int positionToBeInserted = 3;
            
int[] oldArray = {1,2,3,4,5,6,7,8,9,10};
int[] newArray = new int[oldArray.Length + 1];
            
for (int i = 0; i < oldArray.Length + 1; i++)
{
    if (i < positionToBeInserted - 1)
    {
        newArray[i] = oldArray[i];
    }
    else if (i == positionToBeInserted -1)
    {
        newArray[i] = x;
    }
    else
    {
        newArray[i] = oldArray[i - 1];
    }
}
```
### line�rn� vyhled�v�n�
* p��klad line�rn�ho vyhled�v�n�
```
int[] array = { 1, 2, 3, 4, 5 };
int target = 2;
            
for (int i = 0; i < array.Length; i++)
{
    if (target == array[i])
    {
        Console.WriteLine(i + 1);
    }
}
```
### bin�rn� vyhled�v�n�
```
int[] array = { 1, 2, 3, 4, 5 };
            
int low = 0;
int high = array.Length;
int mid = 0;

int target = 2;
            
while (low <= high)
{
    mid = (low + high) / 2;

    if (target > array[mid])
    {
        Console.WriteLine(target+mid);
        break;
    }
    else if (target > array[mid])
    {
        low = mid + 1;
    }
    else
    {
        high = mid - 1;
    }
}
```
## �ad�c� algoritmy
### bubble sort
* Bubble Sort je jednoduch� t��dic� algoritmus, kter� je zalo�en� na porovn�v�n�, p�i kter�m se porovn�v� ka�d� dvojice sousedn�ch prvk� a prvky se prohod�, pokud nejsou v po�ad�
```
int[] array = { 108, 23, 69, 420, 9 };
int temporary;

for (int j = 0; j <= array.Length - 2; j++)
{
    for (int i = 0; i <= array.Length - 2; i++)
    {
        if (array[i] > array[i + 1])
        {
            temporary= array[i + 1];
            array[i + 1] = array[i];
            array[i] = temporary;
        }
    }
}

Console.WriteLine("Se�azeno:");
foreach (int p in array)
{
    Console.Write($"{p} ");
}
Console.ReadLine();
```
##### <hr>
### selection sort
* Selection Sort je t��d�c� algoritmus, funguje tak, �e je seznam rozd�len na dv� ��sti
* v jedn� ��sti jsou v�echny prvky set��d�n� a v druh� ��sti jsou polo�ky neset��d�n�
* Nejprve z pole vybereme maxim�ln� nebo minim�ln� hodnoty, po z�sk�n� hodnot (�ekn�me nejmen��ch) je um�st�me na za��tek seznamu tak, �e hodnoty na prvn�m m�st� nahrad�me nejmen��mi hodnotami. Po proveden� se pole zmen�� 
##### <hr>
### insertion sort
* Insertion Sort je jednoduch� t��dic� algoritmus, kter� sestavuje v�sledn� set��d�n� pole po jednotliv�ch polo�k�ch pomoc� porovn�v�n�.
* Na velk�ch seznamech je mnohem m�n� efektivn� ne� pokro�ilej�� algoritmy, jako je quicksort, heapsort nebo merge sort
```
int[] array = new int[10] { 23, 9, 85, 12, 99, 34, 60, 15, 100, 1 };
int n = 10;
int value;
int flag;

for (int i = 1; i < n; i++)
{
    value = array[i];
    flag = 0;
    for (int j = i - 1; j >= 0 && flag != 1;)
    {
        if (value < array[j])
        {
            array[j + 1] = array[j];
            j--;
            array[j + 1] = value;
        }
        else flag = 1;
    }
}
Console.Write("Se�azeno: ");
for (int i = 0; i < n; i++)
{
    Console.Write(array[i] + " ");
}
```
##### <hr>
### quick sort
* �azen� Quick Sort se prov�d� tak, �e se seznam rozd�l� na dv� ��sti
* Zpo��tku se pomoc� rozd�lovac�ho algoritmu vybere oto�n� prvek (pivot)
* V lev� ��sti pivotu jsou ulo�eny men�� hodnoty ne� pivot a v prav� ��sti v�t�� hodnoty
* Po rozd�len� se ka�d� samostatn� seznam rozd�l� stejn�m postupem
##### <hr>
### merge sort
* Merge Sort je rekurzivn� t��dic� algoritmus, kter� pou��v� metody `Divide()` a `Conquer()`
* Rozd�l� pole na dv� ��sti a pak zavol� s�m sebe pro ka�dou z t�chto dvou ��st�
* Tento proces pokra�uje, dokud nen� pole set��d�no
* Je dobr� pro t��d�n� __Linked List�__
* je stabiln�, co� znamen�, �e stejn� prvky v poli si zachov�vaj� sv� p�vodn� vz�jemn� pozice
##### <hr>
### heap sort
* Heap Sort je t��dic� algoritmus, kter� vyu��v� datovou strukturu haldy
* Poka�d� se odstran� ko�enov� prvek haldy, tj. nejv�t�� prvek, a ulo�� se do pole
* Je nahrazen listov�m prvkem nejvzd�len�j��m zprava a pot� je halda znovu vytvo�ena
* To se prov�d� tak dlouho, dokud v hald� nez�stane ��dn� dal�� prvek a pole nen� set��d�no
```
public static void Main()
{
    int[] array = {55, 25, 89, 34, 12, 19, 78, 95, 1, 100};
    int n = 10, i;
    HeapSort(array, 10);
    Console.Write("Se�azeno: ");
    for (i = 0; i < n; i++)
    {
        Console.Write(array[i] + " ");
    }
    Console.ReadKey();
}
    static void HeapSort(int[] array, int n)
    {
        for (int i = n / 2 - 1; i >= 0; i--)
        {
            Heapify(array, n, i);
        }

        for (int i = n-1; i>=0; i--)
        {
            int temporary = array[0];
            array[0] = array[i];
            array[i] = temporary;

            Heapify(array, i, 0);
        }
    }

    static void Heapify(int[] array, int n, int i)
    {
        int largest = i;
        int left = 2 * i + 1;
        int right = 2 * i + 2;

        if (left < n && array[left] > array[largest])
        {
            largest = left;
        }
        
        if (right < n && array[right] > array[largest])
        {
            largest = right;
        }

        if (largest != i) 
        {
            int swap = array[i];
            array[i] = array[largest];
            array[largest] = swap;
            Heapify(array, n, largest);
        }
    }
```
## stabilita �azen�
*https://cs.wikipedia.org/wiki/�adic�_algoritmus*
## implementace jednoduch�ch algoritm�