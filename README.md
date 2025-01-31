# KNN-Project

# Sonar Classification Project

## Определение камня или мины

### Описание

Сонар, или ультразвуковой локатор, — это техника, используемая для навигации, коммуникации и определения объектов на воде или под водой. В данном проекте мы будем работать с набором данных, содержащим ответные метрики для 60 различных частот сонара, отправленных на известные объекты — мины и камни.

Для каждого отправленного и полученного сигнала были записаны данные об объекте, на который направлялся сонар (мина или камень). Наша цель — создать модель машинного обучения, которая может определить тип объекта — мина или камень — на основе ответа от сонаров на 60 различных частотах.

### Методы и подходы

В данной работе применяется метод KNN (k-ближайших соседей) для выполнения задачи классификации. Для улучшения качества модели используется пайплайн, который включает в себя следующие компоненты:

1. StandardScaler: Нормализация данных для улучшения сходимости и производительности KNN.
2. KNN Classifier: Основная модель для классификации.

После настройки пайплайна, применяется GridSearchCV для поиска оптимального количества соседей k в модели KNN.

### Задания

1. Создание объекта PipeLine: Создание пайплайна, включающего в себя StandardScaler и модель KNN.
2. Поиск по сетке для k: Применение GridSearchCV для определения оптимального значения k и вывод лучших параметров.
3. График mean_test_score: Построение графика средних тестовых оценок (mean_test_score) для каждого значения k с использованием словаря .cv_results_.

### Финальная оценка модели

Используя объект grid classifier, созданный на предыдущем шаге, создаётся финальный отчёт:

- Classification Report: Подробное представление о качестве классификации.
- Confusion Matrix: Матрица неточностей для визуальной оценки результатов.


