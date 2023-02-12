# garbage collector

* _hledá úseky paměti, které jsou obsazeny nepoužívanými „odpadky“, které už dále programem nejsou využívány_
* Sběr odpadu je automatizovaný proces, který je schopný zjistit, jaké objekty už nevyužíváme a zbaví se jich. Tím čistí místo v paměti.
* Garbage Collector se spustí, pokud program zrovna nic nedělá, pokud je paměť přeplněna, nebo pokud ho explicitně zavoláme pomocí: `GC.Collect()`
* Garbage Collector se používá ve většině jazycích. Jeho využíváním se ale program zpomalí
* V jazycích C __GC__ není, jsou naopak rychlejší

## reference counter
* počítá počet odkazů na objekt, když na něj nikdo neodkazuje, objekt se smaže
* nevýhoda je, že nedokáže detekovat cykly (Pokud nespecifikujeme __referenci WEAK__), funguje to tak, že se __WEAK__ do __GC__ nezapočítává.
* Cyklus nastává v okamžiku, kdy dva a více objektů ukazují samy na sebe, například když rodičovská třída odkazuje na svého potomka a ten odkazuje zpátky na rodiče. Tyto dva objekty nebudou mít nikdy čítač roven nule, i když jsou z kořene programu nedosažitelné.
* __RC__ používá třeba jazyk Swift (iOS)
* Jinak se __RC__ moc nepoužívá

## mark-and-sweep
* Funguje dvoufázově: __Mark__ prochází objekty jdoucí ze __stacku__ a dává jim značky, jestli se k nim dá dostat. __Sweep__ projde všechny objekty a pokud u nich značka není, odstraní je.

* Spouští se ve 3 situacích; 1: Když program nemá co dělat. 2: Když je paměť přeplněná. 3: Když ho explicitně explicitně zavoláme pomocí: `GC.Collect()`

* Algoritmus mark and sweep nejdříve nastaví všem objektům, které jsou v paměti, speciální příznak „navštíven“ na hodnotu „ne“. Poté projde všechny objekty, ke kterým se lze dostat. Těm, které takto navštívil, nastaví příznak na hodnotu „ano“. V okamžiku, kdy se už nemůže dostat k žádnému dalšímu objektu, znamená to, že všechny objekty s příznakem „navštíven“ majícím hodnotu „ne“ jsou odpad – a mohou být tedy uvolněny z paměti.

* Tato metoda má několik nevýhod. Největší je, že během garbage collection je pozastaven běh programu. To znamená, že se programy pravidelně „zmrazí“; tato metoda se tedy nehodí pro aplikace běžící v reálném čase. Další nevýhodou je, že se paměť při čištění nevyčistí celá, protože nějaké části paměti využíváme více než jiné
* Generační varianta – čistí se části paměti, když se odloží čištění,  nastaví se značka flag na tolik, kolikrát už objekt byl od čistění odložen

## heap/stack
* 2 části paměti. málá - Stack, velká - Heap.
* Na Stacku se automaticky tvoří všechny proměnné
* Referenční proměnné, nebo objekty se tvoří na Heapu (Příklad: změna velikosti pole - staré pole na Heapu zůsává)

## referenční datové typy

## memory leak
* Situace, kdy jsou v paměti data, ale nemůžeme je použít (příklad s oběžnou drahou: Vypustíme na orbitu tolik družic, které se postupně ničí a nakonec nemáme místo na nové družice)
