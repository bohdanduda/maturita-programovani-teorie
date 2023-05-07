# Unit testy 
## Princip a využití unit testů
* Testovat bychom měli úplně všechny public metody na servisách a objektech
* Dobře napsané unit testy slouží jako dokumentace chování aplikace 
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
* Pokud chceme před každým testem spustit stejnou metodu, který nám něco pro test připraví, použijeme anotace `[SetUp]`
### Post-testové
* Pokud chceme po každém testu spustit stejnou metodu, která nám například "uklidí" parametry nastavené v SetUpu, použijeme anotace `[TearDown]`
## Testování formulářů
## Testování výjimek
* Testovaná metoda
```
public double Divide(double x, double y)
{

    if (y == 0)
    {
      throw new ZeroDivisionException(x, y);
    }
    return x / y;
}
```
* Třída výjimky
```
public class ZeroDivisionException : Exception
    {
        public double Dividend { get; set; }
        public double Divisor{ get; set; }

        public ZeroDivisionException(double dividend, double divisor)
        {
            this.Dividend = dividend;
            this.Divisor = divisor;
        }
    }
```
* Test metody
```
[TestMethod]
public void TestDivideByZero()
{
    Arithmetics arithmetics = new();
    try
    {
        double result = arithmetics.Divide(5, 0);

       Assert.Fail("Expected zero division exception");
    }
    catch (ZeroDivisionException e)
    {
        Assert.AreEqual(5, e.Dividend);
        Assert.AreEqual(0, e.Divisor);
    }
}
```
https://learn.microsoft.com/en-us/dotnet/core/testing/unit-testing-best-practices
