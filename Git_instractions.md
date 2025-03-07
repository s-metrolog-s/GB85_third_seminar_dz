# Инструкция по работе с GIT

## Установка и начало работы: 
1. Необходимо скачать и установить Git по ссылке:
**https://git-scm.com/downloads**
2. Необходимо скачать и установить VSC по ссылке: **https://code.visualstudio.com/Download**
3. При первом использовании Git необходимо в терминале ввести две команды:

>* git config --global user.name «Ваше имя английскими буквами»  

>* git config --global user.email ваша почта@example.com

## Основные команды:

* **git --version** - проверка текущей установленной версии программы
* **git init** - инициализация локального репозитория для отслеживания, создается скрытая папка
* **git status** - получить информацию от git о его текущем состоянии
* **git add "файл с расширением"** - добавить файл или файлы к индексу для следующего коммита 
* **git commit -m "message text"** - создание коммита, фиксация состояния, сообщение в ковычках. Берет данные из последнего индекса команды add
* **git log** - вывод на экран истории всех коммитов с их хеш-кодами
* **git log --graph** - вывод на экран всех коммитов с визуальным графиком веток и коммитов
* **git checkout <название>** - переход от одного коммита или ветки к другому(ой)
* **git checkout master** - вернуться к актуальному состоянию и продолжить работу
* **git diff** - увидеть разницу между текущим файлом сохраненным на жесткий диск и закоммиченным файлом
* **git branch** - просмотр всех веток в репозитории, текущая со значком (*)
* **git branch <название ветки>** - создание новой ветки
* **git branch -d <название ветки>** - удаление ветки
* **git merge <название ветки>** - слияние ветки с текущей, производим из той, в которую сливаем новую ветку
* **git mv <текущее нзвание файла> <новое название файла>** - позволяет изменить имя или расширение файла

### Работа с удаленными репозиториями:

* **git clone <ссылка на репозиторий>** - копирование внешнего репозитория на локальный компьютер
* **git push** - позволяет отправить локальный репозиторий на внешний репозиторий
* **git pull** - позволяет скопировать все из внешнего репозитория и слить с текущей локальной

## GITIGNORE
В Git не принято добавлять файлы изображений, их хранят на сторонних носителях. Чтобы исключить ненужные файлы из загрузки, есть команда git ignore. Для этого создаем файл с названием **.gitignore** и добавляем в него названия файлов, которые хотим исключить из отслеживания.

## Тезисы с лекций и семинаров:

### Порядок действий для сохранения коммитов:

1. Изменяем файл
2. Сохраняем его
3. git add "имя файла"
4. git commit -m "сообщение"

### Как настроить совместную работу

1. Создать аккаунт на GitHub.com
2. Создать локальный репозиторий
3. "Подружить" локальный и удаленный репозиторий
4. Отправить (push) локальный репозиторий в удаленный, при этом, возможно, потребуется авторизация
5. Провести изменения на другом компьютере
6. Выкачать (pull) актуальное состояние их удаленного репозитория

### Pull request
Команда для предложения изменений.
Запрос на вливание изменений в репозиторий

1. Делаем (ответвление) fork репозитория
2. Делаем git clone СВОЕЙ версии репозитория
3. Создаем новую ветку и в НЕЕ вносим свои изменения
4. Фиксируем изменения (делаем коммиты)
5. Отправляем свою версию в свой GitHub
6. На сайте GitHub нажимаем кнопку pull request

>при создании проекта необходимо сделать инициализацировочный коммит