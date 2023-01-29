# øídící struktury
* 3 druhy struktur programu:
1. posloupnost pøíkazù – všechny pøíkazy se postupnì provedou jeden po druhém
2. vìtvení (èi podmínìný pøíkaz) – v závislosti na splnìní podmínky se urèitý pøíkaz buï provede nebo neprovede
3. cyklus – v závislosti na splnìní podmínky se èást programu vykoná vícekrát
## podmínky
### IF
*  podmínìný pøíkaz a podmínìná konstrukce jsou prostøedky, které umožòují rozdílné chování programu, v závislosti na specifikované logické podmínce. Výsledek podmínky je buï `true` nebo `false`
* `IF..GOTO` - Napodobuje typickou strojovou instrukci GOTO, která umožòuje skok na urèitý øádek kódu
* `IF..THEN` - Pokud je podmínka v èásti IF vyhodnocena jako pravda, je vykonán kód specifikovaný v èásti THEN. Když není, je kód v èásti THEN vynechán a program pokraèuje dál.
* `IF..THEN..ELSE` - Pokud podmínka v èásti IF není vyhodnocena jako pravda, provede se kód v èásti `ELSE`

### SWITCH a CASE
* switch porovnává pøedanou hodnotu s pøedem specifikovanými konstantami. V pøípadì shody hodnoty s konstantou, vykoná pøíkaz, který je definován za ní

## cykly
* cyklus je øídící struktura, kde se opakovanì provádí posloupnost pøíkazù. Opakování i ukonèení cyklu je øízeno nìjakou podmínku
* existuje mnoho druhù cyklù:
* `WHILE` - pokud platí podmínka, cyklus bìží furt dokola
* `DO-WHILE` - cyklus s podmínkou na konci posloupnosti pøíkazù
* `FOR` - speciální pøípad cyklu s podmínkou na zaèátku, obvykle užívaný pro výèet prvkù z množiny prvkù
## výjimky (try-and-catch)
* funkce zpracování výjimek jazyka C# pomùžou øešit neoèekávané nebo výjimeèné situace, ke kterým dochází pøi spuštìní programu
* výjimky se vytváøejí pomocí `THROW (exeption)`
* pomocí pøíkazù `TRY` a `CATCH` nejdøíve zkusíme zda je kód funkèní, pokud ne tak `CATCH` "chytí" chybu a vykoná definovaný pøíkaz