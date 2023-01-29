# soubory a souborov� syst�m
## �ten� a z�pis do souboru
* pro �ten� a z�pis do textov�ch soubor� se pou��vaj� t��dy ```StreamWriter``` a ```StreamReader```
* ```StreamWriter``` d�d� funkce ze t��dy ```TextWriter```, kter� poskytuje metody na z�pis objektu do ```string```, z�pis ```string``` do souboru, nebo serializaci do XML

* ```StreamReader``` d�d� funkce ze t��dy ```TextReader```, kter� poskytuje metody na �ten� po charakterech, bloc�ch, ��dc�ch anebo cel�ho obsahu souboru
## zpracov�n� CSV souboru
* CSV (Comma Separated Values) je zp�sob ukl�d�n� dat do textov�ho souboru, ka�d� ��dek CSV je datov� z�znam
* pro z�pis a �ten� z CSV souboru se v C# pou��v� __CSVHelper__ NuGet
## XML

## JSON

## pr�ce se souborov�m syst�mem (FileInfo, DirectoryInfo, DriveInfo)
* t��da ```FileInfo``` se pou��v� na pr�ci a operace se soubory, obsahuje funkce a metody na vytv��en�, �ten� a maz�n� soubor�
* pou��v� t��du ```StreamWriter``` na z�pis dat do souboru 
* je sou��st� ```System.IO```
* nen� d�di�n�
___
* t��da ```DirectoryInfo``` se pou��v� na pr�ci a operace se slo�kami, obsahuje funkce na vytvo�en�, smaz�n� a pohyb se slo�kou
* je sou��st� ```System.IO```
* nen� d�di�n�
___
* t��da ```DriveInfo``` se pou��v� na pr�ci s disky, obsahuje funkce na zji�t�n� detail� soubor�, slo�ek nebo syst�mov�ch informac�
* m��eme pou��t nap��klad jej� funkci ```GetDrives``` pro vyps�n� disk�.. vrac� kolekci ```DriveInfo``` objekt�
* je sou��st� ```System.IO```
* nen� d�di�n