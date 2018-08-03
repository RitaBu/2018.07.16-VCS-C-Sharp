1. Parašyti programą naudojant `while` ciklą, kuri nuskaitinėja įvestus skaičius tol, kol jų suma nėra daugiau 50.

```c#
int sum = 0;
while(sum < 50) 
{
  int number = int.Parse(Console.ReadLine());
  sum += number;
  Console.WriteLine($"suma: {sum} ");
}
Console.ReadLine();
```

2. Parašyti programą naudojant `while` ciklą, kuri nuskaitinėja paspaustus klavišus ir išveda jų pavadinimus tol, kol nepaspaudžiamas ESC klavišas. 

```c#
while(true) 
{
  var key = Console.ReadKey().Key;
  if(key == ConsoleKey.Escape)
  {
    break;
  } 
  else 
  {
    Console.WriteLine(key.ToString());
  }
}
```

3. Parašyti programą naudojant `for` ciklą, kuri suskaičiuoja pirmų 10 natūraliųjų skaičių sumą.

```c#
int sum = 0;
for (var i = 1; i <= 10; i++)
{
  sum += i;
}
Console.WriteLine("sum: " + sum);
Console.ReadKey();
```

4. Parašyti programą naudojant `for` ciklą, kuri prašo įvesti natūralųjį skaičių ir atspausdina visus žemesnius natūraliuosius skaičius mažėjančia tvarka.

```c#
Console.WriteLine("Iveskite skaiciu: ");
int skaicius = int.Parse(Console.ReadLine());

for (var i = skaicius - 1; i > 0; i--) 
{
    Console.WriteLine(i);
}

Console.ReadLine();
```

5. Parašyti programą naudojant for ciklą, kuri prašo įvesti skaičių ir atspausdina jo daugybos lentelę.

```c#
Console.WriteLine("Iveskite skaiciu: ");
int skaicius = int.Parse(Console.ReadLine());

for (var i = 1; i <= 10; i++) 
{
    Console.WriteLine($"{skaicius} * {i} = {skaicius * i}");
}

Console.ReadLine();
```

6. Parašyti programą, kuri nuskaito 10 elementų į masyvą ir jį atspausdina.

```c#
string[] manoMasyvas = new string[10];

for (var i = 0; i < 10; i++ )
{
    var elementas = Console.ReadLine();
    manoMasyvas[i] = elementas;
}

for (var i = 0; i < 10; i++)
{
    Console.WriteLine(manoMasyvas[i]);
}

Console.ReadLine();
```

7. Parašyti programą, kuri prašo įvesti masyvo dydį ir tada nuskaito n elementų į masyvą ir atspausdina jį atvirkščiai.

```c#
Console.Write("Iveskite masyvo dydi: ");
var masyvoDydis = int.Parse(Console.ReadLine());

string[] manoMasyvas = new string[masyvoDydis];

for(var i = 0; i < masyvoDydis; i++)
{
    var elementas = Console.ReadLine();
    manoMasyvas[i] = elementas;
}

for (var i = masyvoDydis - 1; i >= 0; i--)
{
    Console.WriteLine(manoMasyvas[i]);
}

Console.ReadLine();
```

8. Sukurti programą, kuri nuskaitinėja eilutes tol, kol negauna tuščios ir deda eilutes į masyvą. Naudojant foreach ciklą atspausdinti masyvą.

```c#
bool negavauTusciosEilutes = true;
string[] eiluciuMasyvas = new string[10];
int iteratorius = 0;

while (negavauTusciosEilutes)
{
    var eilute = Console.ReadLine();
    if (eilute == "")
    {
        negavauTusciosEilutes = false;
    }
    else 
    {
        eiluciuMasyvas[iteratorius] = eilute;
        iteratorius++;
    }
}

foreach(var eilute in eiluciuMasyvas) 
{
    Console.WriteLine(eilute);
}

Console.ReadLine();
```
