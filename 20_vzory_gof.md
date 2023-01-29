# navrhovan� vzory gof
* N�vrhov� vzory poskytuj� re�ln� �e�en� b�n�ch probl�m� s n�vrhem softwaru, kter� se vyskytuj� p�i pr�ci s mal�mi nebo podnikov�mi aplikacemi
* GoF - gang of four (�ty�i auto�i t�to funkce)
* N�vrhov� vzory poskytuj� zobecn�n� �e�en� ve form� �ablon, kter� lze aplikovat na re�ln� probl�my a efektivn� je �e�it
## Tov�rn� metoda (Factory Method)
__Vytvo�� instanci n�kolika odvozen�ch t��d__
* Tov�rn� metoda je n�vrhov� vzor, kter� poskytuje rozhran� pro vytv��en� objekt� v nadt��d�, ale umo��uje podt��d�m m�nit typ objekt�, kter� budou vytvo�eny.
* Vzor Tov�rn� metoda navrhuje nahradit p��m� vol�n� konstrukce objektu (pomoc� oper�toru new) vol�n�m speci�ln� tov�rn� metody
## Jedin��ek (Singleton)
__T��da, jej� instance m��e existovat pouze jedna__
* Singleton je n�vrhov� vzor, kter� umo��uje zajistit, aby t��da m�la pouze jednu instanci, a z�rove� poskytuje glob�ln� p��stupov� bod k t�to instanci
* T�m ale poru�uje pravidlo: Single Responsibility Principle
* Vyu�ijeme t�eba v p��pad� kdy chceme m�t jednu instanci dostopnou v�em klient�m: datab�zov� objekt, sd�len� r�zn�mi ��stmi programu
## P��kaz (Command)
__Zapouzd�en� po�adavku na p��kaz jako objektu__
* N�vrhov� vzor Command je n�vrhov� __vzor chov�n�__, kter� z po�adavku vytvo�� samostatn� objekt obsahuj�c� v�echny informace o po�adavku.
* To umo��uje nap�. parametrizovat klienty s r�zn�mi po�adavky, �adit po�adavky do fronty nebo je zaznamen�vat a podporovat operace, kter� lze zru�it
## Pozorovatel (Observer)
 __Zp�sob oznamov�n� zm�n v �ad� t��d__
* Observer je n�vrhov� vzor chov�n�, kter� umo��uje definovat mechanismus odb�ru pro upozorn�n� v�ce objekt� na v�echny ud�losti, kter� se stanou s objektem, kter� pozoruj�
## Iterator
__Postupn� p��stup k prvk�m kolekce__
Iter�tor je n�vrhov� vzor chov�n�, kter� umo��uje proch�zet prvky kolekce, ani� by byla odhalena jej� z�kladn� reprezentace (seznam, z�sobn�k, strom atd.)
## State
__Zm�na chov�n� objektu p�i zm�n� jeho stavu__
* Stav je n�vrhov� vzor chov�n�, kter� umo��uje objektu zm�nit sv� chov�n�, kdy� se zm�n� jeho vnit�n� stav. Vypad� to, jako by objekt zm�nil svou t��du.
## Decorator
__Dynamick� p�id�v�n� odpov�dnost� k objekt�m__
* Dekor�tor je struktur�ln� n�vrhov� vzor, kter� umo��uje p�ipojit k objekt�m nov� chov�n� um�st�n�m t�chto objekt� do speci�ln�ch obalov�ch objekt�, kter� obsahuj� chov�n�.
## Memento
__Zachycen� a obnoven� vnit�n�ho stavu objektu__
* Memento je n�vrhov� vzor chov�n�, kter� umo��uje ulo�it a obnovit p�edchoz� stav objektu, ani� by byly odhaleny podrobnosti jeho implementace
## Adapter
__Shoda rozhran� r�zn�ch t��d__
* Adapt�r je konstruk�n� vzor, kter� p�ev�d� r�zdn� typy rozhran� na jin�, podle o�ek�v�n�. Tento n�vrhov� vzor umo��uje spolupr�ci t��d, kter� by jinak nemohly fungovat kv�li nekompatibiln�m rozhran�m

### https://refactoring.guru/design-patterns
### https://www.dofactory.com/net/design-patterns