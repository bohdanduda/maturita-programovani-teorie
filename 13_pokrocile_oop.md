# pokročilé prvky OOP
## statické vlastnosti a metody
#### Metody
* Statická metoda uchovává pouze jednu kopii metody na úrovni typu, nikoli na úrovni objektu
* Poslední aktualizováná hodnota metody je sdílena mezi všemi objekty daného typu - všechny instance třídy sdílejí přesnou kopii metody a její data
* Statické metody se volají pomocí názvu třídy, nikoli instance třídy
* Příklad statických metod: `Console.WriteLine()`, `Console.ReadKey()`. Tyto metody voláme přes jméno třídy Console, aniž bysme ji v kódu inicializovali
#### Vlastnosti
* Statické proměnné mají stejnou hodnotu ve všech instancích objektu.. proto se používají k definování konstant.
* Jejich hodnoty lze získat voláním třídy, aniž by bylo nutné vytvořit její instanci.
* Abychom mohli manipulovat s jejich hodnotami, a používat je, musíme použít statické funkce
* Deklarujeme je použitím `static` modifikátoru
## statický konstruktor
* Statický konstruktor se používá k inicializaci jakýchkoli statických dat nebo k provedení určité akce, kterou je třeba provést pouze jednou.
* Je volán automaticky před vytvořením první instance nebo před odkazem na statické členy. Statický konstruktor bude zavolán nejvýše jednou. 
* Deklarujeme je použitím `static` modifikátoru
## vnitřní třídy
* Třída, která je ve třídě
* může mít další vnitřní třídy - není omezené
## generické třídy
* Pracují s nějakým datovým typem, mají je za sebou v `<``>`, počet parametrů není omezen
* můžeme použít klauzuli where
## generické metody
* čímkoliv naplním metodu, vrátí stejný typ

* příklad s extrakcí čísel z stringů
* Funkce bere jiný datový typ než vrací

* složitá na výrobu
