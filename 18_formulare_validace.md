# Formuláře
## validace vstupních hodnot
* Uživatel může zadat chybné údaje, jakkoli a kdykoli chce, proto musíme použít validaci.
* Základní strategie validace: žádat po uživateli furt to stejné, dokud nenapíše data ve správném formátu.
## validace na úrovni formuláře a položky
## ErrorProvider
* ErrorProvider je třída, která poskytuje uživatelské rozhraní pro označení, že ovládací prvek ve formuláři má přidruženou chybu.
* Je to jednoduchý mechanismus, který uživateli oznamuje, že ovládací prvek ve formuláři obsahuje chybu. Pokud je pro ovládací prvek zadán řetězec popisu chyby, zobrazí se vedle něj ikona.
## aplikace regulárních výrazů
* Další problém při validaci může nastat, pokud uživatel zadá zakázaný charakter např. do vstupu pro jméno napíše `#`
* Takovýhle problém detekujeme pomocí třídy `Regex`
