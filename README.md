# Домашнее задание к работе 11

## Условие задачи
С одномерным массивом, состоящим из n вводимых с клавиатуры положительных и отрицательных целых чисел выполнить следующие вычисления: 
Количество элементов массива, значения которых больше заданного числа A.
## 1. Алгоритм и блок-схема

### Алгоритм
1. **Начало**
2. Объявить переменных:
   - `n` - размер массива.
   - `A` - число для сравнения.
   - `count = 0` - счетчик элементов.
   - `*arr` - указатель на массив.
3. Ввод размера массива.
4. Заполнение массива.
5. Ввод числа А.
6. Подсчет элементов > А.
   - for(int i = 0; i < n; i++) {
         if(arr[i] > A) {
             count++;
         }
     }
7. Вывод результатов:
   printf("\nМассив: ");
   for(int i = 0; i < n; i++) {
         printf("%d ", arr[i]);
     }
   printf("\nКоличество элементов больше %d: %d\n", A, count);
8. **Конец**

### Блок-схема 
<img width="724" height="924" alt="image" src="https://github.com/user-attachments/assets/91e01081-0a44-42c1-ba4f-2aa24580be39" />


## 2. Реализация программы
#include <stdio.h>
#include <locale.h>
#include <stdlib.h>

int main() {
    setlocale(LC_ALL, "RUS");
    int n, A, count = 0;
    int* arr;

    printf("Введите количество элементов массива: ");
    scanf("%d", &n);

    arr = (int*)malloc(n * sizeof(int));
    if (arr == NULL) {
        printf("Ошибка выделения памяти!\n");
        return 1;
    }

    printf("Введите %d элементов массива:\n", n);
    for (int i = 0; i < n; i++) {
        printf("Элемент %d: ", i + 1);
        scanf("%d", &arr[i]);
    }

    printf("Введите число A для сравнения: ");
    scanf("%d", &A);

    for (int i = 0; i < n; i++) {
        if (arr[i] > A) {
            count++;
        }
    }

    printf("\nМассив: ");
    for (int i = 0; i < n; i++) {
        printf("%d ", arr[i]);
    }
    printf("\nКоличество элементов больше %d: %d\n", A, count);

    free(arr);

    return 0;
}

## 3. Результаты работы программы
<img width="539" height="376" alt="image" src="https://github.com/user-attachments/assets/ec016a02-d405-47bf-8603-9e4c19610216" />


