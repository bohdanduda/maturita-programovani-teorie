# Proměnné
* Místo paměti počítače, kam si můžeme uložit data.
* Proměnná má vždy nějaký datový typ - číslo, znak, text atd.
## Datové typy
Hodnotové, odkazové, výčtové - https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types

### Hodnotové
* `bool`, `byte`, `char` a všechny __číselné__ datové typy: `decimal`, `double`, `float`, `int`, `long`, `short`
* Mají svou hodnotu přímo v paměti, která se označuje jako __zásobník__ (stack).
* Obecně jsou to jednoduché struktury, např. jedno číslo, jeden znak. Většinou se chce, abychom s nimi pracovali co nejrychleji, v programu se jich vyskytuje velmi mnoho a zabírají málo místa.

### Odkazové (referenční)
* `string`, `object`, `dynamic`
* V __zásobníku__ (stack) mají uložený pouze __odkaz__ (referenci) na skutečnou hodnotu.
* Jejich __skutečné hodnoty__ se ukládají na __haldu__ (heap).
* Proměnné odkazového (referenčního) typu jsou v paměti uloženy vlastně nadvakrát, jednou v zásobníku a jednou v haldě. V zásobníku je uložena pouze tzv. reference, tedy odkaz do haldy, kde se nachází skutečný objekt.
* Důvod - místo ve stacku je omezené; objekt je obvykle složitější než hodnotový datový typ a zabírá více místa v paměti; při opakovaném použití objektu se nemusí vytvářet jeho kopie, ale předá se pouze malý hodnotový typ s referencí na objekt.
* Mohou obsahovat hodnotu `null` - označuje, že reference neukazuje na žádná data

### Výčtové
* `enum` - konstanta, nedá se měnit, pouze ke čtení (read-only)
* např. seznam měsíců

## Velikosti hodnotových datových typů
Velikost daného typu proměnné v bytech: https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/operators/sizeof

```
bool 	        1
byte, sbyte 	1
char 	        2
short, ushort  	2
int, uint    	4
float        	4
long, ulong 	8
double       	8
decimal     	16
```

## Základní číselné typy v C# / .NET
### Celočíselné
https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types

* `sbyte` = `System.SByte`: 8bitové celé číslo se znaménkem (-127 až 127)
* `byte` = `System.Byte`: 8bitové celé číslo bez znaménka (0 až 255)
* `short` = `System.Int16`: 16bitové celé číslo se znaménkem (-32 768 až 32 767) 
* `ushort` = `System.UInt16`: 16bitové celé číslo bez znaménka (0 až 65 535)
* `int` = `System.Int32`: 32bitové celé číslo se znaménkem (-2 147 483 648 až 2 147 483 647)
* `uint` = `System.UInt32`: 32bitové celé číslo bez znaménka (0 až 4 294 967 295)
* `long ` = `System.Int64`: 64bitové celé číslo se znaménkem (-9 223 372 036 854 775 808 až 9 223 372 036 854 775 807) 
* `ulong ` = `System.UInt64`: 64bitové celé číslo bez znaménka (0 až 18 446 744 073 709 551 615)

### Desetinné (s plovoucí desetinnou čárkou, floating-point)
https://www.altair.blog/2022/04/decimal-numbers, https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types
 
* `float` = `System.Single`: 32 bitů, přesnost ~6-9 číslic
* `double` = `System.Double`: 64 bitů, přesnost ~15-17 číslic
* `decimal` = `System.Decimal`: 128 bitů, přesnost 28–29 číslic
* nejmenší přesnost má `float`, největší `decimal`

Předdefinované číselné typy v C# a jejich ekvivalenty v .NET jsou zaměnitelné, tj. například následující deklarace deklarují proměnné stejného celočíselného typu:
```
int a = 123;
System.Int32 b = 123;
```
A následující deklarace deklarují proměnné stejného typu s plovoucí desetinnou čárkou:
```
double a = 12.3;
System.Double b = 12.3;
```


