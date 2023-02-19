# datové struktury
* představují konkrétní způsob organizace dat v paměti počítače, který zajišťuje, aby mohla data být používána efektivně. Datová struktura umožňuje uchovávat a zpracovávat množinu dat stejného typu nebo různorodých, ale logicky souvisejících dat
## zásobník
* datová struktura, používaná pro dočasné ukládání dat
* prvek lze ze zásobníku vyjmout pouze v případě, že "je na řadě"
* hodnotu prvku můžeme ale přečíst kdykoli (prvek zůstane na místě)
* data uložená v zásobníku poslední, budou odstraněna jako první __LIFO__ ("Last In - First Out")
* přidání prvku do zásobníku se nazývá __PUSH__ operace
* odstranění se nazývá __POP__ operace
* poslední prvek má atribut __TOP__
## fronta
* data uložena jako první budou odstraněna jako první __FIFO__ ("First In – First Out")
* přidání prvku do zásobníku se nazývá __ENQUEUE__ operace
* odstranění se nazývá __DEQUEUE__ operace
* ve frontě se sleduje vždy první a poslední prvek mají atributy (__FRONT__) a (__REAR__)
## sigly-linked list
* list, jehož prvky můžeme procházet jen jedním směrem: Head-to-Tail
* každý prvek linked listu se nazývá __NODE__, obsahuje data a pointer k dalšímu prvku, což pomáhá udržovat strukturu listu
## doubly-linked list
* list, jehož prvky jsou také ukládány ve formě __NODE__
* každý __NODE__ v listu obsahuje 3 sub-elementy: 
1. datovou část, která obsahuje hodnotu elementu
2. link k předchozímu __NODE__
3. link k dalšímu __NODE__

## principy a použití

## implementace fronty zásobníku v poli a ve spojovém seznamu

* příklad implementace zásobníku v poli
```
        private int top;
        private int[] array;

        public Stack(int size)
        {
            top = -1;
            array = new int[size];
        }

        public void Push(int item)
        {
            if (top > array.Length - 1)
            {
                throw new Exception("Stack is full");
            }
            array[++top] = item;
        }

        public int Peek()
        {
            if (top == -1)
            {
                throw new Exception("Stack is empty");
            }
            return array[top];
        }

        public int Pop()
        {
            if (top == -1)
            {
                throw new Exception("Stack is empty");
            }
            return array[top--];
        }
```

* příklad implementace fronty v poli
```
internal class Queue
    {
        private int front;
        private int rear;
        private int[] array;

        public Queue(int size)
        {
            front = 0;
            rear = -1;
            array = new int[size];
        }

        public void Enqueue(int item)
        {
            if (rear == array.Length-1)
            {
                throw new Exception("Queue is full");
            }
            array[++rear] = item;
        }

        public int Dequeue()
        {
            if (front > rear)
            {
                throw new Exception("Queue is empty");
            }
            int item = array[front];
            front++;
            return item;
        }

        public int Peek()
        {
            if (front > rear)
            {
                throw new Exception("Queue is empty");
            }
            return array[front];
        }
    }
```    
