# dědičnost v OOP
## dědičnost
* poskytuje možnost vytvořit třídu s daty z již existující třídy
* název tříd:
* `Odvozená třída` (dítě) - třída která dědí z jiné třídy
* `Základní třída` (rodič) - třída z které je děděno
* pro dědění z třídy použijeme znak `:`
* Když podědíme z jiné třídy, tak můžeme používat její vlastnosti a metody, jako kdyby byly třídy do které dědíme
## polymorfismus
* znamená "mnoho podob" a vyskytuje se, když máme mnoho tříd, které jsou navzájem propojeny dědičností
* využívá zděděné metody k provádění různých úloh, to umožňuje provádět jednu akci různými způsoby
* Příklad polymorfismu:
```
class Animal  // Base class (parent) 
{
  public void animalSound() 
  {
    Console.WriteLine("The animal makes a sound");
  }
}

class Pig : Animal  // Derived class (child) 
{
  public void animalSound() 
  {
    Console.WriteLine("The pig says: wee wee");
  }
}

class Dog : Animal  // Derived class (child) 
{
  public void animalSound() 
  {
    Console.WriteLine("The dog says: bow wow");
  }
}
```
## překrývání metod
* Existuj 2 typy překrývání metod: __Přetěžování__ a __Přepisování__

* Věci k zapamatování :
1. Metoda nesmí být soukromá
2. Přepsat lze pouze abstraktní nebo virtuální metody
3. O tom, která metoda má být volána, se rozhoduje za běhu
#### Přetěžování
* Přetěžování metod znamená vytvoření více metod v jedné třídě se stejnými názvy, ale různými signaturami (parametry)
* Umožňuje třídě, struktuře nebo rozhraní deklarovat více metod se stejným názvem s jedinečnými signaturami.
* _Compiler_ automaticky zavolá požadovanou metodu a zkontroluje počet parametrů a jejich typ předávaný do téže metody
#### Přepisování
* Přepisování metod znamená, že máme dvě metody se stejným názvem a stejnými signaturami. 
* První metoda by měla být v __základní třídě__ a druhá by měla být v __odvozené třídě__.
* Funkčnost metody základní třídy můžete přepsat tak, že vytvoříte metodu stejného jména se stejnou signaturou v odvozené třídě.
* Klíčová slova __Virtual__ a __Override__ slouží k dosažení přepsání metody.

## abstraktní třída
* __abstrakce__ dat je proces skrytí určitých detailů a zobrazení pouze podstatných informací uživateli
* __abstraktní třída__ je omezená třída, kterou nelze použít k vytváření objektů (pro přístup k ní je nutné ji zdědit z jiné třídy)
* __abstraktní metoda__ může být použita jen v abstraktní třídě.. metoda nemá tělo, to je poskytováno odvozenou třídou(z třídy zděděné)
## rozhraní
* další možnost dosažení __abstrakce__
* rozhraní je kompletní "abstraktní třída", která obsahuje pouze abstraktní metody (s prázdnými těly) a vlastnosti
* rozhraní si můžeme představit jako __šablonu__
* pro použití funkcí se musí rozhraní implementovat jinou třídou, používá se znak `:` (jako u dědění)
