# formulare
## datagrid
* Ovl�dac� prvek DataGrid ve Windows Forms zobrazuje data v �ad� ��dk� a sloupc�
* Nejjednodu���m p��padem je, kdy� je m��ka v�z�na na zdroj dat s jedinou tabulkou, kter� neobsahuje ��dn� vztahy, v takov�m p��pad� se data zobrazuj� v jednoduch�ch ��dc�ch a sloupc�ch
* Pokud je m��ka DataGrid sv�z�na s daty s v�ce souvisej�c�mi tabulkami a pokud je v m��ce povolena navigace, zobraz� se v ka�d�m ��dku rozbalovac� prvky
### pr�ce s datagridem
 * Pomoc� expand�ru m��e u�ivatel p�ech�zet z nad�azen� tabulky do pod�azen� tabulky
 * Kliknut�m na uzel se zobraz� pod��zen� tabulka a kliknut�m na tla��tko zp�t se zobraz� p�vodn� rodi�ovsk� tabulka - t�mto zp�sobem m��ka zobrazuje hierarchick� vztahy mezi tabulkami
## p�ipojen� DataSource
* Aby ovl�dac� prvek DataGrid fungoval, m�l by b�t sv�z�n se zdrojem dat pomoc� vlastnost� __DataSource__ a __DataMember__ v dob� n�vrhu nebo metody __SetDataBinding__ v dob� b�hu
* Tato vazba odkazuje DataGrid na instancovan� objekt zdroje dat, nap��klad __DataSet__ nebo __DataTable__, ovl�dac� prvek DataGrid zobrazuje v�sledky akc�, kter� jsou prov�d�ny s daty
## napojen� DataModelu na souborov�/datab�sov� repository
