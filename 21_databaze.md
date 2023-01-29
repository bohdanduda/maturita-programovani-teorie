# datab�ze
## P�ipojen� k MySQL/MSSQL
* Pro p�ipojen� mus�me st�hnout bal��ek NuGet
* Pot� je�t� vytvo�it p�ipojovac� �et�zec
```
"ConnectionStrings": 
{
    "Default": "Server=YOURSERVER;User ID=YOURUSERID;Password=YOURPASSWORD;Database=YOURDATABASE"
}
```
* Datab�zi ovl�d�me z t��dy __Controller__
## ORM - entity famework
* Entity Framework v jazyce C# je sada technologi� ADO.NET, kter� pom�haj� p�i v�voji softwaru zalo�en�ho na datech
* C# Entity framework je r�mec ORM (__Object Relational Mapping__), kter� v�voj���m poskytuje automatizovan� zp�sob ukl�d�n� a p��stupu k datab�z�m
* V�hody pou��v�n� ORM: __�spora �asu__ a  __sledovatelnost zm�n__ proveden�ch v datab�zi - existuj� knihovny specializovan� na ORM, kter� zaznamen�vaj� celou historii dat od jejich vytvo�en�
## Mapov�n� tabulek
## vazby
## DbContext
__Most mezi Entity Framework a datab�z�__
* DbContext je t��da, kter� p�edstavuje relaci s datab�z� a lze ji pou��t k dotazov�n� a ukl�d�n� instanc� entit
* Cokoli d�l�me v Entity Frameworku (z�sk�v�me data, ukl�d�me data, na��t�me data nebo prov�d�me jakoukoli jinou opraci), prov�d�me prost�ednictv�m DbContextu
## Repository
* Repository pattern slou�� k abstrakci zp�sobu, jak�m jsou data uchov�v�na nebo na��t�na z datab�ze
* My�lenkou je odd�lit vrstvu pro p��stup k dat�m od vrstvy pro obchodn� p��stup k aplikaci, tak�e operace (jako je p�id�v�n�, aktualizace, maz�n� a v�b�r polo�ek z kolekce) se prov�d�j� pomoc� jednoduch�ch metod, ani� by se �e�ily probl�my s datab�z� (jako jsou p�ipojen�, p��kazy atd.)
## LinQ
* LINQ (__Language Integrated Query__) je jednotn� syntaxe dotaz� v jazyc�ch C# a VB.NET pro z�sk�v�n� dat z r�zn�ch zdroj� a form�t�
* poskytuje jednotn� dotazovac� rozhran� pro r�zn� typy zdroj� dat nap�: __MySql__, __MS SQL Server__, XML dokumenty..