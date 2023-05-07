# ASP.NET MVC View 
## princip tvorby dynamického view
## Razor engine
* Razor je syntaxe značek, která umožňuje vkládat serverový kód do webových stránek pomocí jazyků C# a VB.Net. Nejedná se o programovací jazyk, ale o jazyk značkovací na straně serveru.
* Razor nemá žádnou vazbu na ASP.NET MVC, protože je to univerzální šablonovací engine
* Můžeme ho použít kdekoli k vygenerování výstupu jako HTML
## layout
* Layout je celková kostra html
* Funkce RenderBody - vygeneruje stránku, dá se použít jen v Layoutu
## základní konstrukce ve View - (výpis proměnné, cyklus, podmínka)
## tvorba odkazů
* Odkazy tvoříme tak, že do objektu `<a>` přidáme parametr `Url.RouteUrl()>` a do něj zadáme jméno cesty kam budeme odkázáni  
* Příklad odkazu: `<a href="@Url.RouteUrl("Login")">`
## template
* Template je html šablona, kterou můžeme využít při tvoření více stránek, které mají nějakou stejnou část např. header, footer, menu nav. bar
* Implementujeme ho tak, že do html kódu napíšeme jméno templatu
## partial view
* Částečné zobrazení, pomocí funkce RenderPartial můžeme zobrazit jiné view, které funkci předáme
* Popužití: Když máme část stránky, která se opakuje
## ViewComponents
* Aby třída byla komponentou, musí dědit ze třidy __ViewComponent__
* poté se chová v podstatě jako controller
## předávání dat do view - (Model, ViewData, ViewBag)
* ViewBag - můžeme si v něm definovat jakoukoli vlastost, kterou si poté vyzvedneme ve View
* ViewData - stejné jako ViewBag, funguje jako dictionary
