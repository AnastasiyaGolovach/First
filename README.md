#include <stdio.h>
#include <stdlib.h>
#include <locale.h>
int main()
{int a[100], b[100], c[100][100];
    int max, n, s, X, Y, i, e, min, Max, Min, j, k;
    setlocale(LC_ALL, "russian");
    printf("Введите количество строк матрицы \n");
    scanf_s("%d", &n);
    printf("Введите количество столбцов матрицы \n");
    scanf_s("%d", &s);
    printf("\n Вывод элементов матрицы : \n");
    for (X = 0; X < n; X++)
    {
        for (Y = 0; Y < s; Y++)
        {
            c[X][Y] = rand() % 100 - 50;
            printf("%d \t", c[X][Y]);
        }
        printf("\n");
    }
    printf("\nМаксимальные значения в столбцах: ");
    for (Y = 0, i = 0; Y < s; Y++, i++)
    {
        max = c[0][Y];
        for (X = 1; X < n; X++)
            if (c[X][Y] > max)
                max = c[X][Y];
             if (X = n)
            for (; i < s; )
            {
                b[i] = max;
                printf("%d ", b[i]);
                break;
            }
    }
    for (e = 1, min = b[0]; e < s; e++)
    {
        if (min > b[e])
        {
            min = b[e];
        }
    }
    printf("\nМинимальное число среди максимальных в столбцах: %d", min);
    printf("\nМаксимальные значения в строках: ");
    for (X = 0, j = 0; X < n; X++, j++)
    {
        Max = c[X][0];
        for (Y = 1; Y < s; Y++)
            if (c[X][Y] > Max)
                Max = c[X][Y];
        if (Y = s)
            for (; j < n; )
            {
                a[j] = Max;
                printf("%d ", a[j]);
                break;
            }
    }
    for (k = 1, Min = a[0]; k < n; k++)
    {
        if (Min > a[k])
        {
            Min = a[k];
        }
    }
    printf("\nМинимальное число среди максимальных в строках %d", Min);
    return 0;
}
