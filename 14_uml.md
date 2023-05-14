# UML
## popis UML
* UML (Unified Modeling Language) je soubor grafických notací, který se používá při vývoji softwaru
* dá se také využít v post-vývojové práci
* Vyvinula ho firma Rational Software v 90. letech

## základní diagramy
* diagramy se dělí na 2 základní skupiny: 

* __Diagramy struktury__ (Structure Diagrams) - Popisují strukturu systému, tedy z čeho je složený
* __Diagramy chování__ (Behaviour Diagram) - Popisují chování systému, tedy jak funguje
* diagram chování má ještě samostatnou skupinu: 
* __Diagramy interakce__ (Interaction diagrams) - Popisují interakci mezi jednotlivými částmi systému

![](images/diagrams.png)

## Class diagram a význam jednotlivých symbolů v kódu
* Diagram tříd popisuje statickou strukturu systému, znázorňuje datové struktury a operace u objektů a souvislosti mezi objekty

* Znázorňuje datový model systému od konceptuální úrovně až po implementaci
* Datové struktury zařazuje do tříd a zobrazuje vztahy těchto tříd
* Je hlavním stavebním kamenem objěktově orientovaného modelování, používá se jak pro běžné koncepční modelování, tak i k detailnímu modelování či převodu modelů do programového kódu
* Další součástí tříd jsou také symboly, které __označují viditelnost__ jednotlivých částí diagramu a tříd
![](images/uml_relationship.png)

* Další důležitý pojem je __multiplicita__ (mohutnost) vztahů
* Udává kolik instancí jedné třídy může být svázáno s instancí třídy druhé

#### Multiplicita:
```
1 - Třída bude jenom jedna
1..* - One-to-many: Nekonečně možno tříd
0..* - One-to-many nullable: Nebude žádná nebo 1, nebo n
0..1 - Zero to one: Možnost (buď bude existovat, nebo ne)
n - Specifický počet tříd které budou existovat
```

#### Vztahy: 
```
Na úrovni instance:

Závislost (Dependency) - Třída je závislá na druhé. Čerchováná šipka otevřená
Asociace (Association) - Třídy spolu mají nějaký vztah. Jednoduchá čara
Agregace (Aggregation) - Speciální typ asociace, říká že třída může být částí jiné, ale nemusí. Prázdný diamant
Kompozice, složení (Composition) - Dítě nemůže existovat bez rodiče. Plný diamant

Na úrovni třídy:

Dědičnost (Generalization, Inheritance) - Třída dědí z jiné. Prázdná šipka k třídě z které dědí
Realizace (Realization) - Třída implementuje z rozhraní
Závislost (Dependency) - Třída je závislá na druhé. Čerchováná šipka otevřená
```
## UseCase diagram
* __Diagram případů užití__ zachycuje vnější pohled na modelovaný systém a tím pomáhá odhalit hranice systému a slouží jako podklad pro odhady rozsahu
* Skládá se ze 3 částí:
   1. Actor - uživatel
   2. System Boundary - hranice systému, samotný program
   3. UseCase - scénář užití

* čára s otevřenou šipkou - include (dávat pozor na směry) - zprava do leva (povinně se zahrne do scénáře), zprava do leva - extend (volitelně rozšiřuje)
* k diagramu je vždycky potřeba dokument, který slovně popisuje projekt 
* Jde o posloupnost souvisejících transakcí mezi účastníkem (zpravidla uživatelem v určité roli, ale také jiným systémem) a systémem během vzájemného dialogu
* Hlavním účelem je zachycení aktérů, kteří se systémem komunikují a vztahů mezi službami a těmi, kterým jsou poskytovány, a to vizuální i textovou podobou
![](images/uml_useCase.png)
## State diagram
* __Stavový diagram__ je způsob grafického zápisu vývoje systému, který má konečný počet stavů

* Takovým systémem může být konečný automat (stavový automat) či další podobné systémy, které vyjadřují stavy určitého objektu a přechody (přechodovou funkci) mezi nimi.
* Diagram poskytuje sadu elementů pro popis chování systému, který je vyjádřen průchodem stavy a je řízen vnějším vstupem. 

TODO: https://cs.wikipedia.org/wiki/Stavov%C3%BD_diagram

## Sequence diagram
* __Sekvenční diagram__ ukazuje nám, jak spolu objekty v aplikaci, nebo třídy v kódu interagují
* zachycuje časově uspořádanou posloupnost zasílání zpráv mezi objekty
* nejčastěji znázorňuje spolupráci několika vzorových objektů v rámci jednoho případu užití

VZHLED:
* Skládá se z dvou typů objektů:
1. Aktor - Symbol stickmana
2. Objekt - Obdélník. Objekty se umisťují v sekvenčím pořadí zprava doleva
* Jednotlivé procesy či objekty zapojené do popisovaného případu užití jsou umístěn v horní části diagramu
* Od nich pak vedou směrem dolů čáry (lifelines), které znázorňují běh času
* Mezi čarami jsou pak zakresleny vodorovné šipky různých typů, které reprezentují zprávy posílané mezi objekty, plné šipky značí volání, přerušované pak odpověď, podlouhlé obdélníky na svislých čarách vyznačují dobu zpracovávání dané zprávy či čekání na odpověď
* Nezapomenout na alternativní zprávy (obdélník kde je situace 2 scenárií)
![](images/uml_sequence.png)
