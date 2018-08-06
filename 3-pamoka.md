## Metodai

1. Parašykite metodą `Pasisveikink`.

```c#
class Program
{
    static void Main(string[] args)
    {
        Pasisveikink("Labas");
        Console.Read();
    }

    public static void Pasisveikink(string pasveikinimoTekstas)
    {
        Console.WriteLine(pasveikinimoTekstas);
    }
}
```

2. Parašyti metodą, kuris prašo įvesti du skaičius ir apkeičia juos vietomis. Pvz.: input – 2,3 result – „Pirmas skaičius yra 3, antras skaičius yra 2“.

```c#
class Program
{
    static void Main(string[] args)
    {
        //metodas yra void ir atspausdina pats
        ApkeiskVietomis1(10, 8);

        //metodas grazina string'a, kuri turim atspausdinti patys
        var tekstas = ApkeiskVietomis2(10, 8);
        Console.WriteLine(tekstas);

        Console.Read();
    }

    //Galima dviem budais:
    public static void ApkeiskVietomis1(int sk1, int sk2)
    {
        Console.WriteLine($"Pirmas skaicius yra {sk1}, o antras - {sk2}");
    }

    public static string ApkeiskVietomis2(int sk1, int sk2)
    {
        return $"Pirmas skaicius yra {sk1}, o antras - {sk2}";
    }
}
```

3. Parašyti metodą, kuris suskaičiuoja žmogaus kūno masės indeksą. Formulė svoris kg / (ūgis metrais) ^ 2).

```c#
class Program
{
    static void Main(string[] args)
    {
        const double ugis = 1.78;
        const double svoris = 200;

        var kmi = KMI(ugis, svoris);

        Console.Read();
    }

    public static double KMI(double ugisMetrais, double svorisKg)
    {
        return svorisKg / ugisMetrais * ugisMetrais;
    }
}
```
4. Papildyti 3-io pratimo programą parašant metodą, kuris pagal gautą KMI nustato žmogaus fizinę būseną (Šis metodas savyje turi iškviesti KMI skaičiuojantį metodą)

```c#
class Program
{
    static void Main(string[] args)
    {
        const double ugis = 1.78;
        const double svoris = 200;

        NustatykFizineBukle(ugis, svoris);

        Console.Read();
    }

    public static void NustatykFizineBukle(double ugisMetrais, double svorisKg) 
    {
        var kmi = KMI(ugisMetrais, svorisKg);
        if(kmi < 15) 
        {
            Console.WriteLine("Badaujantis žmogus");
        }
        else if(kmi < 18.5) {
            Console.WriteLine("Liesas žmogus");
        }
        else if (kmi < 25)
        {
            Console.WriteLine("Normalaus svorio žmogus");
        }
        else if (kmi < 30)
        {
            Console.WriteLine("Turintis viršsvorio žmogus");
        }
        else if (kmi < 40)
        {
            Console.WriteLine("Nutukęs žmogus");
        }
        else
        {
            Console.WriteLine("Ligotai nutukęs žmogus");
        }
    }

    public static double KMI(double ugisMetrais, double svorisKg)
    {
        return svorisKg / ugisMetrais * ugisMetrais;
    }
}
```

5. Parašykite metodą, kuris atspausdina gautą masyvą į vieną eilutę su tarpais

```c#
class Program
{
    static void Main(string[] args)
    {
        int[] manoMasyvas = { 1, 3, 6, 8, 9, 10 };
        AtspausdinkMasyva(manoMasyvas);
        Console.Read();
    }

    public static void AtspausdinkMasyva(int[] masyvas)
    {
        foreach(var elementas in masyvas)
        {
            Console.Write($"{elementas} ");
        }
        Console.WriteLine();
    }
}
```
