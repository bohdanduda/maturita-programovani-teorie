# ��d�c� struktury
* 3 druhy struktur programu:
1. posloupnost p��kaz� � v�echny p��kazy se postupn� provedou jeden po druh�m
2. v�tven� (�i podm�n�n� p��kaz) � v z�vislosti na spln�n� podm�nky se ur�it� p��kaz bu� provede nebo neprovede
3. cyklus � v z�vislosti na spln�n� podm�nky se ��st programu vykon� v�cekr�t
## podm�nky
### IF
*  podm�n�n� p��kaz a podm�n�n� konstrukce jsou prost�edky, kter� umo��uj� rozd�ln� chov�n� programu, v z�vislosti na specifikovan� logick� podm�nce. V�sledek podm�nky je bu� `true` nebo `false`
* `IF..GOTO` - Napodobuje typickou strojovou instrukci GOTO, kter� umo��uje skok na ur�it� ��dek k�du
* `IF..THEN` - Pokud je podm�nka v ��sti IF vyhodnocena jako pravda, je vykon�n k�d specifikovan� v ��sti THEN. Kdy� nen�, je k�d v ��sti THEN vynech�n a program pokra�uje d�l.
* `IF..THEN..ELSE` - Pokud podm�nka v ��sti IF nen� vyhodnocena jako pravda, provede se k�d v ��sti `ELSE`

### SWITCH a CASE
* switch porovn�v� p�edanou hodnotu s p�edem specifikovan�mi konstantami. V p��pad� shody hodnoty s konstantou, vykon� p��kaz, kter� je definov�n za n�

## cykly
* cyklus je ��d�c� struktura, kde se opakovan� prov�d� posloupnost p��kaz�. Opakov�n� i ukon�en� cyklu je ��zeno n�jakou podm�nku
* existuje mnoho druh� cykl�:
* `WHILE` - pokud plat� podm�nka, cyklus b�� furt dokola
* `DO-WHILE` - cyklus s podm�nkou na konci posloupnosti p��kaz�
* `FOR` - speci�ln� p��pad cyklu s podm�nkou na za��tku, obvykle u��van� pro v��et prvk� z mno�iny prvk�
## v�jimky (try-and-catch)
* funkce zpracov�n� v�jimek jazyka C# pom��ou �e�it neo�ek�van� nebo v�jime�n� situace, ke kter�m doch�z� p�i spu�t�n� programu
* v�jimky se vytv��ej� pomoc� `THROW (exeption)`
* pomoc� p��kaz� `TRY` a `CATCH` nejd��ve zkus�me zda je k�d funk�n�, pokud ne tak `CATCH` "chyt�" chybu a vykon� definovan� p��kaz