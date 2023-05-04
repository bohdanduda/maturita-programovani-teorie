# Integrační testy
## Význam integračních testů
* Význam integračního testování se vztahuje k procesu testování rozhraní mezi dvěma komponentami nebo softwarovými moduly s cílem posoudit, jak jsou mezi nimi přenášena data
* Strategie testování integrace umožňují odhalit chyby, které mohou vzniknout při integraci dvou nebo více softwarových modulů, a také vyhodnotit celkovou vhodnost a funkčnost kombinovaných softwarových prvků
* Integrační testy obvykle následují po unit testech. Po zjištění, že každá jednotka funguje samostatně, se v integračním testování posuzuje, jak všechny jednotky fungují dohromady
* Integrační testy jsou závislé na dobře definované specifikaci rozhraní mezi testovanými komponentami. Tyto testy by měly být __co nejvíce automatizované__, aby mohly být často spouštěny a zachytily problémy dříve, než se z nich stanou složité problémy, jejichž oprava v pozdější fázi vývoje zabere čas a prostředky
## Zásady nahraditelnosti
* Nazývá se také __Liskov's notion of a behavioural subtype__ - Poprvé byl zaveden Barbarou Liskovou v roce 1987
* Je to princip objektově orientovaného programování, který říká: Nechť je v počítačovém programu X potomkem předka Y, potom objekty typu Y mohou být nahrazeny objekty typu X beze změny jakékoliv potřebné vlastnosti předka Y.
* Pokud se rozhodneme implementovat tuto zásadu, tak se pro nás stane chování tříd více důležitější než její struktura
* Abysme zajistili, že náš kód dodržuje tuto zásadu, musíme zavést vlastní kontroly... V nejlepším případě to provedeme prostřednictvím code review a testů.

## Mock objekt
* Mock object je simulovaný objekt, který má napodobovat ten pravý
* Používá se především pro testování, standardně se vytvoří objekt proto, aby otestoval funkce jiného
* Mock object je jenom dočasný, po otestování a jeho využití se následně z aplikace odstraní
* Příklad ze života: vytvoření překážky na silnici může sloužit k testu, jak se chová auto při nárazu
