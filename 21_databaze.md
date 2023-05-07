# databáze
## Připojení k MySQL/MSSQL
* pro práci s databází potřebujeme NuGet MySql.EntityFrameworkCore
* Poté ještě vytvořit připojovací řetězec
```
"ConnectionStrings": 
{
    "Default": "Server=YOURSERVER;User ID=YOURUSERID;Password=YOURPASSWORD;Database=YOURDATABASE"
}
```
* Databázi ovládáme z třídy __Controller__
## ORM - entity framework
* Entity Framework v jazyce C# je sada technologií ADO.NET, které pomáhají při vývoji softwaru založeného na datech
* C# Entity framework je rámec ORM (__Object Relational Mapping__), který vývojářům poskytuje automatizovaný způsob ukládání a přístupu k databázím
* Výhody používání ORM: __Úspora času__ a  __sledovatelnost změn__ provedených v databázi - existují knihovny specializované na ORM, které zaznamenávají celou historii dat od jejich vytvoření
## Mapování tabulek
* Je proces zákódování vlastnosti, aby se jmenovala stejně jako tabulka, nebo sloupec v databázi
* Přiklad mapování sloupce: `[Column("my_column")]`
* Přiklad mapování tabulky: `[Table("my_column")]`
## vazby
* Vazba je anotace vlastnosti, která je v databázi jako cizí klíč
* Příklad anotace vazby: `[ForeignKey("my_foreign_key")]`
* Cizí klíč __se v anotaci musí jmenovat stejně__ jako ten v databázi
## DbContext
__Most mezi Entity Framework a databází__
* DbContext je třída, která představuje relaci s databází a lze ji použít k dotazování a ukládání instancí entit
* Cokoli děláme v Entity Frameworku (získáváme data, ukládáme data, načítáme data nebo provádíme jakoukoli jinou opraci), provádíme prostřednictvím DbContextu
## Repository
* Repository pattern slouží k abstrakci způsobu, jakým jsou data uchovávána nebo načítána z databáze
* Myšlenkou je oddělit vrstvu pro přístup k datům od vrstvy pro obchodní přístup k aplikaci, takže operace (jako je přidávání, aktualizace, mazání a výběr položek z kolekce) se provádějí pomocí jednoduchých metod, aniž by se řešily problémy s databází (jako jsou připojení, příkazy atd.)
## LinQ
* LINQ (__Language Integrated Query__) je jednotná syntaxe dotazů v jazycích C# a VB.NET pro získávání dat z různých zdrojů a formátů
* poskytuje jednotné dotazovací rozhraní pro různé typy zdrojů dat např: __MySql__, __MS SQL Server__, XML dokumenty...
