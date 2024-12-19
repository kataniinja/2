# Visualizer

## Описание
`Visualizer` — это инструмент командной строки для визуализации графа зависимостей коммитов в Git-репозитории. Он обходит все коммиты указанной ветки, строит транзитивные зависимости и создает граф в формате PNG с помощью PlantUML.

## Особенности
- Чтение Git-объектов напрямую из `.git/objects`.
- Построение графа зависимостей коммитов, включая сообщения коммитов.
- Визуализация графа в формате PNG с использованием PlantUML.

## Установка
1. Убедитесь, что Python 3.7+ установлен на вашем устройстве.
2. Установите [Java](https://www.oracle.com/java/technologies/javase-downloads.html) и добавьте её в PATH.
3. Скачайте `plantuml.jar` с [официального сайта](https://plantuml.com/download).

## Использование
### Команда запуска
```bash
python visualizer.py <repo_path> <branch_name> <output_image_path> <plantuml_jar_path>
```

### Аргументы
- `<repo_path>`: Путь к анализируемому Git-репозиторию.
- `<branch_name>`: Имя ветки, для которой строится граф.
- `<output_image_path>`: Путь к выходному PNG-файлу.
- `<plantuml_jar_path>`: Путь к файлу `plantuml.jar`.

### Пример
```bash
python visualizer.py "C:\Users\user\my_repo" main "C:\Users\user\graph.png" "C:\Users\user\plantuml.jar"
```

## Тестирование
Проект содержит тесты для всех ключевых функций. Для запуска тестов выполните:
```bash
python -m unittest test_visualizer.py
```
![Скриншот результата](photo/Снимок%20экрана%202024-12-18%20225335.png)