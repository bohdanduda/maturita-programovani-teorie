# Algoritmy
* Algoritmus je přesný postup jak vyřešit daný typ úlohy
## vlastnosti
* Aby měl algoritmus smysl, musí být plně srozumitelný pro toho, kdo ho bude vykonávat
* Proto by měl splňovat následující vlastnosti:
* __správnost__ - výstup algoritmu musí být správný
* __rezultativnost__ - mždy musí přinést výsledek (klidně i hlášení o chybě) 
* __konečnost__ - měl by mít jasně stanovené dílčí fáze které vedou z bodu A do bodu B 
* __hromadnost__ - algoritmus musí být aplikovatelný na určitou skupinu úloh. Nikdy by neměl řešit jen jeden problém
* __determinovanost (jednoznačnost)__ - musí být přesně dané, co následuje po splnění určitého kroku
* __opakovatelnost__ - při zadání stejných vstupních dat musí algoritmus vrátit opět shodný výsledek
## vztah algoritmů a programovacích jazyků
## výpočet asymptotické složitosti (funkce omikron, omega, theta)
* složitost algoritmu se vyjadřuje počtem provedených základních operací (arit. operace, podmínky, přesuny v paměti)
* funkce __omega__ - nejlepší scénář
* funkce __theta__ - průměrný scénář
* funkce __omikron__ - nejhorší scénář
## algoritmy v poli
### min/max
* příklad hledání min/max hodnoty
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
### otočení (reverse array)
* příklad algoritmu otočení
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
* příklad algoritmu vkládání
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
* příklad lineárního vyhledávání
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
## řadící algoritmy
* Řadící algoritmy slouží k setřízení jednotlivých prvků vstupního souboru (obvykle seznamu) dle jejich velikosti
* Při volbě vhodného řadícího algoritmu je třeba dbát na několik kritérií - výkon algoritmu (jeho časová složitost), implementační složitost, vhodnost pro danou datovou strukturu a stabilita algoritmu
### bubble sort
* Bubble Sort je jednoduchý třídicí algoritmus, který je založený na porovnávání, při kterém se porovnává každá dvojice sousedních prvků a prvky se prohodí, pokud nejsou v pořadí
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

Console.WriteLine("Seřazeno:");
foreach (int p in array)
{
    Console.Write($"{p} ");
}
Console.ReadLine();
```
##### <hr>
### selection sort
* Selection Sort je třídící algoritmus, funguje tak, že je seznam rozdělen na dvě části
* v jedné části jsou všechny prvky setříděné a v druhé části jsou položky nesetříděné
* Nejprve z pole vybereme maximální nebo minimální hodnoty, po získání hodnot (řekněme nejmenších) je umístíme na začátek seznamu tak, že hodnoty na prvním místě nahradíme nejmenšími hodnotami. Po provedení se pole zmenší 
##### <hr>
### insertion sort
* Insertion Sort je jednoduchý třídicí algoritmus, který sestavuje výsledné setříděné pole po jednotlivých položkách pomocí porovnávání.
* Na velkých seznamech je mnohem méně efektivní než pokročilejší algoritmy, jako je quicksort, heapsort nebo merge sort
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
Console.Write("Seřazeno: ");
for (int i = 0; i < n; i++)
{
    Console.Write(array[i] + " ");
}
```
##### <hr>
### quick sort
* Řazení Quick Sort se provádí tak, že se seznam rozdělí na dvě části
* Zpočátku se pomocí rozdělovacího algoritmu vybere otočný prvek (pivot)
* V levé části pivotu jsou uloženy menší hodnoty než pivot a v pravé části větší hodnoty
* Po rozdělení se každý samostatný seznam rozdělí stejným postupem
##### <hr>
### merge sort
* Merge Sort je rekurzivní třídicí algoritmus, který používá metody `Divide()` a `Conquer()`
* Rozdělí pole na dvě části a pak zavolá sám sebe pro každou z těchto dvou částí
* Tento proces pokračuje, dokud není pole setříděno
* Je dobrý pro třídění __Linked Listů__
* je stabilní, což znamená, že stejné prvky v poli si zachovávají své původní vzájemné pozice
##### <hr>
### heap sort
* Heap Sort je třídicí algoritmus, který využívá datovou strukturu haldy
* Pokaždé se odstraní kořenový prvek haldy, tj. největší prvek, a uloží se do pole
* Je nahrazen listovým prvkem nejvzdálenějším zprava a poté je halda znovu vytvořena
* To se provádí tak dlouho, dokud v haldě nezůstane žádný další prvek a pole není setříděno
```
public static void Main()
{
    int[] array = {55, 25, 89, 34, 12, 19, 78, 95, 1, 100};
    int n = 10, i;
    HeapSort(array, 10);
    Console.Write("Seřazeno: ");
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
## stabilita řazení
*https://cs.wikipedia.org/wiki/Řadicí_algoritmus*
## implementace jednoduchých algoritmů
