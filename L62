using System;

public class MathOperations
{
    // Перевантажений метод додавання для чисел
    public static int Add(int a, int b)
    {
        return a + b;
    }

    // Перевантажений метод додавання для масивів чисел
    public static int[] Add(int[] arr1, int[] arr2)
    {
        if (arr1.Length != arr2.Length)
        {
            throw new ArgumentException("Array lengths must be equal.");
        }

        int[] result = new int[arr1.Length];
        for (int i = 0; i < arr1.Length; i++)
        {
            result[i] = arr1[i] + arr2[i];
        }

        return result;
    }

    // Перевантажений метод додавання для матриць
    public static int[,] Add(int[,] matrix1, int[,] matrix2)
    {
        int rows = matrix1.GetLength(0);
        int cols = matrix1.GetLength(1);

        if (rows != matrix2.GetLength(0) || cols != matrix2.GetLength(1))
        {
            throw new ArgumentException("Matrix dimensions must be equal.");
        }

        int[,] result = new int[rows, cols];
        for (int i = 0; i < rows; i++)
        {
            for (int j = 0; j < cols; j++)
            {
                result[i, j] = matrix1[i, j] + matrix2[i, j];
            }
        }

        return result;
    }

    // Додайте інші методи для віднімання, множення тощо...
}

class Program
{
    static void Main()
    {
        // Приклад використання
        int sum1 = MathOperations.Add(5, 3);
        Console.WriteLine($"Sum of numbers: {sum1}");

        int[] array1 = { 1, 2, 3 };
        int[] array2 = { 4, 5, 6 };
        int[] sum2 = MathOperations.Add(array1, array2);
        Console.WriteLine($"Sum of arrays: [{string.Join(", ", sum2)}]");

        int[,] matrix1 = { { 1, 2 }, { 3, 4 } };
        int[,] matrix2 = { { 5, 6 }, { 7, 8 } };
        int[,] sum3 = MathOperations.Add(matrix1, matrix2);
        Console.WriteLine("Sum of matrices:");
        for (int i = 0; i < sum3.GetLength(0); i++)
        {
            for (int j = 0; j < sum3.GetLength(1); j++)
            {
                Console.Write($"{sum3[i, j]} ");
            }
            Console.WriteLine();
        }
    }
}
