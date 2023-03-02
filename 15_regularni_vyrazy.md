# regulární výrazy
* regulární výraz je vzor, který se používá k analýze a kontrole, zda zadaný vstupní text odpovídá danému vzoru
* .NET poskytuje engine, který takovéhle porovnávání umožňuje
## Třída Regex
* Třída Regex představuje engine regulárních výrazů.
* Lze ji použít k rychlému rozboru velkého množství textu za účelem nalezení specifických vzorů znaků, k extrakci, úpravě, nahrazení nebo odstranění textových podřetězců a k přidání extrahovaných řetězců do kolekce pro generování sestavy
* Regex můžeme například využít pro validaci jestli je daný řetěžec v Email formátu
* Obsahuje několik statických metod:

* `Escape` - Escapes regex metacharacters within a string
* `Unescape`- Unescapes any escaped characters within a string
* `IsMatch` - Vrací boolean pokud se zadaný výraz shoduje s řetězcem
* `Match` - Metoda vrací __Match__ instanci
* `Matches` - Metoda vrací list __Match__ instanci jako kolekci
* `Replace` - Metoda nahradí vyhledávaný řetězec za řetězec zvolený
* `Split` - Metoda vrací pole řetězců určené výrazem

* Implementace třídy __Regex__ `Regex regex = new Regex("Test");`
## Významy jednotlivých znaků
* `\` - Označí následující znak jako speciální znak nebo escapuje literál
* `^` - V závislosti na tom, zda je nastavena možnost MultiLine, odpovídá pozici před prvním znakem v řádku nebo prvnímu znaku v řetězci
* `$` - V závislosti na tom, zda je nastavena možnost MultiLine, odpovídá pozici za posledním znakem v řádku nebo poslednímu znaku v řetězci
* `*` - Shoduje se s předchozím znakem nulakrát nebo vícekrát. Například `zo*` odpovídá buď "z", nebo "zoo"
* `+` - Shoduje se s předchozím znakem jedenkrát nebo vícekrát. Například `zo+` odpovídá "zoo", ale ne "z"
* `?` - Shoduje se s předchozím znakem nulakrát nebo jednou. Například `a?ve?` odpovídá znaku "ve" ve slově "never" 
* `.` - Shoduje se s libovolným jednotlivým znakem kromě znaku nového řádku
* `(pattern)` - Shoduje se se vzorem a zapamatuje si shodu. Shodný podřetězec lze načíst z výsledné kolekce Matches pomocí položky [0]...[n]
* `(?<name>pattern)` - Shoduje se se vzorem a dává shodě jméno
* `(?:pattern)` - Skupina, která nezachycuje
* `(?=...)` - Positive lookahead
* `(?!...)` - Negative lookahead
* `(?<=...)` - Positive lookbehind
* `(?<!...)` - Negative lookbehind
* `x|y` - Shoduje se s x nebo y. Například `z|wood` se shoduje s "z" nebo "wood". `(z|w)oo` odpovídá "zoo" nebo "wood"
* `{n}` - n je nezáporné celé číslo. Shoduje se přesně n-krát. Například `o{2}` neodpovídá písmenu "o" ve slově "Bob", ale odpovídá prvním dvěma písmenům "o" ve slově "foooood"
* `{n,}` -  Shoduje se alespoň n-krát. Například `o{2,}` se neshoduje s "o" ve slově "Bob", ale shoduje se se všemi "o" ve slově "foooood". `o{1,}` je ekvivalentní `o+`. `o{0,}` je ekvivalentní `o*`
* `{n,m}` - m a n jsou nezáporná celá čísla. Shoduje se nejméně nkrát a nejvýše mkrát. Například `o{1,3}` odpovídá prvním třem o ve slově "fooooood". `o{0,1}` je ekvivalentní `o?`
* `[xyz]` - Znaková sada. Shoduje se s libovolným z přiložených znaků. Například `[abc]` odpovídá znaku "a" ve slově "plain"
* `[^xyz]` - Sada záporných znaků. Shoduje se s jakýmkoli neuzavřeným znakem. Například `[^abc]` odpovídá znaku "p" ve slově "plain"
* `[a-z]` - Rozsah znaků. Shoduje se s libovolným znakem v zadaném rozsahu. Například `[a-z]` odpovídá libovolnému znaku malé abecedy v rozsahu "a" až "z"
* `[^m-z]` - Negativní rozsah znaků. Shoduje se s libovolným znakem, který není v zadaném rozsahu. Například `[^m-z]` odpovídá libovolnému znaku malé abecedy který není v rozsahu "m" až "z"
* `\b` - Shoduje se s hranicí slova, tj. pozici mezi slovem a mezerou. Například `er\b` odpovídá "er" ve slově "never", ale ne "er" ve slově "verb"
* `\B` - Shoduje se s neslovní hranicí. `ea*r\B` odpovídá "ear" ve slově "never early"
* `\d` - Shoduje se s číselnými charaktery. Ekvivalentní `[0-9]`
* `\D` - Shoduje se s jiným než číselným znakem. Ekvivalentní `[^0-9]`
* `\f` - Shoduje se s formulářovým znakem
* `\k` - Zpětný odkaz na pojmenovanou skupinu
* `\n` - Shoduje se se znakem nového řádku
* `\r` - Matches a carriage return character
* `\s` - Shoduje se s jakýmkoli white-space včetně mezery, tabulátoru, posuvníku atd. Ekvivalent: `[ \f\n\r\t\v]`
* `\S` - Shoduje se s jakýmkoli znakem, který není white-space. Ekvivalent: `[^ \f\n\r\t\v]` 
* `\t` - Shoduje se s charakterem tabulátoru
* `\v` - Odpovídá znaku svislého tabulátoru
* `\w` - Shoduje se s libovolným znakem slova včetně podtržítka. Ekvivalent `[A-Za-z0-9_]`
* `\W` - Shoduje se s libovolným neslovním znakem. Ekvivalent `[^A-Za-z0-9_]` 
* `\num` - Odpovídá num, kde num je celé kladné číslo. Například `(.)\1` odpovídá dvěma po sobě jdoucím stejným znakům
* `\A` - Shoduje se s pozicí před prvním znakem v řetězci. Není ovlivněno nastavením MultiLine
* `\Z` - Shoduje se s pozicí za posledním znakem řetězce. Není ovlivněno nastavením MultiLine
* `\G` - Určuje, že shody musí být po sobě jdoucí, bez jakýchkoli neshodných znaků


* _\n_ 	Matches n, where n is an octal escape value. Octal escape values must be 1, 2, or 3 digits long. For example, "\11" and "\011" both match a tab character. "\0011" is the equivalent of "\001" & "1". Octal escape values must not exceed 256. If they do, only the first two digits comprise the expression. Allows ASCII codes to be used in regular expressions.
* _\xn_ 	Matches n, where n is a hexadecimal escape value. Hexadecimal escape values must be exactly two digits long. For example, "\x41" matches "A". "\x041" is equivalent to "\x04" & "1". Allows ASCII codes to be used in regular expressions.
* _\un_ 	Matches a Unicode character expressed in hexadecimal notation with exactly four numeric digits. "\u0200" matches a space character. 
