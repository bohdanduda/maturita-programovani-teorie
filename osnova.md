# Okruhy otázek


1. [proměnné](01_promenne.md) - datové typy, velikosti, uložení záporných čísel (přímý, doplňkový kód), desetinná čísla, hodnotové a referenční, platnost proměnných, operátory (aritmetické, logické + pravdivostní tabulky, bitové), enum, přetěžování operátorů

2. [procedury, funkce](02_procedury.md) - parametry, rozdíly, návratový typ, předávání parametrů do funkce (hodnotou, ref, out)

3. [garbage collector](03_garbage_collector.md) (reference counter, mark-and-sweep), heap/stack, referenční datové typy, memory leak

4. [řídící struktury](04_ridici_struktury.md) - podmínky, cykly, výjimky (vyhození a odchyt)

5. [algoritmy](5_algoritmy.md) - vlastnosti, vztah algoritmů a programovacích jazyků, výpočet asymptotické složitosti (funkce omikron, omega, theta), algoritmy v poli (min/max, otočení, vkládání, linární vyhl. binární vyhl. řadící alg. - bubble sort, selection sort, insertion sort, quick sort, merge sort, heap sort), stabilita řazení, implementace jednoduchých alg.

6. [rekurze](06_rekurze.md) - definice, vztah rekurzivního a iterativního algoritmu, příklady

7. [pole a kolekce](07_pole_a_kolekce.md) - definice pole, princip, uložení v RAM, rozdíl polí a kolekcí, výhody/nevýhody, indexy, 2D/3D pole, List, Dictionary

8. [řetězce](08_retezce.md) - string, jeho reprezentace v RAM, vztah stringu a pole, velikost, práce s řetězci (základní funkce - split, substring, tolower, toupper, replace, trim, pad...), spojování řetězců, StringBuilder, bile znaky, escape sekvence \n \r \t \\, @"\string", $"hello {variable}"

9. [datové struktury](09_datove_struktury.md) - zásobník, fronta, single-linked list, double-linked list, principy a použití, implementace fronty a zásobníku v poli a ve spojovém seznamu

10. [soubory a souborový systém](10_soubory.md) - čtení a zápis do souboru, zpracování CSV souboru, XML, JSON, práce se souborovým systémem (FileInfo, DirectoryInfo, DriveInfo) 

11. [základy OOP](11_zaklady_oop.md) - třída, instance, vlastnosti, metody, zapouzdření, modifikátory přístupu, konstruktor

12. [dědičnost v OOP](12_dedicnost_oop.md) - dědičnost, konstruktory, polymorfismus, překrývání metod, rozhraní, abstraktní třída

13. [pokročilé prvky OOP](13_pokrocile_oop.md) - statické vlastnosti a metody, statický konstruktor, vnitřní třídy, generické třídy, generické metody

14. [UML](14_uml.md) - popis UML, základní diagramy, Class diagram (diagram tříd) a význam jednotlivých symbolů v kódu, UseCase diagram (diagram případů užití) , State diagram, Sequence diagram (sekvenční diagram)

15. [regulární výrazy](15_regularni_vyrazy.md) - význam jednotlivých speciálních znaků (výčet, opakování, povinnost, začátek/konec, ...), jejich praktické využití

16. [formuláře](16_formulare_zakladni.md) - základní práce s formulářovými prvky (textbox, button, listbox, combobox), události, otevírání formulářů a zpracování hodnot, Show/ShowDialog

17. [formuláře](17_formulare_stredni.md) - datagrid - práce s komponentou datagrid, připojení DataSource, napojení DataModelu na souborové/databázové repository

18. formuláře - validace vstupních hodnot, validace na úrovni formuláře a položky, ErrorProvider, aplikace DAregulárních výrazů

19. GDI grafika - kreslení jednoduchých objektů - čára, kružnice, obdélník, práce s barvami, definice štětce a pera, objekt Graphics, událost Paint, kreslení obrázků, textů, export do JPG, transformace SS

20. [návrhové vzory GoF](20_vzory_gof.md) - Tovární metoda (Factory Method), Jedináček (Singleton), Příkaz (Command), Pozorovatel (Observer), Iterator, State, Decorator, Memento, Adapter

21.  [Databáze](21_databaze.md) - připojení k MySQL/MSSQL, ORM - entity framework, mapování tabulek, vazby, DbContext, DbSet, repository, LINQ

22. [Teorie testování](22_testovani-teorie.md) - typy testů, blackbox/whitebox, test UI, usability testy, testy výkonu, profiler, Test Driven Development

23. [Unit testy](23_unit_testy.md) - princip a využití unit testů, testovací třídy, testovací metody, pre-testové a post-testové rutiny, testování formulářů

24. [Integrační testy](24_integracni_testy.md) - význam integračních testů, zásady nahraditelnosti, mock objekt

25. [ASP.NET MVC základy](25_asp_zaklady.md) - princip architektury Model-View-Controller, zpracování požadavku, směrování, výchozí směrování, HTTP protokol, controller, akce, parametry akce, návratový typ (ActionResult - View, Redirect)

26. [ASP.NET MVC View](26_asp_view.md) - princip tvorby dynamického view, Razor engine, layout, základní konstrukce ve View (výpis proměnné, cyklus, podmínka), tvorba odkazů, template, partial view, ViewComponents, předávání dat do view - (Model, ViewData, ViewBag)

27. ASP.NET MVC formuláře - definice a generování formuláře, formulářové prvky (label, textbox, checkbox,...), zpracování formuláře, validace hodnot, session

28. REST API - HTTP metody (GET, POST, PUT, DELETE), mapovani na akce, response, JSON, XML, stavove kody (200, 201, 301, 302, 400, 401, 403, 404, 500), autentizace (JWT), REST - restful - formát adres (/users/:id), ASP.NET MVC API

29. Události a delegáty, delegáty Action/Func/Predicate,  Observer, Lambda funkce, anonymní funkce/objekty, dynamické typy (var, dynamic)

30. Reflexe - Type, PropertyInfo, MethodInfo, přístup k private, tvorba instancí (volání konstruktoru), volání metod podle názvu (Invoke), Atributy (anotace)
