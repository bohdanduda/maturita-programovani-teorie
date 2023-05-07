# Teorie testování
## Typy testů
* Testování dělíme na 2 základní typy: Unit testy a Itegrační testy
#### Unit testy
* V unit testech testujeme jednotlivé metody třídy... V ideálním případě bychom měli mít otestované všechny use-case business logiky
* Do metody předáváme růzdné kombinace vstupů. Vždy by měli vracet smysluplné hodnoty
* Zárověň bychom měli testovat očekávané chování při zadání neplatných vstupních hodnot 
#### Integrační testy
* V integračních testech testujeme spolupráci dvou nebo více objektů. Testuje se jejich data-flow, konzistence dat a jejich chování
* Itengrační testy obvykle děláme až po Unit testech
## Blackbox/whitebox
* Testy, které předpokládají znalost, či neznalost kódu
### Whitebox - znalost kodu
* U whiteboxu tester zná chování aplikace. Trefujeme se do slabin programu
### Blackbox - neznalost kodu
* U blackboxu tester nezná implementaci kódu, takže nemůže vědět slabiny a nevýhody kódu.
* Testuje jestli se mu vrací správé hodnoty
## Test UI
* testujeme z dvou pohledů - funkční
* funkční - snažíme se zjistit funkčnost celé aplikace. Provádíme buď ručně, nebo automatizovaně (unit testy).
## Usability testy
* Předpokládáme, že aplikace funguje, zajímá nás použitelnost programu.(user friendly)
* Vzorek lidí, kteří aplikaci testujou, poté zpracovat jejich zpětnou vazbu
* Časově i finančně náročné
## Testy výkonu
* Testuje se výkon pod nátlakem - tím že je delší dobu používaná, tak se vše zpomaluje
* Testujeme např. před spuštěním, kolik toho aplikace zvládne
* Najít bottlenecks a odstranit je
* Řešení - algoritmické, nasadit Cache(super rychlé, data ale nemusí být platné, problematika stárnutí dat), Optimalizace na úrovni UI, LoadBallance - přidají se uzly, které budou požadavky zpracovávat
## Profiler
* Nástroj pro měření doby trvání jednotlivých metod - zjistíme co při požadavku trvá nejdéle
## Test Driven Development
* První napíšeme testy, poté píšeme až kód - aplikaci nespouštíme, testujeme je
* Zdlouhavé, nudné, prý o ničem, __dřevácká otrocká práce__
* _"__Práce k ničemu__" - Šibrava 2023_
