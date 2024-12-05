
## Описание проекта

**Graph Editor** — это приложение на C++ для работы с графами различных видов. Программа предоставляет инструменты для создания, редактирования, визуализации и анализа графов. Поддерживаются операции с несколькими графами, экспорт и импорт данных, а также сложные аналитические функции.

---

## Основные возможности

### Редактирование графов
- **Работа с несколькими графами (MDI)**: Возможность открывать и редактировать несколько графов одновременно.
- **Назначение имен графам**: Каждому графу можно задать уникальное имя.
- **Сохранение и загрузка графов**: Поддержка сохранения в собственный внутренний формат.
- **Экспорт и импорт**: 
  - Текстовый формат для описания графа (см. ниже).
  - Поддержка импорта из и экспорта в простой текстовый файл.
- **Редактирование узлов и дуг**:
  - Создание, удаление и перемещение узлов.
  - Создание ориентированных и неориентированных дуг.
  - Изменение содержимого узлов (текст, ссылки).
  - Задание цветов и форм узлов, а также цветов дуг.

### Дополнительные функции (*)
- **Выделение и копирование**: Выделение нескольких элементов (узлов и дуг) для копирования и вставки.
- **Петли и кратные дуги**: Поддержка циклов и множественных связей между узлами.

---

### Анализ графов

#### Основные функции
1. **Информация о графе**:
   - Количество вершин и дуг.
   - Степени всех вершин.
   - Матрицы инцидентности и смежности.
2. **Проверка свойств графа**:
   - Дерево.
   - Полный граф.
   - Связный граф.
   - Эйлеров граф.
3. **Поиск путей и расстояний**:
   - Все пути между двумя узлами.
   - Кратчайший путь (алгоритмы Дейкстры, Флойда-Уоршелла).
   - Расстояние между двумя узлами.
4. **Характеристики графа**:
   - Диаметр, радиус, центр графа.

#### Дополнительные функции (*)
- **Раскраска графа**: Автоматическая раскраска с минимальным числом цветов.
- **Циклы**: Нахождение эйлеровых и гамильтоновых циклов.
- **Операции над графами**:
  - Объединение, пересечение, дополнение.
- **Приведение к определенным типам**:
  - Бинарное дерево.
  - Полный граф.
  - Связный граф.

---

## Архитектура

### Основные классы:
1. **`Graph`**: Хранение структуры графа и методы редактирования.
2. **`Node`** и **`Edge`**: Узлы и дуги как базовые элементы графа.
3. **`GraphEditor`**: Управление интерфейсом и взаимодействием с пользователем.
4. **`GraphAnalyzer`**: Реализация алгоритмов анализа графов.

### Технологический стек:
- **Язык программирования**: C++.
- **Библиотеки**:
  - Qt — интерфейс пользователя.
  - Boost Graph Library (BGL) — работа с графами.
  - STL — контейнеры и алгоритмы.

---

## Формат текстового файла

### Пример:
```plaintext
GraphName: MyGraph
Nodes:
    A [label="Start", color="red"];
    B [label="Middle", color="blue"];
    C [label="End"];
Edges:
    A -> B [weight=2, color="black"];
    B -> C [weight=3];
    C -> A [weight=1];
