# Unit testy 
## Princip a využití unit testů
## Testovací třídy
* Příklad testovací třídy
```
[TestClass]
public class UnitTest1
{

}
```
## Testovací metody
* Příklad testovací metody
```
 [DataTestMethod]
        [DataRow(2,2,4)]
        [DataRow(1,3,4)]
        [DataRow(4,4,8)]
        public void TestAdd(double x, double y, double expected)
        {
            Arithmetics arithmetics = new();
            double result = arithmetics.Add(x, y);

            Assert.AreEqual(expected, result);
        }
```
## Pre-testové a post-testové rutiny
### Pre-testové
### Post-testové
## Testování formulářů

https://learn.microsoft.com/en-us/dotnet/core/testing/unit-testing-best-practices
