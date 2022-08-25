# Файл Readme по VSC  

## Сайт для тренировки навыков GIT: https://learngitbranching.js.org  

## Основные команды Git
+ **git init** – инициализация локального репозитория  
+ **git status** – получить информацию от git о его текущем состоянии  
+ **git add имя_файла** – добавить файл или файлы к следующему коммиту  
+ **git commit -m “message”** – создание коммита.  
+ **git reset хэш коммита** - отменяет коммит
+ **git revert хэш коммита** - отменяет коммит, создавая коммит об этом действии  
+ **git restore хэш коммита** - сброс состояния файла до того, на которое указать
+ **git log** – вывод на экран истории всех коммитов с их хеш-кодами  
+ **git reflog** - выводит на экран полную истоию всех измнений, в том числе удаления коммитов  
+ **git log graph** - вывод на экран истории всех коммитов с графическими ветками 
+ **git checkout** – переход от одного коммита к другому (а также между ветками)  
+ **git checkout -b имя_ветки** - создание новой ветки и переход на нее  
+ **git checkout имя_ветки^** - переместиться на один коммит вверх по ветке  
+ **git checkout имя_ветки^^** - переместиться на два коммита вверх по ветке  
+ **git checkout Имя_ветки~num** - переместиться на указанное num количество коммитов вверх по ветке
+ **git branch** - вывод списка всех веток
+ **git branch имя_ветки** - создание новой ветки 
+ **git branch -f имя_ветки номер коммита/HEAD^/HEAD~num** - переносит ветку на указанный коммит или на указанное число коммитов от HEAD
+ **git checkout master** – вернуться к актуальному состоянию и продолжить работу  
+ **git diff** - позволяет увидеть разницу между текущим файлом и законченным файлом  
+ **git merge имя_ветки** - слияние ветки с той веткой, в котрой находишься в данный момент
+ **git rebase имя_ветки** - переносит все изменения ветки так что все изменения выглядят последовательно выполненными  
+ **git reset HEAD~1/имя_ветки** - отмена изменений на один коммит (работает для локального репозитория, но не работает для удаленного)  
+ **git revert имя_ветки** - отменяте одно изменение и делится этим изменением с пользователями этого репозитория  
+ **git cherry-pick <commit 1> <commit 2> <...>** - копирует несколько коммитов на то место, где сейчас находишься (для использования этой команды нужно точно знать хэши нужных коммитов)  

## Создание удаленного репозитория на GitHub

**…or create a new repository on the command line
echo "# GIT-instruction" >> README.md**   
+ git init  
+ git add README.md  
+ git commit -m "first commit"  
+ git branch -M main  
+ git remote add origin https://github.com/Datitov1986/GIT-instruction.git  
+ git push -u origin main  

**…or push an existing repository from the command line**  
+ git remote add origin https://github.com/Datitov1986/GIT-instruction.git  
+ git branch -M main  
+ git push -u origin main  
…or import code from another repository  
You can initialize this repository with code from a Subversion, Mercurial, or TFS project.


## Выделение текста  
Чтобы выделить текст курсива необходимо текст заключить в знаки "*" *Курсив* или знак нижнего подчеркивания, например _так_ 
Чтобы выделить текст полужирным необходимо текст заключить в двойные звездочки **Полужирный** или двойные нижние подчеркивания __вот так__  
Альтернативные способы выделения текста курсивом или жирным нужны для того, чтобы мы могли совмещать оба этих способа. Например: _текст может быть выделен курсивом и при этом быть **полужирным**_
## Списки  
Для добавления ненумерованных списков нужно поставить знак "*" или знаком "+" перед тектом
* Элемент 1
* Элемент 2
* Элемент 3  
+ Элемент 4  

Для добавления нумерованных списков нужно поставить цифру
1. Первый элемент нумерованного списка
2. Второй элемент
## Работа с изображениями  
Чтобы добавить изображение в текст необходимо сделать следующее:
![Это моя блок-схема](Homework.png)  
Категорически приветсвую всех присутсвующих на семинаре!  
> Попробую блок цитирования  

Для добавления таблицы в markdown нужно заключить столбцы в "|", а разделить строки "--------". Вот так:  
|Table | Столбец 1 | Столбец 2  | Столбец 3|
|------|-----------|------------|----------|
| Text | Текст 1   | Текст 2    | Текст 3  |
| Like | Таким образом создается таблица| Не очень удобно конечно| Но что делать
|Simple| Как-то так| Пора заканчивать| Последняя запись|

Также таблицы можно выполнять с отступами от краев

|Column left  |Column center  |Column right  |
|:-----------|:-------------:|-------------:|
|Примерно так это выглядит| С центровкой по середине| И по правому краю|
|Не удобно работать с таблицами| Это вам не ворд| Но ко всему можно привыкнуть|

# **Работа с удалнным репозиторием**
Для работы с удаленным репозиторием необходимо:
1. Зарегистрироваться на сервисе (например GitHub)
2. Сделайте fork проекта.
3. Склонируйте репозиторий.
4. Создайте ветку для своей работы.
5. Сделайте необходимые изменения в файлах — коде, документации, тестах. Закоммитьте их в только что созданную ветку.
6. Убедитесь, что проект работает после ваших изменений.
7. Сделайте Pull Request.
8. Обсудите его с рецензентом в процессе Code Review. При необходимости, внесите изменения в свой Pull Request.
9. Когда все довольны, Pull Request принимают — с этого момента ваши изменения попали в исходный репозиторий (upstream) и являются частью проекта.  
## Некоторые команды для работы с удаленным репозиторием:

|команда	|что делает    |
|:----------:|:-------------|
|git remote -v|	# показать список удалённых репозиториев, связанных с локальным|
|git clone (код)|	клонирует удаленный репозиторий в локальный|
|git pull|	влить изменения с удаленного репозитория|
|git push|	отправить в удаленный репозиторий|
|git fetch origin|	скачать ветки удаленного репозитория, но не сливать со своими|
