# regul�rn� v�razy
* regul�rn� v�raz je vzor, kter� se pou��v� k anal�ze a kontrole, zda zadan� vstupn� text odpov�d� dan�mu vzoru
* .NET poskytuje engine, kter� takov�hle porovn�v�n� umo��uje
## T��da Regex
* T��da Regex p�edstavuje engine regul�rn�ch v�raz�.
* Lze ji pou��t k rychl�mu rozboru velk�ho mno�stv� textu za ��elem nalezen� specifick�ch vzor� znak�, k extrakci, �prav�, nahrazen� nebo odstran�n� textov�ch pod�et�zc� a k p�id�n� extrahovan�ch �et�zc� do kolekce pro generov�n� sestavy
* Regex m��eme nap��klad vyu��t pro validaci jestli je dan� �et�ec v Email form�tu
* Obsahuje n�kolik statick�ch metod:

* `Escape` - Escapes regex metacharacters within a string
* `Unescape`- Unescapes any escaped characters within a string
* `IsMatch` - Vrac� boolean pokud se zadan� v�raz shoduje s �et�zcem
* `Match` - Metoda vrac� __Match__ instanci
* `Matches` - Metoda vrac� list __Match__ instanci jako kolekci
* `Replace` - Metoda nahrad� vyhled�van� �et�zec za �et�zec zvolen�
* `Split` - Metoda vrac� pole �et�zc� ur�en� v�razem
## V�znamy jednotliv�ch znak�
* `\` - Ozna�� n�sleduj�c� znak jako speci�ln� znak nebo escapuje liter�l
* `^` - V z�vislosti na tom, zda je nastavena mo�nost MultiLine, odpov�d� pozici p�ed prvn�m znakem v ��dku nebo prvn�mu znaku v �et�zci
* `$` - V z�vislosti na tom, zda je nastavena mo�nost MultiLine, odpov�d� pozici za posledn�m znakem v ��dku nebo posledn�mu znaku v �et�zci
* `*` - Shoduje se s p�edchoz�m znakem nulakr�t nebo v�cekr�t. Nap��klad `zo*` odpov�d� bu� "z", nebo "zoo"
* `+` - Shoduje se s p�edchoz�m znakem jedenkr�t nebo v�cekr�t. Nap��klad `zo+` odpov�d� "zoo", ale ne "z"
* `?` - Shoduje se s p�edchoz�m znakem nulakr�t nebo jednou. Nap��klad `a?ve?` odpov�d� znaku "ve" ve slov� "never" 
* `.` - Shoduje se s libovoln�m jednotliv�m znakem krom� znaku nov�ho ��dku
* `(pattern)` - Shoduje se se vzorem a zapamatuje si shodu. Shodn� pod�et�zec lze na��st z v�sledn� kolekce Matches pomoc� polo�ky [0]...[n]
* `(?<name>pattern)` - Shoduje se se vzorem a d�v� shod� jm�no
* `(?:pattern)` - Skupina, kter� nezachycuje
* `(?=...)` - Positive lookahead
* `(?!...)` - Negative lookahead
* `(?<=...)` - Positive lookbehind
* `(?<!...)` - Negative lookbehind
* `x|y` - Shoduje se s x nebo y. Nap��klad `z|wood` se shoduje s "z" nebo "wood". `(z|w)oo` odpov�d� "zoo" nebo "wood"
* `{n}` - n je nez�porn� cel� ��slo. Shoduje se p�esn� n-kr�t. Nap��klad `o{2}` neodpov�d� p�smenu "o" ve slov� "Bob", ale odpov�d� prvn�m dv�ma p�smen�m "o" ve slov� "foooood"
* `{n,}` -  Shoduje se alespo� n-kr�t. Nap��klad `o{2,}` se neshoduje s "o" ve slov� "Bob", ale shoduje se se v�emi "o" ve slov� "foooood". `o{1,}` je ekvivalentn� `o+`. `o{0,}` je ekvivalentn� `o*`
* `{n,m}` - m a n jsou nez�porn� cel� ��sla. Shoduje se nejm�n� nkr�t a nejv��e mkr�t. Nap��klad `o{1,3}` odpov�d� prvn�m t�em o ve slov� "fooooood". `o{0,1}` je ekvivalentn� `o?`
* `[xyz]` - Znakov� sada. Shoduje se s libovoln�m z p�ilo�en�ch znak�. Nap��klad `[abc]` odpov�d� znaku "a" ve slov� "plain"
* `[^xyz]` - Sada z�porn�ch znak�. Shoduje se s jak�mkoli neuzav�en�m znakem. Nap��klad `[^abc]` odpov�d� znaku "p" ve slov� "plain"
* `[a-z]` - Rozsah znak�. Shoduje se s libovoln�m znakem v zadan�m rozsahu. Nap��klad `[a-z]` odpov�d� libovoln�mu znaku mal� abecedy v rozsahu "a" a� "z"
* `[^m-z]` - Negativn� rozsah znak�. Shoduje se s libovoln�m znakem, kter� nen� v zadan�m rozsahu. Nap��klad `[^m-z]` odpov�d� libovoln�mu znaku mal� abecedy kter� nen� v rozsahu "m" a� "z"
* `\b` - Shoduje se s hranic� slova, tj. pozici mezi slovem a mezerou. Nap��klad `er\b` odpov�d� "er" ve slov� "never", ale ne "er" ve slov� "verb"
* `\B` - Shoduje se s neslovn� hranic�. `ea*r\B` odpov�d� "ear" ve slov� "never early"
* `\d` - Shoduje se s ��seln�mi charaktery. Ekvivalentn� `[0-9]`
* `\D` - Shoduje se s jin�m ne� ��seln�m znakem. Ekvivalentn� `[^0-9]`
* `\f` - Shoduje se s formul��ov�m znakem
* `\k` - Zp�tn� odkaz na pojmenovanou skupinu
* `\n` - Shoduje se se znakem nov�ho ��dku
* `\r` - Matches a carriage return character
* `\s` - Shoduje se s jak�mkoli white-space v�etn� mezery, tabul�toru, posuvn�ku atd. Ekvivalent: `[ \f\n\r\t\v]`
* `\S` - Shoduje se s jak�mkoli znakem, kter� nen� white-space. Ekvivalent: `[^ \f\n\r\t\v]` 
* `\t` - Shoduje se s charakterem tabul�toru
* `\v` - Odpov�d� znaku svisl�ho tabul�toru
* `\w` - Shoduje se s libovoln�m znakem slova v�etn� podtr��tka. Ekvivalent `[A-Za-z0-9_]`
* `\W` - Shoduje se s libovoln�m neslovn�m znakem. Ekvivalent `[^A-Za-z0-9_]` 
* `\num` - Odpov�d� num, kde num je cel� kladn� ��slo. Nap��klad `(.)\1` odpov�d� dv�ma po sob� jdouc�m stejn�m znak�m
* `\A` - Shoduje se s pozic� p�ed prvn�m znakem v �et�zci. Nen� ovlivn�no nastaven�m MultiLine
* `\Z` - Shoduje se s pozic� za posledn�m znakem �et�zce. Nen� ovlivn�no nastaven�m MultiLine
* `\G` - Ur�uje, �e shody mus� b�t po sob� jdouc�, bez jak�chkoli neshodn�ch znak�


* _\n_ 	Matches n, where n is an octal escape value. Octal escape values must be 1, 2, or 3 digits long. For example, "\11" and "\011" both match a tab character. "\0011" is the equivalent of "\001" & "1". Octal escape values must not exceed 256. If they do, only the first two digits comprise the expression. Allows ASCII codes to be used in regular expressions.
* _\xn_ 	Matches n, where n is a hexadecimal escape value. Hexadecimal escape values must be exactly two digits long. For example, "\x41" matches "A". "\x041" is equivalent to "\x04" & "1". Allows ASCII codes to be used in regular expressions.
* _\un_ 	Matches a Unicode character expressed in hexadecimal notation with exactly four numeric digits. "\u0200" matches a space character. 