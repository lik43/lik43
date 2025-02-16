# Проект по определению показаний на аналоговом приборе
## Описание проекта
Этот проект направлен на разработку модели машинного обучения для определения показаний на аналоговых приборах. В качестве основы используется архитектура YOLOv11n.
Датасеты

    * Тренировочный датасет: 23 000 изображений.
    * Валидационный датасет: 2 000 изображений.
    * Тестовый датасет: 1 000 изображений.

## Предобработка данных
Предобработка данных осуществляется в файле **Preprocessing.ipynb**. Она включает в себя следующие шаги:

    * Разархивация zip-файла с изображениями.
    * Уменьшение размера всех тренировочных изображений до (224x224) пикселей и преобразование их в серый цвет.
    * Аугментация данных:
        1. Поворот выбранных картинок на случайный угол в диапазоне от -15 до +15 градусов.
        2. Случайное закрашивание части изображения черным прямоугольником (ширина и высота прямоугольника меняются от 20 до 50 пикселей).
    * Архивация обработанных данных.

## Обучение модели
Обучение модели YOLOv11n происходит в файле **Train.ipynb**. Здесь модель обучается на тренировочных данных, тестируется на валидационных и оценивается по метрикам:

    1. Accuracy
    2. ROC-AUC
    3. F1-score (macro)

## Используемые инструменты и библиотеки
Для реализации этого проекта используются *Jupyter Notebook*, *Python*, *Pillow*, *Albumentations* для обработки изображений и *Ultaralytics*. Необходимые пакеты с версиями лежит в файле *requirement_cv.txt* 


