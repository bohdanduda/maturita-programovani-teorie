# Proměnné
* Místo paměti počítače, kam si můžeme uložit data.
* Proměnná má vždy nějaký datový typ - číslo, znak, text atd.
## Datové typy
hodnotové, odkazové, výčtové - https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types
* hodnotové: např. `int`, `double`, `bool`, `char`
* odkazové: např. `string`, `object`, `dynamic`
* výčtové: `enum`

## Velikosti
Velikost daného typu proměnné v bytech
    https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/operators/sizeof

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
je-li číslo záporné provede se na klasickou reprezentaci čísla bitová negace a číslo zvětšíme
o 1

* jediná interpretace nuly
* např.:
```
 123 01111011
-123 10000101
```

## desetinná čísla
* `single`, `double`, `decimal`
* nejmenší přesnost má single, největší decimal

    https://www.altair.blog/2022/04/decimal-numbers

## hodnotové a referenční proměnné
* Hodnotové datové typy obsahují přímo hodnotu, referenčné datové typy obsahují pouze referenci (odkaz) na místo v paměti, kde je uložena hodnota proměnné, nebo má reference hodnotu null.
http://uzlabina2.aspone.cz/dathr.aspx

## platnost proměnných
* Názvy proměnných musí být jen takové, které umožní jejich jednoznačnou identifikaci


## operátory
### aritmetické
* Tyto operátory podporují všechny celočíselné a číselné typy s plovoucí desetinou čárkou
* `sčítání: +`, `odčítání: -`, `násobení *`, `dělení: /`, `zbytek: %`,
* `přírůstek: ++`, `dekrement: --` předponové / příponové


* Složené přiřazení:
* `+=`, `-=`, `*=`, `/=`, `%=`

https://learn.microsoft.com/cs-cz/dotnet/csharp/language-reference/operators/arithmetic-operators

### relační
* Porovnání (menší než), (větší než), (menší než nebo rovno) a (větší než nebo rovno), označované také jako relační operátory, porovnávají své operandy. Tyto operátory jsou podporovány všemi integrálními číselnými typy a číselnými typy s plovoucí desetinnou čárkou.

* `menší než: <`, `větší než: >`, `menší nebo rovno: <=`, `větší nebo rovno: <=`


### logické + pravdivostní tabulky
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

## enum
* speciální třída, která reprezentuje konstanty (nemění se, read-only)
https://www.w3schools.com/cs/cs_enums.php

## přetěžování operátorů
* Umožňuje definovat vlastní funkčnost operátorů nad třídami, nebo strukturami (např. sčítání římských čísel, zlomků atd.)

např:
```
public static Fraction operator +(Fraction a) => a;
public static Fraction operator -(Fraction a) => new Fraction(-a.num, a.den);

public static Fraction operator +(Fraction a, Fraction b) => new Fraction(a.num * b.den + b.num * a.den, a.den * b.den);
```
https://learn.microsoft.com/cs-cz/dotnet/csharp/language-reference/operators/operator-overloading
