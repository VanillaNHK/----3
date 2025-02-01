def sum_negative_between_min_max(arr):
    # Находим индексы минимального и максимального элементов
    min_index = arr.index(min(arr))
    max_index = arr.index(max(arr))
    
    # Определяем начальный и конечный индексы для суммирования
    start = min(min_index, max_index)
    end = max(min_index, max_index)
    
    # Суммируем отрицательные элементы между start и end
    sum_neg = sum(x for x in arr[start+1:end] if x < 0)
    
    return sum_neg

# Пример использования
A = [3, -1, -4, 2, -5, 7, -2, 8]
result = sum_negative_between_min_max(A)
print("Сумма отрицательных элементов между минимальным и максимальным:", result)
