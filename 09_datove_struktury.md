# datov� struktury
## z�sobn�k
* datov� struktura, pou��van� pro do�asn� ukl�d�n� dat
* prvek lze ze z�sobn�ku vyjmout pouze v p��pad�, �e "je na �ad�"
* hodnotu prvku m��eme ale p�e��st kdykoli (prvek z�stane na m�st�)
* data ulo�en� v z�sobn�ku posledn�, budou odstran�na jako prvn� __LIFO__ ("Last In - First Out")
* p�id�n� prvku do z�sobn�ku se naz�v� __PUSH__ operace
* odstran�n� se naz�v� __POP__ operace
* posledn� prvek m� atribut __TOP__
## fronta
* data ulo�ena jako prvn� budou odstran�na jako prvn� __FIFO__ ("First In � First Out")
* p�id�n� prvku do z�sobn�ku se naz�v� __ENQUEUE__ operace
* odstran�n� se naz�v� __DEQUEUE__ operace
* ve front� se sleduje v�dy prvn� a posledn� prvek maj� atributy (__FRONT__) a (__REAR__)
## sigly-linked list
* list, jeho� prvky m��eme proch�zet jen jedn�m sm�rem: Head-to-Tail
* ka�d� prvek linked listu se naz�v� __NODE__, obsahuje data a pointer k dal��mu prvku, co� pom�h� udr�ovat strukturu listu
## doubly-linked list
* list, jeho� prvky jsou tak� ukl�d�ny ve form� __NODE__
* ka�d� __NODE__ v listu obsahuje 3 sub-elementy: 
1. datovou ��st, kter� obsahuje hodnotu elementu
2. link k p�edchoz�mu __NODE__
3. link k dal��mu __NODE__

## principy a pou�it�

## implementace fronty z�sobn�ku v poli a ve spojov�m seznamu
