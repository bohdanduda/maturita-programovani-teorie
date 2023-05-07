# ASP.NET MVC formuláře
## definice a generování formuláře
* Formuláře můžeme vygenerovat přes kliknutí na metodu v controlleru, po vyplnění informací o formuláři se automaticky vygeneruje formulář
## formulářové prvky (label, textbox, checkbox,...)
## zpracování formuláře
* Formulář a jeho parametry zpracováváme v __controlleru__
* Musíme pro něj vytvořit samostatnou metodu s anotací `[HttpPost]`
## validace hodnot
* V modelu vždy vybírat druhou anotaci required - past
## session
* prostor na serveru, do kterého si klient může schovat data
* Sessioně můžeme přidat identifikátor
* V controlleru s ní pracujeme pomocí ``HttpContext.Session``
* Session můžeme naplnit pouze stringem.
* Když potřebujeme pracovat s jinými daty, tak použijeme Json k serializaci dat.
