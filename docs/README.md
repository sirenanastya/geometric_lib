# geometric_lib

[![linux](https://img.shields.io/badge/linux-passing-34D058?style=flat&logo=linux&logoColor=white)](https://github.com/sirenanastya/geometric_lib/actions/workflows/linux.yml)
[![macos](https://img.shields.io/badge/macos-passing-34D058?style=flat&logo=apple&logoColor=white)](https://github.com/sirenanastya/geometric_lib/actions/workflows/macos.yml)
[![windows](https://img.shields.io/badge/windows-passing-34D058?style=flat&logo=windows&logoColor=white)](https://github.com/sirenanastya/geometric_lib/actions/workflows/windows.yml)
[![python](https://img.shields.io/badge/python-3-blue.svg)](https://www.python.org/)

Библиотека для вычисления площади и периметра плоских фигур. У каждой фигуры свой модуль и две функции: `area` и `perimeter`. Сторонние пакеты не нужны. Число π берётся из `math.pi`.

## Установка

Пакет не выкладывается в PyPI. Склонируйте репозиторий и запускайте примеры из его корня:

```bash
git clone https://github.com/sirenanastya/geometric_lib.git
cd geometric_lib
```

## Пример

```python
import circle
import rectangle
import square
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

Аргументы — числа `int` или `float`. Ноль, отрицательные числа и посторонние типы библиотека не проверяет.

## Модули

| Модуль | Фигура | Площадь | Периметр |
| --- | --- | --- | --- |
| `circle` | круг | S = πr² | P = 2πr |
| `square` | квадрат | S = a² | P = 4a |
| `rectangle` | прямоугольник | S = ab | P = 2(a + b) |
| `triangle` | треугольник | S = ah / 2 | P = a + b + c |

Для треугольника площадь считается по основанию и высоте, периметр — по трём сторонам.

## Справка

### `circle.area(r)`

Площадь круга.

- **r** (`int` или `float`) — радиус.
- **Возвращает** `float`. Формула: S = πr².

```python
import circle

circle.area(3)  # 28.274333882308138
```

### `circle.perimeter(r)`

Длина окружности.

- **r** (`int` или `float`) — радиус.
- **Возвращает** `float`. Формула: P = 2πr.

```python
import circle

circle.perimeter(3)  # 18.84955592153876
```

### `square.area(a)`

Площадь квадрата.

- **a** (`int` или `float`) — сторона.
- **Возвращает** площадь. Формула: S = a².

```python
import square

square.area(5)  # 25
```

### `square.perimeter(a)`

Периметр квадрата.

- **a** (`int` или `float`) — сторона.
- **Возвращает** периметр. Формула: P = 4a.

```python
import square

square.perimeter(5)  # 20
```

### `rectangle.area(a, b)`

Площадь прямоугольника.

- **a**, **b** (`int` или `float`) — стороны.
- **Возвращает** площадь. Формула: S = ab.

```python
import rectangle

rectangle.area(5, 3)  # 15
```

### `rectangle.perimeter(a, b)`

Периметр прямоугольника.

- **a**, **b** (`int` или `float`) — стороны.
- **Возвращает** периметр. Формула: P = 2(a + b).

```python
import rectangle

rectangle.perimeter(5, 3)  # 16
```

### `triangle.area(a, h)`

Площадь треугольника.

- **a** (`int` или `float`) — основание.
- **h** (`int` или `float`) — высота, проведённая к этому основанию.
- **Возвращает** `float`. Формула: S = ah / 2.

```python
import triangle

triangle.area(4, 3)  # 6.0
```

### `triangle.perimeter(a, b, c)`

Периметр треугольника.

- **a**, **b**, **c** (`int` или `float`) — стороны.
- **Возвращает** периметр. Формула: P = a + b + c.

```python
import triangle

triangle.perimeter(3, 4, 5)  # 12
```

## Структура

```text
geometric_lib/
├── circle.py
├── square.py
├── rectangle.py
├── triangle.py
├── tests/
│   └── test_figures.py
├── .github/
│   └── workflows/
└── docs/
    └── README.md
```

## История изменений

- `70509d1` — добавлены прямоугольник, треугольник и документация
- `28f8c82` — в документацию добавлена история коммитов
- `bc70c33` — добавлена документация
- `d078c8d` — добавлено описание формул
- `8ba9aeb` — добавлены круг и квадрат
