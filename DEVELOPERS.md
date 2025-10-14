# Руководство по развертыванию среды разработки для участников проекта

## 1. Установка зависимостей
Эта инструкция поможет вам установить Quarto и все необходимые зависимости для
работы над проектом.

Установите или обновите до актуальных версий все обязательные зависимости:
1. [**Git**](https://git-scm.com/downloads).
2. [**Pandoc**](https://pandoc.org/installing.html).
3. [**Python**](https://www.python.org/downloads/) до версии 3.13.
4. [**Quarto**](https://quarto.org/docs/get-started/)
  - Плагин Quarto: [**pyodide**](https://github.com/coatless-quarto/pyodide)
  - Плагин Quarto: [**quarto-quiz**](https://github.com/parmsam/quarto-quiz)

Установите или обновите до актуальных версий все не обязательные зависимости:
1. [**Poetry**](https://python-poetry.org/docs/#installation)
  - [**poetry-plugin-exec**](https://pypi.org/project/poetry-plugin-exec/) 
  - [**poetry-plugin-export**](https://pypi.org/project/poetry-plugin-export/)
  - [**poetry-plugin-shell**](https://pypi.org/project/poetry-plugin-shell/)

## 2. Клонирование репозитория
1. Создайте [форк](https://github.com/msal-tech/msal-tech/fork) данного
репозитория.
2. Получите локальную версию репозитория:
```bash
git clone https://github.com/ваш-username/msal-tech.git
```
3. Перейдите в папку проекта
```bash
cd msal-tech
```

## 3. Создание виртуального окружения
Данный пункт не обязателен, но очень желателен.

1. С использованием [**venv**](https://docs.python.org/3/library/venv.html):

В папке проекта выполните:
```bash
python -m venv путь/до/желаемого/расположения/venv
```

2. С использованием [**Poetry**](https://python-poetry.org/docs/#installation):

В папке проекта выполните:
```bash
$eval (poetry env activate)
```
или (при установленном [**poetry-plugin-shell**](https://pypi.org/project/poetry-plugin-shell/))
```
poetry shell
```

## 4. Установка необходимых пакетов python
Данный пункт не обязателен, но очень желателен.

1. С использованием [**venv**](https://docs.python.org/3/library/venv.html):

В папке проекта выполните:
```bash
python -m pip install pip --upgrade pip
python -m pip install -r requirements.txt
```

2. С использованием [**Poetry**](https://python-poetry.org/docs/#installation):
В папке проекта выполните:
```bash
poetry install
```

## 5. Проверка установки
```bash
quarto check
```
Убедитесь, что все компоненты отмечены как "OK".

## 6. Запуск локального сервера
Для предпросмотра вносимых изменений в реальном времени:
```bash
quarto preview
```
Сайт будет доступен по адресу: `http://localhost:xxxx`,
где `xxxx` - черырехзначный номер порта, зависящий от вашей системы

## 7. Внесение изменений в проект
1. Отредактируйте необходимые файлы, например `отредактированный_файл.qmd`.
2. Добавьте изменения в индекс:
```bash
git add отредактированный_файл.qmd
```
3. Зафиксируйте изменения:
```bash
git commit -m 'Описание сути изменений'
```
4. Отправьте изменения в свой репозиторий:
```bash
git push origin
```
5. Создайте **Pull Request** для добавления ваших изменений в основной репозиторий.
