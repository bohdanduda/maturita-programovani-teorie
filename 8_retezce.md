# �et�zce
* �et�zec je objekt typu `string`, jeho� hodnota je text
* text v �et�zci se ukl�d� jako sekven�n� kolekce `char` objekt�
## string
* `string` je prom�nn�, kter� se pou��vaj� k vyj�d�en� textu
## reprezentace stringu v RAM
* jak `string` tak `char` jsou v pam�ti ukl�d�ny na hald�
## vztah stringu a pole
## velikost stringu
* maxim�ln� velikost objektu v `string` pam�ti je 2 GB nebo p�ibli�n� 1 miliarda znak�.
## pr�ce s �et�zci
## spojov�n� �et�zc�
* Z�et�zen� je proces p�ipojen� jednoho �et�zce na konec jin�ho �et�zce
* �et�zce se z�et�zuj� pomoc� oper�toru `+`
* p��klad z�et�zen�:
``` 
Console.WriteLine("Hello" + "World");
``` 
* �et�zce m��eme tak� spojit pomoc� **interpolace**
* p�ed uvozovky se p�e `$` , prom�nn� se p�� do `{}` 
* p��klad interpolace:
```
string text = "Hello";
Console.WriteLine($"{text} World!");
``` 
* dal�� mo�nost� spojen� �et�zc� je funkce `String.Format()` - tuto mo�nost pou�ijeme, pokud pot�ebujete vlo�it hodnotu objektu, prom�nn� nebo v�razu do �et�zce
* p��klad funkce `String.Format()`
``` 
decimal temp = 20.4m;
string s = String.Format("The temperature is {0}�C.", temp);
``` 
## StringBuilder
* `string` je v nem�nn� objekt - �et�zec po vytvo�en� nem��eme zm�nit, ani upravit, nap��klad kdy� `string` s textem "Hello World!" zm�n�me na "Greetins World!", tak zabereme nov� m�sto v pam�ti a star� hodnota stringu z�stane v pam�ti n�zm�n�na.
* v tu chv�li se n�m hod� `StringBuilder`, nevytvo�� nov� m�sto v pam�ti, ale dynamicky roz���� pam�, aby se p�izp�sobila zm�n�n�mu �et�zci
* `StringBuilder` se deklaruje stejn� jako t��da
``` 
StringBuilder s = new StringBuilder();

 nebo m��eme hodnotu StringBuilderu rovnou naplnit...

StringBuilder s = new StringBuilder(Hello World!);
```
## b�l� znaky
* b�l� znaky jsou nepsan� text nap�.: mezery, tabel�tor, konce ��dk�
* b�l� znaky, kter� jsou nav�c jsou ignorov�ny v k�du v c#
## escape sekvence
* escape sekvence je kombinace charakter� za��naj�c� na `\` n�sleduje p�smeno nebo ��slo
* reprezentuje "non-printable" a specialn� charaktery v �et�zci

```
\' - Single quote
\" - Double quote
\\ - Backslash
\0 - Null
\a - Alert
\b - Backspace
\f - Form feed
\n - New line
\r - Carriage return
\t - Horizontal tab
\v - Vertical tab
\u - Unicode escape sequence (UTF-16)
\U - Unicode escape sequence (UTF-32)
\x - Unicode escape sequence similar to "\u" except with variable length
```