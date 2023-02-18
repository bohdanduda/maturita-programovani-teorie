# UML
## popis UML
* UML (Unified Modeling Language) je soubor grafick�ch notac�, kter� se pou��v� p�i v�voji softwaru
* Vyvinula ho firma Rational Software v 90. letech

## z�kladn� diagramy
* diagramy se d�l� na 2 z�kladn� skupiny: 

* __Diagramy struktury__ (Structure Diagrams) - Popisuj� strukturu syst�mu, tedy z �eho je slo�en�
* __Diagramy chov�n�__ (Behaviour Diagram) - Popisuj� chov�n� syst�mu, tedy jak funguje
* diagram chov�n� m� je�t� samostatnou skupinu: 
* __Diagramy interakce__ (Interaction diagrams) - Popisuj� interakci mezi jednotliv�mi ��stmi syst�mu

![](images/diagrams.png)

## Class diagram a v�znam jednotliv�ch symbol� v k�du
* Diagram t��d popisuje statickou strukturu syst�mu, zn�zor�uje datov� struktury a operace u objekt� a souvislosti mezi objekty

* Zn�zor�uje datov� model syst�mu od konceptu�ln� �rovn� a� po implementaci
* Datov� struktury za�azuje do t��d a zobrazuje vztahy t�chto t��d
* Je hlavn�m stavebn�m kamenem obj�ktov� orientovan�ho modelov�n�, pou��v� se jak pro b�n� koncep�n� modelov�n�, tak i k detailn�mu modelov�n� �i p�evodu model� do programov�ho k�du
* Dal�� sou��st� t��d jsou tak� symboly, kter� __ozna�uj� viditelnost__ jednotliv�ch ��st� diagramu a t��d
![](images/uml_relationship.png)

* Dal�� d�le�it� pojem je __multiplicita__ (mohutnost) vztah�
* Ud�v� kolik instanc� jedn� t��dy m��e b�t sv�z�no s instanc� t��dy druh�
![](images/uml_multiplicity.png)

* Vztahy: 
```
Na �rovni instance:

Z�vislost (Dependency)
Asociace (Association)
Agregace (Aggregation)
Kompozice, slo�en� (Composition)

Na �rovni t��dy:

D�di�nost (Generalization)
Realizace (Realization)
Z�vislost (Dependency)
```
## UseCase diagram
* __Diagram p��pad� u�it�__ zachycuje vn�j�� pohled na modelovan� syst�m a t�m pom�h� odhalit hranice syst�mu a slou�� jako podklad pro odhady rozsahu

* Jde o posloupnost souvisej�c�ch transakc� mezi ��astn�kem (zpravidla u�ivatelem v ur�it� roli, ale tak� jin�m syst�mem) a syst�mem b�hem vz�jemn�ho dialogu
* Hlavn�m ��elem je zachycen� akt�r�, kte�� se syst�mem komunikuj� a vztah� mezi slu�bami a t�mi, kter�m jsou poskytov�ny, a to vizu�ln� i textovou podobou
![](images/uml_useCase.png)
## State diagram
* __Stavov� diagram__ je zp�sob grafick�ho z�pisu v�voje syst�mu, kter� m� kone�n� po�et stav�

* Takov�m syst�mem m��e b�t kone�n� automat (stavov� automat) �i dal�� podobn� syst�my, kter� vyjad�uj� stavy ur�it�ho objektu a p�echody (p�echodovou funkci) mezi nimi.
* Diagram poskytuje sadu element� pro popis chov�n� syst�mu, kter� je vyj�d�en pr�chodem stavy a je ��zen vn�j��m vstupem. 

TODO: https://cs.wikipedia.org/wiki/Stavov%C3%BD_diagram

## Sequence diagram
* __Sekven�n� diagram__ zachycuje �asov� uspo��danou posloupnost zas�l�n� zpr�v mezi objekty
* nej�ast�ji zn�zor�uje spolupr�ci n�kolika vzorov�ch objekt� v r�mci jednoho p��padu u�it�

VZHLED:
* Jednotliv� procesy �i objekty zapojen� do popisovan�ho p��padu u�it� jsou um�st�n v horn� ��sti diagramu
* Od nich pak vedou sm�rem dol� ��ry (lifelines), kter� zn�zor�uj� b�h �asu
* Mezi �arami jsou pak zakresleny vodorovn� �ipky r�zn�ch typ�, kter� reprezentuj� zpr�vy pos�lan� mezi objekty, pln� �ipky zna�� vol�n�, p�eru�ovan� pak odpov��, podlouhl� obd�ln�ky na svisl�ch �ar�ch vyzna�uj� dobu zpracov�v�n� dan� zpr�vy �i �ek�n� na odpov��
![](images/uml_sequence.png)