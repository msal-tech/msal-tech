---
name: Сообщение об ошибке в работе
about: Сообщите о проблеме в работе приложения/библиотеки
    (краши, некорректное поведение, баги)
title: '[Ошибка в работе] Краткое описание проблемы'
labels: 'Ошибка в работе'
assignees: ''
---

Благодарим за вклад в развитие проекта!
Пожалуйста, опишите обнаруженную проблему в работе приложения, используя
эту форму.

Для эффективной обработки:
- Перед созданием сообщения проверьте актуальность версии кода
- Формулируйте информацию лаконично и четко
- Ограничьте одно сообщение описанием **одной проблемы**
- Указывайте точные ссылки на проблемные места
- Перед отправкой проверьте корректность заполнения

---

## Категория проблемы
Выберите тип ошибки:
- [ ] Критический сбой (краш приложения)
- [ ] Некорректное поведение функционала
- [ ] Ошибка обработки данных
- [ ] Утечка памяти/ресурсов
- [ ] Необработанное исключение
- [ ] Проблемы совместимости
- [ ] Другое: ____

---

## Локализация
Укажите точное место в коде:
- Компонент: (API / UI / БД / иное)
- Версия: (v2.1.0 / commit a1b2c3d)
- Файл/модуль:
- Метод/функция:
- Связанные тикеты: (JIRA-ID/GH-Issue):
- Другое: ____

---

## Детализация
Опишите проблему и условия её проявления.

Примеры:
- POST /api/v1/payments вызывает 500 ошибку при сумме > 10000
- Рендер графиков падает при 10k+ точек данных
- Утечка 2MB/сек в WebSocket-обработчике

**Суть проблемы:** ____

---

# Шаги воспроизведения:
1. Запустите сервер с параметрами...
2. Отправьте запрос на эндпоинт...
3. Наблюдайте исключение в...

**Фактический результат:**
[Опишите наблюдаемое поведение]

**Ожидаемый результат:**
[Как должно работать по документации]

---

## Предлагаемое исправление
Если есть возможность, предложите исправленную версию кода.
Опишите как должно быть правильно.
- **Текущий вариант:**
```python
for num in range(-10, 11):
    print(1 / num)
```
- **Предлагаемое исправление:**
```python
for num in range(-10, 11):
    if num != 0:
        print(1 / num)
```
- **Пояснение:** исправление ошибки деления на нуль.

**Ваше предложение:**
- **Текущий вариант:**
```[язык]
[Текущая проблемная реализация]
```
- **Предлагаемое исправление:**
```[язык]
[Предлагаемое исправление]
```
- **Пояснение:**  ____

---

## Контекст выполнения
Для воспроизводимости укажите:
- Устройство (например, iPhone 15 Pro):
- Операционная система (например, iOS 17.2.1):
- Версия языка: (Python 3.11.4)
- Зависимости: (requirements.txt / package.json)
- Окружение: (Docker, OS, версия библиотеки)
- Другое: ____

---

## Дополнительные материалы
Приложите (по возможности):
- Логи ошибок/краш-репорты
- Профилирование памяти/CPU (для перфоманс-проблем)
- Сравнение с эталонной реализацией (benchmarks)
- Ссылки на документацию/стандарты
- Минимальный воспроизводимый пример (MRE)
- HAR-файл/снимок сети
- Скриншот интерфейсной ошибки
- Другое: ____
