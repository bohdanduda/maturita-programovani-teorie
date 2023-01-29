# formul��e
* Windows Forms je open-source knihovna grafick�ch t��d, kter� je sou��st� Microsoft .NET Framework
## TextBox
* TextBox slou�� k p�ij�m�n� a zobrazov�n� vstupn�ch �daj� v podob� jednoho ��dku textu
* Ovl�dac� prvky WinForms TextBox slou�� k p�ij�m�n� vstup� od u�ivatele a k jejich zobrazen�
* TextBox se obecn� pou��v� k �prav� textu, ale lze jej tak� nastavit pouze pro �ten�
* TextBox umo��uje jedin� form�t pro text, kter� se v n�m zobrazuje nebo zad�v�
## Button
* Button je z�kladn� sou��st aplikace, softwaru nebo webov� str�nky. Umo��uje u�ivateli interakci s aplikac� nebo softwarem
* Button slou�� ke zpracov�n� ud�losti kliknut� a lze na n�j kliknout my��, nebo stisknut�m kl�ves ENTER nebo ESC
## ListBox
* ListBox (nebo tak� __v�b�rov� seznam__) poskytuje u�ivatelsk� rozhran� pro zobrazen� seznamu polo�ek
* U�ivatel� mohou ze seznamu vybrat jednu nebo v�ce polo�ek
* Ovl�dac� prvek ListBox m��e b�t pou�it k zobrazen� v�ce sloupc� a tyto sloupce mohou obsahovat obr�zky a dal�� ovl�dac� prvky
* U ListBoxu je na rozd�l od ComboBoxu (__rozbalovac�ho seznamu__) pole seznamu ji� rozbaleno, to znamen�, �e v seznamu je vid�t alespo� jedna mo�nost
* Do ListBoxu se p�id�vaj� polo�ky funkc� `Add`, odstra�uj� pomoc� `Remove`
## ComboBox
* ComboBox m� dv� podoby. V podob� "klidov�" zobrazuje pr�v� jednu vybranou polo�ku. Kdy� na n�j klikneme, rozbal� se a vyzobraz� v�echy sv� polo�ky
* Do ComboBoxu p�id�v�me polo�ky pomoc� funkce `Add`, odstra�ujeme jednotliv� pomoc� `Remove` nebo v�echny polo�ky pomoc� `Clear`

## Ud�losti
* Ka�d� prvek u�ivatelsk�ho rozhran� p�ij�m� ur�it� ud�losti. Nap��klad u tla��tek m��ete m�t ud�lost kliknut�, u za�krt�vac�ch pol��ek ud�lost zm�ny nebo u panel� ud�lost p�eta�en�
* Ud�losti pou��vaj� obsluhy ud�lost� nebo funkce, kter� se spust� pouze tehdy, kdy� nastane dan� ud�lost

## Otev�r�n� formul��� a zpracov�n� hodnot

## Show / ShowDialog
* `Show()` - __MَEME__ prov�d�t akce na rodi�ovsk�m formul��i
* `ShowDialog()` - __NEMَEME__ prov�d�t akce na rodi�ovsk�m formul��i
### Show
* Metoda `Show()` slou�� k otev�en� nov�ho formul��e, kdy� pou�ijeme metodu `Show()`, umo�n� n�m prov�st jakoukoli akci na rodi�ovsk� str�nce
* Kdy� pou�ijeme metodu `Show()` k otev�en� nov�ho okna, m��eme stejn� formul�� otev��t v�cekr�t, proto�e umo��uje kliknout na rodi�ovsk� formul�� po otev�en� pod��zen�ho formul��e
### ShowDialog
* Metoda `ShowDialog()` slou�� k otev�en� nov�ho formul��e, ale neumo��uje po otev�en� pod��zen�ho formul��e prov�d�t akce na rodi�ovsk�m formul��i
* Kdy� pou�ijeme metodu ShowDialog() pro otev�en� nov�ho okna, neumo��uje otev��t stejn� okno v�cekr�t