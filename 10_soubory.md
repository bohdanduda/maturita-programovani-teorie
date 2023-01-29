# soubory a souborový systém
## ètení a zápis do souboru
* pro ètení a zápis do textových souborù se používají tøídy ```StreamWriter``` a ```StreamReader```
* ```StreamWriter``` dìdí funkce ze tøídy ```TextWriter```, která poskytuje metody na zápis objektu do ```string```, zápis ```string``` do souboru, nebo serializaci do XML

* ```StreamReader``` dìdí funkce ze tøídy ```TextReader```, která poskytuje metody na ètení po charakterech, blocích, øádcích anebo celého obsahu souboru
## zpracování CSV souboru
* CSV (Comma Separated Values) je zpùsob ukládání dat do textového souboru, každý øádek CSV je datový záznam
* pro zápis a ètení z CSV souboru se v C# používá __CSVHelper__ NuGet
## XML

## JSON

## práce se souborovým systémem (FileInfo, DirectoryInfo, DriveInfo)
* tøída ```FileInfo``` se používá na práci a operace se soubory, obsahuje funkce a metody na vytváøení, ètení a mazání souborù
* používá tøídu ```StreamWriter``` na zápis dat do souboru 
* je souèástí ```System.IO```
* není dìdièná
___
* tøída ```DirectoryInfo``` se používá na práci a operace se složkami, obsahuje funkce na vytvoøení, smazání a pohyb se složkou
* je souèástí ```System.IO```
* není dìdièná
___
* tøída ```DriveInfo``` se používá na práci s disky, obsahuje funkce na zjištìní detailù souborù, složek nebo systémových informací
* mùžeme použít napøíklad její funkci ```GetDrives``` pro vypsání diskù.. vrací kolekci ```DriveInfo``` objektù
* je souèástí ```System.IO```
* není dìdièná