# formulare
## datagrid
* Ovládací prvek DataGrid ve Windows Forms zobrazuje data v øadì øádkù a sloupcù
* Nejjednodušším pøípadem je, když je møížka vázána na zdroj dat s jedinou tabulkou, která neobsahuje žádné vztahy, v takovém pøípadì se data zobrazují v jednoduchých øádcích a sloupcích
* Pokud je møížka DataGrid svázána s daty s více souvisejícími tabulkami a pokud je v møížce povolena navigace, zobrazí se v každém øádku rozbalovací prvky
### práce s datagridem
 * Pomocí expandéru mùže uživatel pøecházet z nadøazené tabulky do podøazené tabulky
 * Kliknutím na uzel se zobrazí podøízená tabulka a kliknutím na tlaèítko zpìt se zobrazí pùvodní rodièovská tabulka - tímto zpùsobem møížka zobrazuje hierarchické vztahy mezi tabulkami
## pøipojení DataSource
* Aby ovládací prvek DataGrid fungoval, mìl by být svázán se zdrojem dat pomocí vlastností __DataSource__ a __DataMember__ v dobì návrhu nebo metody __SetDataBinding__ v dobì bìhu
* Tato vazba odkazuje DataGrid na instancovaný objekt zdroje dat, napøíklad __DataSet__ nebo __DataTable__, ovládací prvek DataGrid zobrazuje výsledky akcí, které jsou provádìny s daty
## napojení DataModelu na souborové/databásové repository
