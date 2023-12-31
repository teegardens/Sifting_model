## Симуляция движения частиц через сито

Этот репозиторий содержит Python-скрипт для моделирования просеивания частиц и определения вероятности прохождения через сетку. Ниже представлено краткое описание ключевых компонентов кода:

### Введенные понятия
В коде используются следующие понятия:
- **Сито** разделено на полосы вдоль двух осей - X и Y, каждая полоса имеет номер в пределах от 0 до m-1.
- **Номер ячейки** - пара номеров полос по обеим осям, например: (12, 7).
- **Относительные координаты** - связаны с начальным положением частицы; начало координат - левый нижний угол частицы, оси совпадают с её гранями.
- **Абсолютные координаты** - связаны с ситом; начало координат - левый нижний угол ячейки под номером (0, 0).
- **"Активная" ячейка** - та, в которую попала хотя бы одна вершина.

### Константы
- **D**: Размер сита.
- **m**: Число ячеек.
- **a**: Ширина ячейки.
- **b, k**: Размеры частиц и соотношение сторон.

### Основные функции
1. **initialize_state**: Инициализирует состояние частицы после встряхивания, учитывая размеры и угол поворота.
2. **is_passing**: Определяет, проходит ли частица сквозь сито. Возвращает 0, 1 или 2 в зависимости от результата.
3. **get_passing_probability**: Оценивает вероятность прохождения частиц через сетку.

### Проведение экспериментов
- **parts_on_grid_plot**: Создает графическое представление сетки и моделирует движение нескольких частиц через сито. Отображает результаты на графике.
- **get_probability_grid**: Проводит серию экспериментов с разными параметрами и строит таблицу вероятностей прохождения частиц для различных значений b/a и k.
- **Графики полученного распределения**: Визуализирует результаты экспериментов в 3D и 2D графиках.
