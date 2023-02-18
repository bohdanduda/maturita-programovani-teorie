# Algoritmy
## vlastnosti
* Aby mìl algoritmus smysl, musí být plnì srozumitelný pro toho, kdo ho bude vykonávat
* Proto by mìl splòovat následující vlastnosti:
* __správnost__ - výstup algoritmu musí být správný
* __rezultativnost__ - mždy musí pøinést výsledek (klidnì i hlášení o chybì) 
* __koneènost__ - mìl by mít jasnì stanovené dílèí fáze které vedou z bodu A do bodu B 
* __hromadnost__ - algoritmus musí být aplikovatelný na urèitou skupinu úloh. Nikdy by nemìl øešit jen jeden problém
* __determinovanost (jednoznaènost)__ - musí být pøesnì dané, co následuje po splnìní urèitého kroku
* __opakovatelnost__ - pøi zadání stejných vstupních dat musí algoritmus vrátit opìt shodný výsledek
## vztah algoritmù a programovacích jazykù
## výpoèet asymptotické složitosti (funkce omikron, omega, theta)
* algoritmus je øešení na daný problém, 
* funkce __omega__ - nejlepší scénáø
* funkce __theta__ - prùmìrný scénáø
* funkce __omikron__ - nejhorší scénáø
## algoritmy v poli
### min/max
* pøíklad hledání min/max hodnoty
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
* nebo použít funkci `Max()` a `Min()` :relaxed:
#### <hr>
### otoèení (reverse array)
* pøíklad algoritmu otoèení
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
### vkládání
* pøíklad algoritmu vkládání
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
### lineární vyhledávání
* pøíklad lineárního vyhledávání
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
### binární vyhledávání
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
## øadící algoritmy
### bubble sort
* Bubble Sort je jednoduchý tøídicí algoritmus, který je založený na porovnávání, pøi kterém se porovnává každá dvojice sousedních prvkù a prvky se prohodí, pokud nejsou v poøadí
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

Console.WriteLine("Seøazeno:");
foreach (int p in array)
{
    Console.Write($"{p} ");
}
Console.ReadLine();
```
##### <hr>
### selection sort
* Selection Sort je tøídící algoritmus, funguje tak, že je seznam rozdìlen na dvì èásti
* v jedné èásti jsou všechny prvky setøídìné a v druhé èásti jsou položky nesetøídìné
* Nejprve z pole vybereme maximální nebo minimální hodnoty, po získání hodnot (øeknìme nejmenších) je umístíme na zaèátek seznamu tak, že hodnoty na prvním místì nahradíme nejmenšími hodnotami. Po provedení se pole zmenší 
##### <hr>
### insertion sort
* Insertion Sort je jednoduchý tøídicí algoritmus, který sestavuje výsledné setøídìné pole po jednotlivých položkách pomocí porovnávání.
* Na velkých seznamech je mnohem ménì efektivní než pokroèilejší algoritmy, jako je quicksort, heapsort nebo merge sort
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
Console.Write("Seøazeno: ");
for (int i = 0; i < n; i++)
{
    Console.Write(array[i] + " ");
}
```
##### <hr>
### quick sort
* Øazení Quick Sort se provádí tak, že se seznam rozdìlí na dvì èásti
* Zpoèátku se pomocí rozdìlovacího algoritmu vybere otoèný prvek (pivot)
* V levé èásti pivotu jsou uloženy menší hodnoty než pivot a v pravé èásti vìtší hodnoty
* Po rozdìlení se každý samostatný seznam rozdìlí stejným postupem
##### <hr>
### merge sort
* Merge Sort je rekurzivní tøídicí algoritmus, který používá metody `Divide()` a `Conquer()`
* Rozdìlí pole na dvì èásti a pak zavolá sám sebe pro každou z tìchto dvou èástí
* Tento proces pokraèuje, dokud není pole setøídìno
* Je dobrý pro tøídìní __Linked Listù__
* je stabilní, což znamená, že stejné prvky v poli si zachovávají své pùvodní vzájemné pozice
##### <hr>
### heap sort
* Heap Sort je tøídicí algoritmus, který využívá datovou strukturu haldy
* Pokaždé se odstraní koøenový prvek haldy, tj. nejvìtší prvek, a uloží se do pole
* Je nahrazen listovým prvkem nejvzdálenìjším zprava a poté je halda znovu vytvoøena
* To se provádí tak dlouho, dokud v haldì nezùstane žádný další prvek a pole není setøídìno
```
public static void Main()
{
    int[] array = {55, 25, 89, 34, 12, 19, 78, 95, 1, 100};
    int n = 10, i;
    HeapSort(array, 10);
    Console.Write("Seøazeno: ");
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
## stabilita øazení
*https://cs.wikipedia.org/wiki/Øadicí_algoritmus*
## implementace jednoduchých algoritmù