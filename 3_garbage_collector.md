# garbage collector

_hledá úseky paměti, které jsou obsazeny nepoužívanými „odpadky“, které už dále programem nejsou využívány_
Sběr odpadu je automatizovaný proces, který je schopný zjistit, jaké objekty už nevyužíváme a zbaví se jich. Tím čistí místo v paměti.

## reference counter
* počítá počet odkazů na objekt, když na něj nikdo neodkazuje, objekt se smaže
* nevýhoda je, že nedokáže detekovat cykly. Cyklus nastává v okamžiku, kdy dva a více objektů ukazují samy na sebe, například když rodičovská třída odkazuje na svého potomka a ten odkazuje zpátky na rodiče. Tyto dva objekty nebudou mít nikdy čítač roven nule, i když jsou z kořene programu nedosažitelné. Další nevýhoda spočívá v režii, která je nutná pro zvyšování a snižování čítačů u každého objektu. Kvůli těmto nedostatkům se počítání referencí v dnešní době jako univerzální garbage collector nepoužívá.

## mark-and-sweep
* Algoritmus mark and sweep nejdříve nastaví všem objektům, které jsou v paměti, speciální příznak „navštíven“ na hodnotu „ne“. Poté projde všechny objekty, ke kterým se lze dostat. Těm, které takto navštívil, nastaví příznak na hodnotu „ano“. V okamžiku, kdy se už nemůže dostat k žádnému dalšímu objektu, znamená to, že všechny objekty s příznakem „navštíven“ majícím hodnotu „ne“ jsou odpad – a mohou být tedy uvolněny z paměti.

* Tato metoda má několik nevýhod. Největší je, že během garbage collection je pozastaven běh programu. To znamená, že se programy pravidelně „zmrazí“; tato metoda se tedy nehodí pro aplikace běžící v reálném čase.
* 
## heap/stack

## referenční datové typy

## memory leak
