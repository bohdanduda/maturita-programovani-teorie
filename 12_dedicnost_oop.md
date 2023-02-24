# dědičnost v OOP
## dědičnost
* poskytuje možnost vytvořit třídu s daty z již existující třídy
* název tříd:
* `Odvozená třída` (dítě) - třída která dědí z jiné třídy
* `Základní třída` (rodič) - třída z které je děděno
* pro dědění z třídy použijeme znak `:`
## polymorfismus
* znamená "mnoho podob" a vyskytuje se, když máme mnoho tříd, které jsou navzájem propojeny dědičností
* využívá zděděné metody k provádění různých úloh, to umožňuje provádět jednu akci různými způsoby
## překrývání metod
## abstraktní třída
* __abstrakce__ dat je proces skrytí určitých detailů a zobrazení pouze podstatných informací uživateli
* __abstraktní třída__ je omezená třída, kterou nelze použít k vytváření objektů (pro přístup k ní je nutné ji zdědit z jiné třídy)
* __abstraktní metoda__ může být použita jen v abstraktní třídě.. metoda nemá tělo, to je poskytováno odvozenou třídou(z třídy zděděné)
## rozhraní
* další možnost dosažení __abstrakce__
* rozhraní je kompletní "abstraktní třída", která obsahuje pouze abstraktní metody (s prázdnými těly) a vlastnosti
* rozhraní si můžeme představit jako __šablonu__
* pro použití funkcí se musí rozhraní implementovat jinou třídou, používá se znak `:` (jako u dědění)
