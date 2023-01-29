# d�di�nost v OOP
## d�di�nost
* poskytuje mo�nost vytvo�it t��du s daty z ji� existuj�c� t��dy
* n�zev t��d:
* `Odvozen� t��da` (d�t�) - t��da kter� d�d� z jin� t��dy
* `Z�kladn� t��da` (rodi�) - t��da z kter� je d�d�no
* pro d�d�n� z t��dy pou�ijeme znak `:`
## polymorfismus
* znamen� "mnoho podob" a vyskytuje se, kdy� m�me mnoho t��d, kter� jsou navz�jem propojeny d�di�nost�
* vyu��v� zd�d�n� metody k prov�d�n� r�zn�ch �loh, to umo��uje prov�d�t jednu akci r�zn�mi zp�soby
* 
## p�ekr�v�n� metod
## abstraktn� t��da
* __abstrakce__ dat je proces skryt� ur�it�ch detail� a zobrazen� pouze podstatn�ch informac� u�ivateli
* __abstraktn� t��da__ je omezen� t��da, kterou nelze pou��t k vytv��en� objekt� (pro p��stup k n� je nutn� ji zd�dit z jin� t��dy)
* __abstraktn� metoda__ m��e b�t pou�ita jen v abstraktn� t��d�.. metoda nem� t�lo, to je poskytov�no odvozenou t��dou(z t��dy zd�d�n�)
## rozhran�
* dal�� mo�nost dosa�en� __abstrakce__
* rozhran� je kompletn� "abstraktn� t��da", kter� obsahuje pouze abstraktn� metody (s pr�zdn�mi t�ly) a vlastnosti
* rozhran� si m��eme p�edstavit jako __�ablonu__
* pro pou�it� funkc� se mus� rozhran� implementovat jinou t��dou, pou��v� se znak `:` (jako u d�d�n�)