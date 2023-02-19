# řídící struktury
* 3 druhy struktur programu:
1. posloupnost příkazů – všechny příkazy se postupně provedou jeden po druhém (psaní kódu po řádcích)
2. větvení (či podmíněný příkaz) – v závislosti na splnění podmínky se určitý příkaz buď provede nebo neprovede (podmíněný příkaz `if`)
3. cyklus – v závislosti na splnění podmínky se část programu vykoná vícekrát (příkazy `while`, `for`, `foreach`)
## podmínky
### IF
*  podmíněný příkaz a podmíněná konstrukce jsou prostředky, které umožňují rozdílné chování programu, v závislosti na specifikované logické podmínce. Výsledek podmínky je buď `true` nebo `false`
* `IF..GOTO` - Napodobuje typickou strojovou instrukci GOTO, která umožňuje skok na určitý řádek kódu
* `IF..THEN` - Pokud je podmínka v části IF vyhodnocena jako pravda, je vykonán kód specifikovaný v části THEN. Když není, je kód v části THEN vynechán a program pokračuje dál.
* `IF..THEN..ELSE` - Pokud podmínka v části IF není vyhodnocena jako pravda, provede se kód v části `ELSE`
* Syntaxe `IF`
![If syntaxe](https://cdn.programiz.com/sites/tutorial2program/files/if-else-statement-csharp.png)


### SWITCH a CASE
* switch porovnává předanou hodnotu s předem specifikovanými konstantami. V případě shody hodnoty s konstantou, vykoná příkaz, který je definován za ní
* Syntaxe `CASE`
![Case syntaxe](https://miro.medium.com/max/1110/1*jgsNHffPE39208jn4cUI6g.png)
* Case jako logický příkaz
  ```
  int x = int.Parse(Console.ReadLine());
  switch (true)
  {
    case true when x == 2:
        Console.WriteLine("2");
    break;  
  }
  ```

## cykly
* cyklus je řídící struktura, kde se opakovaně provádí posloupnost příkazů. Opakování i ukončení cyklu je řízeno nějakou podmínku
* existuje mnoho druhů cyklů:
* `WHILE` - první se vyhodnotí podmínka, potom se spustí kód. Pokud platí podmínka, cyklus běží furt dokola (jde vytvořit nekonečná smyčka: `WHILE(true)`)
* `DO-WHILE` - první se spustí kód, potom se vyhodnotí podmínka
* `FOR` - speciální případ cyklu s podmínkou na začátku, obvykle užívaný pro výčet prvků z množiny prvků (`FOR(; ;)` - nekonečná smyčka jako u `WHILE(true)`)

## Enumerator


## výjimky (try-and-catch)
* funkce zpracování výjimek jazyka C# pomůžou řešit neočekávané nebo výjimečné situace, ke kterým dochází při spuštění programu
* výjimky se vytvářejí pomocí `THROW (exeption)`
* pomocí příkazů `TRY` a `CATCH` nejdříve zkusíme zda je kód funkční, pokud ne tak `CATCH` "chytí" chybu a vykoná definovaný příkaz
