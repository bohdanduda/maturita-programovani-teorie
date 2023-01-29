# regulární výrazy
* regulární výraz je vzor, který se používá k analýze a kontrole, zda zadaný vstupní text odpovídá danému vzoru
* .NET poskytuje engine, který takovéhle porovnávání umožòuje
## Tøída Regex
* Tøída Regex pøedstavuje engine regulárních výrazù.
* Lze ji použít k rychlému rozboru velkého množství textu za úèelem nalezení specifických vzorù znakù, k extrakci, úpravì, nahrazení nebo odstranìní textových podøetìzcù a k pøidání extrahovaných øetìzcù do kolekce pro generování sestavy
* Regex mùžeme napøíklad využít pro validaci jestli je daný øetìžec v Email formátu
* Obsahuje nìkolik statických metod:

* `Escape` - Escapes regex metacharacters within a string
* `Unescape`- Unescapes any escaped characters within a string
* `IsMatch` - Vrací boolean pokud se zadaný výraz shoduje s øetìzcem
* `Match` - Metoda vrací __Match__ instanci
* `Matches` - Metoda vrací list __Match__ instanci jako kolekci
* `Replace` - Metoda nahradí vyhledávaný øetìzec za øetìzec zvolený
* `Split` - Metoda vrací pole øetìzcù urèené výrazem
## Významy jednotlivých znakù
* `\` - Oznaèí následující znak jako speciální znak nebo escapuje literál
* `^` - V závislosti na tom, zda je nastavena možnost MultiLine, odpovídá pozici pøed prvním znakem v øádku nebo prvnímu znaku v øetìzci
* `$` - V závislosti na tom, zda je nastavena možnost MultiLine, odpovídá pozici za posledním znakem v øádku nebo poslednímu znaku v øetìzci
* `*` - Shoduje se s pøedchozím znakem nulakrát nebo vícekrát. Napøíklad `zo*` odpovídá buï "z", nebo "zoo"
* `+` - Shoduje se s pøedchozím znakem jedenkrát nebo vícekrát. Napøíklad `zo+` odpovídá "zoo", ale ne "z"
* `?` - Shoduje se s pøedchozím znakem nulakrát nebo jednou. Napøíklad `a?ve?` odpovídá znaku "ve" ve slovì "never" 
* `.` - Shoduje se s libovolným jednotlivým znakem kromì znaku nového øádku
* `(pattern)` - Shoduje se se vzorem a zapamatuje si shodu. Shodný podøetìzec lze naèíst z výsledné kolekce Matches pomocí položky [0]...[n]
* `(?<name>pattern)` - Shoduje se se vzorem a dává shodì jméno
* `(?:pattern)` - Skupina, která nezachycuje
* `(?=...)` - Positive lookahead
* `(?!...)` - Negative lookahead
* `(?<=...)` - Positive lookbehind
* `(?<!...)` - Negative lookbehind
* `x|y` - Shoduje se s x nebo y. Napøíklad `z|wood` se shoduje s "z" nebo "wood". `(z|w)oo` odpovídá "zoo" nebo "wood"
* `{n}` - n je nezáporné celé èíslo. Shoduje se pøesnì n-krát. Napøíklad `o{2}` neodpovídá písmenu "o" ve slovì "Bob", ale odpovídá prvním dvìma písmenùm "o" ve slovì "foooood"
* `{n,}` -  Shoduje se alespoò n-krát. Napøíklad `o{2,}` se neshoduje s "o" ve slovì "Bob", ale shoduje se se všemi "o" ve slovì "foooood". `o{1,}` je ekvivalentní `o+`. `o{0,}` je ekvivalentní `o*`
* `{n,m}` - m a n jsou nezáporná celá èísla. Shoduje se nejménì nkrát a nejvýše mkrát. Napøíklad `o{1,3}` odpovídá prvním tøem o ve slovì "fooooood". `o{0,1}` je ekvivalentní `o?`
* `[xyz]` - Znaková sada. Shoduje se s libovolným z pøiložených znakù. Napøíklad `[abc]` odpovídá znaku "a" ve slovì "plain"
* `[^xyz]` - Sada záporných znakù. Shoduje se s jakýmkoli neuzavøeným znakem. Napøíklad `[^abc]` odpovídá znaku "p" ve slovì "plain"
* `[a-z]` - Rozsah znakù. Shoduje se s libovolným znakem v zadaném rozsahu. Napøíklad `[a-z]` odpovídá libovolnému znaku malé abecedy v rozsahu "a" až "z"
* `[^m-z]` - Negativní rozsah znakù. Shoduje se s libovolným znakem, který není v zadaném rozsahu. Napøíklad `[^m-z]` odpovídá libovolnému znaku malé abecedy který není v rozsahu "m" až "z"
* `\b` - Shoduje se s hranicí slova, tj. pozici mezi slovem a mezerou. Napøíklad `er\b` odpovídá "er" ve slovì "never", ale ne "er" ve slovì "verb"
* `\B` - Shoduje se s neslovní hranicí. `ea*r\B` odpovídá "ear" ve slovì "never early"
* `\d` - Shoduje se s èíselnými charaktery. Ekvivalentní `[0-9]`
* `\D` - Shoduje se s jiným než èíselným znakem. Ekvivalentní `[^0-9]`
* `\f` - Shoduje se s formuláøovým znakem
* `\k` - Zpìtný odkaz na pojmenovanou skupinu
* `\n` - Shoduje se se znakem nového øádku
* `\r` - Matches a carriage return character
* `\s` - Shoduje se s jakýmkoli white-space vèetnì mezery, tabulátoru, posuvníku atd. Ekvivalent: `[ \f\n\r\t\v]`
* `\S` - Shoduje se s jakýmkoli znakem, který není white-space. Ekvivalent: `[^ \f\n\r\t\v]` 
* `\t` - Shoduje se s charakterem tabulátoru
* `\v` - Odpovídá znaku svislého tabulátoru
* `\w` - Shoduje se s libovolným znakem slova vèetnì podtržítka. Ekvivalent `[A-Za-z0-9_]`
* `\W` - Shoduje se s libovolným neslovním znakem. Ekvivalent `[^A-Za-z0-9_]` 
* `\num` - Odpovídá num, kde num je celé kladné èíslo. Napøíklad `(.)\1` odpovídá dvìma po sobì jdoucím stejným znakùm
* `\A` - Shoduje se s pozicí pøed prvním znakem v øetìzci. Není ovlivnìno nastavením MultiLine
* `\Z` - Shoduje se s pozicí za posledním znakem øetìzce. Není ovlivnìno nastavením MultiLine
* `\G` - Urèuje, že shody musí být po sobì jdoucí, bez jakýchkoli neshodných znakù


* _\n_ 	Matches n, where n is an octal escape value. Octal escape values must be 1, 2, or 3 digits long. For example, "\11" and "\011" both match a tab character. "\0011" is the equivalent of "\001" & "1". Octal escape values must not exceed 256. If they do, only the first two digits comprise the expression. Allows ASCII codes to be used in regular expressions.
* _\xn_ 	Matches n, where n is a hexadecimal escape value. Hexadecimal escape values must be exactly two digits long. For example, "\x41" matches "A". "\x041" is equivalent to "\x04" & "1". Allows ASCII codes to be used in regular expressions.
* _\un_ 	Matches a Unicode character expressed in hexadecimal notation with exactly four numeric digits. "\u0200" matches a space character. 