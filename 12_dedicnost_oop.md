# dìdiènost v OOP
## dìdiènost
* poskytuje monost vytvoøit tøídu s daty z ji existující tøídy
* název tøíd:
* `Odvozená tøída` (dítì) - tøída které dìdí z jiné tøídy
* `Základní tøída` (rodiè) - tøída z které je dìdìno
* pro dìdìní z tøídy pouijeme znak `:`
## polymorfismus
* znamená "mnoho podob" a vyskytuje se, kdy máme mnoho tøíd, které jsou navzájem propojeny dìdièností
* vyuívá zdìdìné metody k provádìní rùznıch úloh, to umoòuje provádìt jednu akci rùznımi zpùsoby
* 
## pøekrıvání metod
## abstraktní tøída
* __abstrakce__ dat je proces skrytí urèitıch detailù a zobrazení pouze podstatnıch informací uivateli
* __abstraktní tøída__ je omezená tøída, kterou nelze pouít k vytváøení objektù (pro pøístup k ní je nutné ji zdìdit z jiné tøídy)
* __abstraktní metoda__ mùe bıt pouita jen v abstraktní tøídì.. metoda nemá tìlo, to je poskytováno odvozenou tøídou(z tøídy zdìdìné)
## rozhraní
* další monost dosaení __abstrakce__
* rozhraní je kompletní "abstraktní tøída", která obsahuje pouze abstraktní metody (s prázdnımi tìly) a vlastnosti
* rozhraní si mùeme pøedstavit jako __šablonu__
* pro pouití funkcí se musí rozhraní implementovat jinou tøídou, pouívá se znak `:` (jako u dìdìní)