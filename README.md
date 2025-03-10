# Описание проекта

Этот проект представляет собой систему для автоматического извлечения и суммаризации текста из PDF-файлов, в частности, резюме (CV). Используется модель T5 для создания кратких аннотаций текста, что позволяет эффективно обрабатывать большие объемы информации. 
Система автоматически извлекает текст из PDF-документов, разбивает его на блоки для суммаризации и генерирует краткий вывод, который помогает быстро ознакомиться с основными фактами, такими как личные данные, опыт работы и ключевые навыки.

## Что было сделано

- **Извлечение текста из PDF:** Реализована функция для извлечения текста из PDF-файлов с помощью библиотеки PyMuPDF (fitz).
- **Суммаризация текста:** Используется модель `rut5_base_sum_gazeta` для сокращения текста и создания кратких аннотаций на основе информации, извлеченной из документа.
- **Обработка длинных текстов:** Тексты, превышающие допустимую длину для модели, разбиваются на блоки, которые суммаризируются по отдельности, а затем комбинируются в итоговый вывод.
- **Автоматизация работы с резюме:** Реализована основная функция, которая принимает файл резюме, извлекает из него текст, а затем создает суммарное описание.

## Использованные технологии

- **Язык программирования:** Python 3.x
- **Модели и API:**
  - T5 (`IlyaGusev/rut5_base_sum_gazeta`) для создания суммаризаций текста.
- **Библиотеки для работы с PDF:** PyMuPDF (fitz) для извлечения текста из PDF.
- **Библиотеки для обработки текста:** Huggingface Transformers для загрузки и использования предобученных моделей.
