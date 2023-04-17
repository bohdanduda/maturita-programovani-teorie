# Reflexe
## Type
* Datový typ, který popisuje všechny informace o datovém typu, na kterém ho zavoláme
* získáme ho z instance pomocí metody `GetType()`
## PropertyInfo
* Všechny informace o vlastnostech třídy
* Vypíšeme je cyklem `foreach`
* Do vlastností třídy můžeme zapisovat pomocí metody `SetValue()`
## MethodInfo
* Všechny informace o metodách třídy
* Vypíšeme je cyklem `foreach`
* Metodu můžeme zavolat pomocí metody `Invoke()`
## přístup k private
* Přístupk privátním metodám nebo vlastnostem provádíme tak, že při zadávaní jména přidáme bindingFlags
* příklad:
* FieldInfo field = type.GetField("jméno", BindingFlags.Instance | BindingFlags.NonPublic) 
## tvorba instancí (volání konstruktoru)
## volání metod podle názvu (Invoke)
## Atributy (anotace)
