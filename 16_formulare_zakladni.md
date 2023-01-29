# formuláøe
* Windows Forms je open-source knihovna grafických tøíd, která je souèástí Microsoft .NET Framework
## TextBox
* TextBox slouží k pøijímání a zobrazování vstupních údajù v podobì jednoho øádku textu
* Ovládací prvky WinForms TextBox slouží k pøijímání vstupù od uživatele a k jejich zobrazení
* TextBox se obecnì používá k úpravì textu, ale lze jej také nastavit pouze pro ètení
* TextBox umožòuje jediný formát pro text, který se v nìm zobrazuje nebo zadává
## Button
* Button je základní souèást aplikace, softwaru nebo webové stránky. Umožòuje uživateli interakci s aplikací nebo softwarem
* Button slouží ke zpracování události kliknutí a lze na nìj kliknout myší, nebo stisknutím kláves ENTER nebo ESC
## ListBox
* ListBox (nebo také __výbìrový seznam__) poskytuje uživatelské rozhraní pro zobrazení seznamu položek
* Uživatelé mohou ze seznamu vybrat jednu nebo více položek
* Ovládací prvek ListBox mùže být použit k zobrazení více sloupcù a tyto sloupce mohou obsahovat obrázky a další ovládací prvky
* U ListBoxu je na rozdíl od ComboBoxu (__rozbalovacího seznamu__) pole seznamu již rozbaleno, to znamená, že v seznamu je vidìt alespoò jedna možnost
* Do ListBoxu se pøidávají položky funkcí `Add`, odstraòují pomocí `Remove`
## ComboBox
* ComboBox má dvì podoby. V podobì "klidové" zobrazuje právì jednu vybranou položku. Když na nìj klikneme, rozbalí se a vyzobrazí všechy své položky
* Do ComboBoxu pøidáváme položky pomocí funkce `Add`, odstraòujeme jednotlivì pomocí `Remove` nebo všechny položky pomocí `Clear`

## Události
* Každý prvek uživatelského rozhraní pøijímá urèité události. Napøíklad u tlaèítek mùžete mít událost kliknutí, u zaškrtávacích políèek událost zmìny nebo u panelù událost pøetažení
* Události používají obsluhy událostí nebo funkce, které se spustí pouze tehdy, když nastane daná událost

## Otevírání formuláøù a zpracování hodnot

## Show / ShowDialog
* `Show()` - __MÙŽEME__ provádìt akce na rodièovském formuláøi
* `ShowDialog()` - __NEMÙŽEME__ provádìt akce na rodièovském formuláøi
### Show
* Metoda `Show()` slouží k otevøení nového formuláøe, když použijeme metodu `Show()`, umožní nám provést jakoukoli akci na rodièovské stránce
* Když použijeme metodu `Show()` k otevøení nového okna, mùžeme stejný formuláø otevøít vícekrát, protože umožòuje kliknout na rodièovský formuláø po otevøení podøízeného formuláøe
### ShowDialog
* Metoda `ShowDialog()` slouží k otevøení nového formuláøe, ale neumožòuje po otevøení podøízeného formuláøe provádìt akce na rodièovském formuláøi
* Když použijeme metodu ShowDialog() pro otevøení nového okna, neumožòuje otevøít stejné okno vícekrát