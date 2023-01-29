# z�klady OOP
## t��da
* datov� struktura, kter� spojuje datov� prom�nn� a funkce do jednoho celku
* instanc�m t��d se ��ka objekty
* t��da je pouze objektov� konstruktor, nebo "blueprint" pro vytvo�en� objektu...
## instance
* prom�nn� libovoln�ho typu obsa�en� ve t��d� nebo struktu�e
* slou�� k ukl�d�n� dat objektu
* pole instanc� p�edstavuj� data t��dy, kter� umo��uj� objektu udr�ovat jeho stav
## vlastnosti
* atributy, kter� charakterizuj� t��dy
* vlastnosti se chovaj� jako pole, na rozd�l od pol� jsou v�ak implementov�ny pomoc� __accessor�__ (definuj� p��kazy prov�d�n� p�i p��stupu, nebo p�i�ezen� vlastnosti)
## metody
* metody jsou bloky k�d� nebo p��kaz� v programu, kter� d�vaj� u�ivateli mo�nost opakovan� pou��vat stejn� k�d, co� �et�� spot�ebu pam�ti, p�sob� jako �spora �asu a hlavn� zaji��uje lep�� �itelnost k�du
* syntnaxe deklarace metody:
```
<Access_Modifier> <return_type> <method_name>([<param_list>])
     public	       void	   Vypocitej  (int x, int y)
```
## zapouzd�en�
* zapouzd�en� je definov�no jako zabalen� dat do jedn� jednotky, je to mechanismus, kter� spojuje k�d a data, s nimi� manipuluje
* p�i zapouzd�en� jsou prom�nn� nebo data t��dy skryty p�ed jakoukoli jinou t��dou a lze k nim p�istupovat pouze prost�ednictv�m n�kter� �lensk� funkce vlastn� t��dy, v n� jsou deklarov�ny

	https://www.geeksforgeeks.org/c-sharp-encapsulation/
## modifik�tory p��stupu
* modifik�tory p��stupu jsou kl��ov� slova pou��van� k ur�en� deklarovan� p��stupnosti �lena nebo typu
* `public` - k�d je p��stupn� pro v�echny t��dy
* `private` - k�d je p��stupn� jen pro t��du samotnou
* `protected` - k�d je p��stupn� jen pro t��du samotnou, nebo pro t��du kter� je d�di�n�
* `internal` - k�d je p��stupn� pouze v r�mci vlastn� sestavy
## konstruktor
* metoda pou�ita k inicializaci objekt�
* nem� ��dn� n�vratov� typ
* mouhou p�ij�mat parametry, kter� jsou pou�ity k inicializaci pol�
* m��e b�t p�et�en