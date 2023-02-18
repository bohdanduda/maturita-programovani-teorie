# UML
## popis UML
* UML (Unified Modeling Language) je soubor grafických notací, který se používá pøi vývoji softwaru
* Vyvinula ho firma Rational Software v 90. letech

## základní diagramy
* diagramy se dìlí na 2 základní skupiny: 

* __Diagramy struktury__ (Structure Diagrams) - Popisují strukturu systému, tedy z èeho je složený
* __Diagramy chování__ (Behaviour Diagram) - Popisují chování systému, tedy jak funguje
* diagram chování má ještì samostatnou skupinu: 
* __Diagramy interakce__ (Interaction diagrams) - Popisují interakci mezi jednotlivými èástmi systému

![](images/diagrams.png)

## Class diagram a význam jednotlivých symbolù v kódu
* Diagram tøíd popisuje statickou strukturu systému, znázoròuje datové struktury a operace u objektù a souvislosti mezi objekty

* Znázoròuje datový model systému od konceptuální úrovnì až po implementaci
* Datové struktury zaøazuje do tøíd a zobrazuje vztahy tìchto tøíd
* Je hlavním stavebním kamenem objìktovì orientovaného modelování, používá se jak pro bìžné koncepèní modelování, tak i k detailnímu modelování èi pøevodu modelù do programového kódu
* Další souèástí tøíd jsou také symboly, které __oznaèují viditelnost__ jednotlivých èástí diagramu a tøíd
![](images/uml_relationship.png)

* Další dùležitý pojem je __multiplicita__ (mohutnost) vztahù
* Udává kolik instancí jedné tøídy mùže být svázáno s instancí tøídy druhé
![](images/uml_multiplicity.png)

* Vztahy: 
```
Na úrovni instance:

Závislost (Dependency)
Asociace (Association)
Agregace (Aggregation)
Kompozice, složení (Composition)

Na úrovni tøídy:

Dìdiènost (Generalization)
Realizace (Realization)
Závislost (Dependency)
```
## UseCase diagram
* __Diagram pøípadù užití__ zachycuje vnìjší pohled na modelovaný systém a tím pomáhá odhalit hranice systému a slouží jako podklad pro odhady rozsahu

* Jde o posloupnost souvisejících transakcí mezi úèastníkem (zpravidla uživatelem v urèité roli, ale také jiným systémem) a systémem bìhem vzájemného dialogu
* Hlavním úèelem je zachycení aktérù, kteøí se systémem komunikují a vztahù mezi službami a tìmi, kterým jsou poskytovány, a to vizuální i textovou podobou
![](images/uml_useCase.png)
## State diagram
* __Stavový diagram__ je zpùsob grafického zápisu vývoje systému, který má koneèný poèet stavù

* Takovým systémem mùže být koneèný automat (stavový automat) èi další podobné systémy, které vyjadøují stavy urèitého objektu a pøechody (pøechodovou funkci) mezi nimi.
* Diagram poskytuje sadu elementù pro popis chování systému, který je vyjádøen prùchodem stavy a je øízen vnìjším vstupem. 

TODO: https://cs.wikipedia.org/wiki/Stavov%C3%BD_diagram

## Sequence diagram
* __Sekvenèní diagram__ zachycuje èasovì uspoøádanou posloupnost zasílání zpráv mezi objekty
* nejèastìji znázoròuje spolupráci nìkolika vzorových objektù v rámci jednoho pøípadu užití

VZHLED:
* Jednotlivé procesy èi objekty zapojené do popisovaného pøípadu užití jsou umístìn v horní èásti diagramu
* Od nich pak vedou smìrem dolù èáry (lifelines), které znázoròují bìh èasu
* Mezi èarami jsou pak zakresleny vodorovné šipky rùzných typù, které reprezentují zprávy posílané mezi objekty, plné šipky znaèí volání, pøerušované pak odpovìï, podlouhlé obdélníky na svislých èarách vyznaèují dobu zpracovávání dané zprávy èi èekání na odpovìï
![](images/uml_sequence.png)