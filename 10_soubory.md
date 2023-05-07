# soubory a souborový systém
## čtení a zápis do souboru
* pro čtení a zápis do textových souborů se používají třídy ```StreamWriter``` a ```StreamReader```
* ```StreamWriter``` dědí funkce ze třídy ```TextWriter```, která poskytuje metody na zápis objektu do ```string```, zápis ```string``` do souboru, nebo serializaci do XML

* ```StreamReader``` dědí funkce ze třídy ```TextReader```, která poskytuje metody na čtení po charakterech, blocích, řádcích anebo celého obsahu souboru
## zpracování CSV souboru
* CSV (Comma Separated Values) je způsob ukládání dat do textového souboru, každý řádek CSV je datový záznam
* pro zápis a čtení z CSV souboru se v C# používá __CSVHelper__ NuGet
## XML
* XML neboli Extensible Markup Language je obecný značkovací jazyk, který se používá pro uchovávání a transport dat
* Umožňuje snadné vytváření konkrétních značkovacích jazyků pro různé účely a různé typy dat.
* Používá se pro serializaci dat, v čemž soupeří např. s JSON
## JSON
* JSON neboli JavaScript Object Notation je způsob zápisu dat nezávislý na pc platformě
* Je určený pro přenos dat, která mohou být organizována v polích nebo agregována v objektech
* Vstupem je libovolná datová struktura, výstupem je vždy řetězec
* V C# ho můžeme využít například v session pro serializaci dat... Využívá se třídy JsonSerializer
* Příklad serializace do textového řetězce: `string jsonString = JsonSerializer.Serialize("Hello World!");`
## práce se souborovým systémem (FileInfo, DirectoryInfo, DriveInfo)
* třída ```FileInfo``` se používá na práci a operace se soubory, obsahuje funkce a metody na vytváření, čtení a mazání souborů
* používá třídu ```StreamWriter``` na zápis dat do souboru 
* je součástí ```System.IO```
* není dědičná
___
* třída ```DirectoryInfo``` se používá na práci a operace se složkami, obsahuje funkce na vytvoření, smazání a pohyb se složkou
* je součástí ```System.IO```
* není dědičná
___
* třída ```DriveInfo``` se používá na práci s disky, obsahuje funkce na zjištění detailů souborů, složek nebo systémových informací
* můžeme použít například její funkci ```GetDrives``` pro vypsání disků.. vrací kolekci ```DriveInfo``` objektů
* je součástí ```System.IO```
* není dědičná
