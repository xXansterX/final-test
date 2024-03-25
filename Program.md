using System;

class Program
{
    static void Main()
    {
        string[] originalArray = { "Hello", "2", "world", ":-)" };
        
        // Подсчет строк подходящих под условие.
        int count = 0;
        foreach (var str in originalArray)
        {
            if (str.Length <= 3)
            {
                count++;
            }
        }
        string[] newArray = new string[count];
        int index = 0;
        foreach (var str in originalArray)
        {
            if (str.Length <= 3)
            {
                newArray[index++] = str;
            }
        }
        Console.WriteLine("Original array: [" + string.Join(", ", originalArray) + "]");
        Console.WriteLine("Filtered array: [" + string.Join(", ", newArray) + "]");
    }
}
