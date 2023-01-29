# datové struktury
## zásobník
* datová struktura, používaná pro doèasné ukládání dat
* prvek lze ze zásobníku vyjmout pouze v pøípadì, že "je na øadì"
* hodnotu prvku mùžeme ale pøeèíst kdykoli (prvek zùstane na místì)
* data uložená v zásobníku poslední, budou odstranìna jako první __LIFO__ ("Last In - First Out")
* pøidání prvku do zásobníku se nazývá __PUSH__ operace
* odstranìní se nazývá __POP__ operace
* poslední prvek má atribut __TOP__
## fronta
* data uložena jako první budou odstranìna jako první __FIFO__ ("First In – First Out")
* pøidání prvku do zásobníku se nazývá __ENQUEUE__ operace
* odstranìní se nazývá __DEQUEUE__ operace
* ve frontì se sleduje vždy první a poslední prvek mají atributy (__FRONT__) a (__REAR__)
## sigly-linked list
* list, jehož prvky mùžeme procházet jen jedním smìrem: Head-to-Tail
* každý prvek linked listu se nazývá __NODE__, obsahuje data a pointer k dalšímu prvku, což pomáhá udržovat strukturu listu
## doubly-linked list
* list, jehož prvky jsou také ukládány ve formì __NODE__
* každý __NODE__ v listu obsahuje 3 sub-elementy: 
1. datovou èást, která obsahuje hodnotu elementu
2. link k pøedchozímu __NODE__
3. link k dalšímu __NODE__

## principy a použití

## implementace fronty zásobníku v poli a ve spojovém seznamu
