# ASP.NET MVC základy
* MVC - Model View Controller
* Model - jádro aplikace
* Controller - zpracovává požadavky a řeší je, žádá data k modelu
* View - 
## princip architektury Model-View-Controller
## Zpracování požadavku
## Směrování
* Směrování je definováno v program.cs, určuje mapování a formát adresy
* paremetry jsou nepovinné, když nevyplníme, vyplní se sami
## Výchozí směrování
## HTTP protokol
* Textový, bezestavový protokol, používán ke komunikaci se serverem
* Jaký požadavek přijde, tomu odpoví, neřeší od koho je
## Controller
* Třída, která dědí z rodičovské třídy __Controller__
* Má v sobě akce - vrací IActionResult. Je to činnost, která se poté na stránce provádí
## Akce
* Akcí na kontroleru může být několik, vždycky vrací nějakou hodnotu. View, Json, atd.
## Parametry akce
* Předáváme do parametrů metod v Controlleru
## Návratový typ (ActionResult - View, Redirect)
* Redirect - zadáme url stránku na kterou budeme přesměrováni
* RedirectToAction - zadáme jméno modelu a jeho akci, na kterou nás budeme přesměrováni
