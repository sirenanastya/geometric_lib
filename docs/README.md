# geometric_lib

Библиотека на Python для вычисления площади и периметра простых фигур.

Состав:

- `circle.py` — круг
- `square.py` — квадрат

## Запуск

Модули лежат в корне проекта. Запускайте примеры из этой папки:

```python   
import circle
import square

print(circle.area(3))
print(circle.perimeter(3))
print(square.area(5))
print(square.perimeter(5))
```

Аргументы — числа `int` или `float`. Отрицательные значения и ноль функциями не проверяются.

## Круг (`circle`)

| Функция | Формула | Что возвращает |
| --- | --- | --- |
| `area(r)` | S = πr² | площадь |
| `perimeter(r)` | P = 2πr | длина окружности |

`r` — радиус. Число π берётся из `math.pi`.

```python
import circle

circle.area(3)       # 28.274333882308138
circle.perimeter(3)  # 18.84955592153876
```

## Квадрат (`square`)

| Функция | Формула | Что возвращает |
| --- | --- | --- |
| `area(a)` | S = a² | площадь |
| `perimeter(a)` | P = 4a | периметр |

`a` — длина стороны.

```python
import square

square.area(5)       # 25
square.perimeter(5)  # 20
```
## История изменений
```
bc70c33 (HEAD -> main) Documentation added
d078c8d (origin/main, origin/HEAD) L-03: Docs added
8ba9aeb L-03: Circle and square added

```