# øetìzce
* øetìzec je objekt typu `string`, jeho hodnota je text
* text v øetìzci se ukládá jako sekvenèní kolekce `char` objektù
## string
* `string` je promìnná, která se pouívají k vyjádøení textu
## reprezentace stringu v RAM
* jak `string` tak `char` jsou v pamìti ukládány na haldì
## vztah stringu a pole
## velikost stringu
* maximální velikost objektu v `string` pamìti je 2 GB nebo pøiblinì 1 miliarda znakù.
## práce s øetìzci
## spojování øetìzcù
* Zøetìzení je proces pøipojení jednoho øetìzce na konec jiného øetìzce
* øetìzce se zøetìzují pomocí operátoru `+`
* pøíklad zøetìzení:
``` 
Console.WriteLine("Hello" + "World");
``` 
* øetìzce mùeme také spojit pomocí **interpolace**
* pøed uvozovky se píše `$` , promìnné se píší do `{}` 
* pøíklad interpolace:
```
string text = "Hello";
Console.WriteLine($"{text} World!");
``` 
* další moností spojení øetìzcù je funkce `String.Format()` - tuto monost pouijeme, pokud potøebujete vloit hodnotu objektu, promìnné nebo vırazu do øetìzce
* pøíklad funkce `String.Format()`
``` 
decimal temp = 20.4m;
string s = String.Format("The temperature is {0}°C.", temp);
``` 
## StringBuilder
* `string` je v nemìnnı objekt - øetìzec po vytvoøení nemùeme zmìnit, ani upravit, napøíklad kdy `string` s textem "Hello World!" zmìníme na "Greetins World!", tak zabereme nové místo v pamìti a stará hodnota stringu zùstane v pamìti nìzmìnìna.
* v tu chvíli se nám hodí `StringBuilder`, nevytvoøí nové místo v pamìti, ale dynamicky rozšíøí pamì, aby se pøizpùsobila zmìnìnému øetìzci
* `StringBuilder` se deklaruje stejnì jako tøída
``` 
StringBuilder s = new StringBuilder();

 nebo mùeme hodnotu StringBuilderu rovnou naplnit...

StringBuilder s = new StringBuilder(Hello World!);
```
## bílé znaky
* bílé znaky jsou nepsanı text napø.: mezery, tabelátor, konce øádkù
* bílé znaky, které jsou navíc jsou ignorovány v kódu v c#
## escape sekvence
* escape sekvence je kombinace charakterù zaèínající na `\` následuje písmeno nebo èíslo
* reprezentuje "non-printable" a specialní charaktery v øetìzci

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