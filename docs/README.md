# geometric_lib

Библиотека на Python для вычисления площади и периметра плоских фигур: круга, квадрата, прямоугольника и треугольника.

## Описание

Каждая фигура вынесена в отдельный модуль. В модуле две функции:

- `area` — площадь;
- `perimeter` — периметр (для круга — длина окружности).

Сторонние пакеты не используются. Для числа π модуль круга обращается к `math.pi`.

## Требования

- Python 3

## Структура проекта

```text
geometric_lib/
├── circle.py
├── square.py
├── rectangle.py
├── triangle.py
└── docs/
    └── README.md
```

| Файл | Фигура |
| --- | --- |
| `circle.py` | круг |
| `square.py` | квадрат |
| `rectangle.py` | прямоугольник |
| `triangle.py` | треугольник |
| `docs/README.md` | документация |

## Установка

Отдельная установка не требуется. Склонируйте репозиторий и запускайте код из корня проекта, чтобы импорт модулей находил файлы `circle.py`, `square.py`, `rectangle.py` и `triangle.py`.

## Использование

```python
import circle
import square
import rectangle
import triangle

print(circle.area(3))
print(circle.perimeter(3))
print(square.area(5))
print(square.perimeter(5))
print(rectangle.area(5, 3))
print(rectangle.perimeter(5, 3))
print(triangle.area(4, 3))
print(triangle.perimeter(3, 4, 5))
```

Аргументы всех функций — числа `int` или `float`. Проверки на ноль, отрицательные значения и нечисловой ввод нет: такие аргументы передаются в формулу как есть.

## Модули

### circle — круг

#### area(r)

Возвращает площадь круга.

| | |
| --- | --- |
| Параметр | `r` (`int` или `float`) — радиус |
| Возвращаемое значение | `float` — площадь |
| Формула | S = πr² |

```python
import circle

circle.area(3)  # 28.274333882308138
```

#### perimeter(r)

Возвращает длину окружности.

| | |
| --- | --- |
| Параметр | `r` (`int` или `float`) — радиус |
| Возвращаемое значение | `float` — длина окружности |
| Формула | P = 2πr |

```python
import circle

circle.perimeter(3)  # 18.84955592153876
```

### square — квадрат

#### area(a)

Возвращает площадь квадрата.

| | |
| --- | --- |
| Параметр | `a` (`int` или `float`) — сторона |
| Возвращаемое значение | `int` или `float` — площадь |
| Формула | S = a² |

```python
import square

square.area(5)  # 25
```

#### perimeter(a)

Возвращает периметр квадрата.

| | |
| --- | --- |
| Параметр | `a` (`int` или `float`) — сторона |
| Возвращаемое значение | `int` или `float` — периметр |
| Формула | P = 4a |

```python
import square

square.perimeter(5)  # 20
```

### rectangle — прямоугольник

#### area(a, b)

Возвращает площадь прямоугольника.

| | |
| --- | --- |
| Параметры | `a`, `b` (`int` или `float`) — стороны |
| Возвращаемое значение | `int` или `float` — площадь |
| Формула | S = ab |

```python
import rectangle

rectangle.area(5, 3)  # 15
```

#### perimeter(a, b)

Возвращает периметр прямоугольника.

| | |
| --- | --- |
| Параметры | `a`, `b` (`int` или `float`) — стороны |
| Возвращаемое значение | `int` или `float` — периметр |
| Формула | P = 2(a + b) |

```python
import rectangle

rectangle.perimeter(5, 3)  # 16
```

### triangle — треугольник

#### area(a, h)

Возвращает площадь треугольника по основанию и высоте.

| | |
| --- | --- |
| Параметры | `a` (`int` или `float`) — основание; `h` (`int` или `float`) — высота, проведённая к этому основанию |
| Возвращаемое значение | `float` — площадь |
| Формула | S = ah / 2 |

```python
import triangle

triangle.area(4, 3)  # 6.0
```

#### perimeter(a, b, c)

Возвращает периметр треугольника по трём сторонам.

| | |
| --- | --- |
| Параметры | `a`, `b`, `c` (`int` или `float`) — стороны |
| Возвращаемое значение | `int` или `float` — периметр |
| Формула | P = a + b + c |

```python
import triangle

triangle.perimeter(3, 4, 5)  # 12
```

## История изменений

- 70509d1 Add rectangle, triangle and project documentation
- 28f8c82 Commit hash history add to docs
- bc70c33 Documentation added
- d078c8d L-03: Docs added
- 8ba9aeb L-03: Circle and square added

