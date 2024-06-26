# Task 1

## Задание

На языке Python или C++ написать алгоритм (функцию) определения четности целого числа, который будет аналогичен нижеприведенному по функциональности, но отличен по своей сути. Объяснить плюсы и минусы обеих реализаций.

Пример:
```python
def isEven(value):
    return value % 2 == 0
```

## Тесты

Можно запустить, с помощью:
`pytest -s task1`

## Результаты тестов

- Время выполнения is_even: 0.8610043525695801
- Время выполнения is_even_bitwise: 0.7839422225952148
- Время выполнения is_even для отрицательных: 0.8378450870513916
- Время выполнения is_even_bitwise для отрицательных: 0.7929728031158447
- Время выполнения is_even для больших чисел: 0.9102687835693359
- Время выполнения is_even_bitwise для больших чисел: 0.9359309673309326

## is_even()

Плюсы:

- Легко читается. Даже без комментариев понятно, как работает.
- Не требует знаний битовой арифметики.
- В моих тестах отрабатывает быстрее побитовой функции на больших числах. (скорее особенность python)

Минусы:

- Модульное деление медленнее, чем битовые операции, в большинстве случаев (проверено на тестах)

## is_even_bitwise()

Плюсы:

- Время исполнения не зависит от знака числа

Минусы:

- Может быть менее очевидным для тех, кто не знаком с битовыми операциями.

