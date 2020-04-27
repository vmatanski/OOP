# Цикли - обогатяване на данни

Друг основен похват, щом става въпрос за програмирането и писането на код, представляват циклите. Възможноста да се повтаря определен код X пъти. В C# има 4 различни варианта на цикли.

# While loop

While цикъла изпълнява определен код, докато условието е вярно (true). 

```C#
using System;

namespace ConsoleApplication1
{
    class Program
    {
    static void Main(string[] args)
    {
        int number = 0;

        while(number < 5)
        {
        Console.WriteLine(number);
        number = number + 1;
        }

        Console.ReadLine();
    }
    }
}
```

Ако стартираме кода, ще получим като резултат числата от 0 до 4. Първото дефинирано число е 0 (int number = 0) и всеки следващ път, в който кодът се изпълни, числото се увеличава с 1 (number = number + 1 или number += 1). Но защо стига само до 4, при положение, че в условието имаме 5? Това е така, тъй като условието се проверява, преди да се стигне до изпълнението на кода.

# Do loop

Do е огледален пример за While цикъл. В неговия случай, условието се проверява след като кодът е изпълнен. Следователно, в случая на do loop, кодът от цикъла се изпълнява поне веднъж, докато при whilе, може да не се изпълни въобще.

```C#
int number = 0;
do  
{  
    Console.WriteLine(number);  
    number = number + 1;  
} while(number < 5);
```

# For loop

For цикъла е различен. Използва се в случай, когато или знаем точно, колко изпълнения на кода искаме да получим или когато имаме променлива.

```C#
using System;

namespace ConsoleApplication1
{
    class Program
    {
    static void Main(string[] args)
    {
        int number = 5;

        for(int i = 0; i < number; i++)
        Console.WriteLine(i);

        Console.ReadLine();
    }
    }
}
```

В този случай, имаме резултат, като предните два цикъла, но кодът е по-компактен:
- дефинираме си променлива (int i = 0)
- създаваме условие (i < number)
- увеличаваме промелнивата (i++)

Foreach loop

# Този цикъл работи с колекция от неща (обекти, масиви, списъци).

```C#
using System;
using System.Collections;

namespace ConsoleApplication1
{
    class Program
    {
    static void Main(string[] args)
    {        
        ArrayList list = new ArrayList();
        list.Add("John Doe");
        list.Add("Jane Doe");
        list.Add("Someone Else");
        
        foreach(string name in list)
        Console.WriteLine(name);

        Console.ReadLine();
    }
    }
}
```

На първо място си създаваме инстанция на ArrayList и след това добавяме стойности. 
След това използваме foreach цикъл, за да изведем стойностите от списъка. Забележете, че стойностите от списъка са дефинирани като string.
Когато работим с foreach, трябва да знаем, какви данни да изведем. Ако не сме сигурни, можем да работим с обекти, от които да извеждаме различни данни.

Когато се работи с колекция от данни, в повечето случай се ползва foreach.

# Задачи за упражнение

### 1. Решете задачите от Day 1.md, използвайки цикли.