## Uložení záporných čísel (přímý, doplňkový kód)

### Přímý kód
* první bit zleva je vyhrazen pro zápis znaménka
* 1 značí záporné číslo
* 0 značí kladné číslo
* změna rozsahu jednoho byte z hodnot 0 - 255 kombinací na -127 až 127
* existují dvě reprezentace nuly +0 a -0
* snadno se dá stanovit absolutní hodnota čísla
* např.:
```
 123 01111011
-123 11111011
   0 00000000
  -0 11111111
```
### Doplňový kód
je-li číslo záporné, provede se na klasickou reprezentaci čísla bitová negace a číslo zvětšíme
o 1

* jediná interpretace nuly
* např.:
```
 123 01111011
-123 10000101
```

## Hodnotové a referenční proměnné
* Hodnotové datové typy obsahují přímo hodnotu, referenčné datové typy obsahují pouze referenci (odkaz) na místo v paměti, kde je uložena hodnota proměnné, nebo má reference hodnotu null.
http://uzlabina2.aspone.cz/dathr.aspx

## Platnost proměnných
* Názvy proměnných musí být jen takové, které umožní jejich jednoznačnou identifikaci


## Operátory
### Aritmetické
* Tyto operátory podporují všechny celočíselné a číselné typy s plovoucí desetinou čárkou
* sčítání `+`, odčítání `-`, násobení `*`, dělení `/`, modulo (zbytek po celočíselném dělení) `%`,
* přírůstek (increment): `++`, snížení (decrement) `--`, může být předponový nebo příponový 

#### Předponový (prefix) vs. příponový (postfix) operátor přírůstku (nebo snížení)
* předponový - hodnota proměnné se zvýší (nebo sníží) už před přiřazením:
```
int a=0;
int b=++a;  // a=1, b=1 
```
* příponový - hodnota proměnné se zvýší (nebo sníží) až po přiřazení:
```
int a=0;
int b=a++;  // a=1, b=0 
```

#### Složené přiřazení:
* `+=`, `-=`, `*=`, `/=`, `%=`
```
int a=0;
a+=10;  // a=10;
```
https://learn.microsoft.com/cs-cz/dotnet/csharp/language-reference/operators/arithmetic-operators

### Relační
* Porovnání (menší než), (větší než), (menší než nebo rovno) a (větší než nebo rovno), označované také jako relační operátory, porovnávají své operandy. Tyto operátory jsou podporovány všemi integrálními číselnými typy a číselnými typy s plovoucí desetinnou čárkou.
* menší než: `<`, větší než: `>`, menší nebo rovno: `<=`, větší nebo rovno: `>=`

### Logické + pravdivostní
Provádějí logické operace s logickými operandy:
* `AND &` - vyhodnocuje vždy obě strany výrazu
* `AND &&` - pokud první strana výrazu není platná, už nevyhodnotí druhou
* `OR ^` - XOR "buď a nebo"
```
Console.WriteLine(true ^ true);    // output: False
Console.WriteLine(true ^ false);   // output: True
Console.WriteLine(false ^ true);   // output: True
Console.WriteLine(false ^ false);  // output: False
```
* `OR |` - vyhodnocuje vždy obě strany výrazu
* `OR ||` - pokud první strana výrazu je platná, už nevyhodnotí druhou

## `enum`
* speciální třída, která reprezentuje konstanty (nemění se, read-only)
https://www.w3schools.com/cs/cs_enums.php

## Přetěžování operátorů
* Umožňuje definovat vlastní funkčnost operátorů nad třídami, nebo strukturami (např. sčítání římských čísel, zlomků atd.)

např.:
```
public static Fraction operator +(Fraction a) => a;
public static Fraction operator -(Fraction a) => new Fraction(-a.num, a.den);

public static Fraction operator +(Fraction a, Fraction b) => new Fraction(a.num * b.den + b.num * a.den, a.den * b.den);
```
https://learn.microsoft.com/cs-cz/dotnet/csharp/language-reference/operators/operator-overloading
