# databáze
## Pøipojení k MySQL/MSSQL
* Pro pøipojení musíme stáhnout balíèek NuGet
* Poté ještì vytvoøit pøipojovací øetìzec
```
"ConnectionStrings": 
{
    "Default": "Server=YOURSERVER;User ID=YOURUSERID;Password=YOURPASSWORD;Database=YOURDATABASE"
}
```
* Databázi ovládáme z tøídy __Controller__
## ORM - entity famework
* Entity Framework v jazyce C# je sada technologií ADO.NET, které pomáhají pøi vývoji softwaru založeného na datech
* C# Entity framework je rámec ORM (__Object Relational Mapping__), který vývojáøùm poskytuje automatizovaný zpùsob ukládání a pøístupu k databázím
* Výhody používání ORM: __Úspora èasu__ a  __sledovatelnost zmìn__ provedených v databázi - existují knihovny specializované na ORM, které zaznamenávají celou historii dat od jejich vytvoøení
## Mapování tabulek
## vazby
## DbContext
__Most mezi Entity Framework a databází__
* DbContext je tøída, která pøedstavuje relaci s databází a lze ji použít k dotazování a ukládání instancí entit
* Cokoli dìláme v Entity Frameworku (získáváme data, ukládáme data, naèítáme data nebo provádíme jakoukoli jinou opraci), provádíme prostøednictvím DbContextu
## Repository
* Repository pattern slouží k abstrakci zpùsobu, jakým jsou data uchovávána nebo naèítána z databáze
* Myšlenkou je oddìlit vrstvu pro pøístup k datùm od vrstvy pro obchodní pøístup k aplikaci, takže operace (jako je pøidávání, aktualizace, mazání a výbìr položek z kolekce) se provádìjí pomocí jednoduchých metod, aniž by se øešily problémy s databází (jako jsou pøipojení, pøíkazy atd.)
## LinQ
* LINQ (__Language Integrated Query__) je jednotná syntaxe dotazù v jazycích C# a VB.NET pro získávání dat z rùzných zdrojù a formátù
* poskytuje jednotné dotazovací rozhraní pro rùzné typy zdrojù dat napø: __MySql__, __MS SQL Server__, XML dokumenty..