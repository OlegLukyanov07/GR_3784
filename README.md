@@ -0,0 +1,144 @@
**Инструкция для работы с Git и удалёнными репозиториями**
**Что такое Git?**
Git - это одна из реализаций распределённых систем контроля версий, имеющая как и локальные, так и удалённые репозитории. Является самой популярной реализацией систем контроля версий в мире.

**Подготовка репозитория**
Для создание репозитория необходимо выполнить команду git init в папке с репозиторием и у Вас создаться репозиторий (появится скрытая папка .git)

**Создание коммитов**
Git add
Для добавления измений в git initкоммит используется команда git add. Чтобы использовать команду git add напишите git add <имя файла>

**Просмотр состояния репозитория**
Для того, чтобы посмотреть состояние репозитория используется команда git status. Для этого необходимо в папке с репозиторием написать git status, и Вы увидите были ли измения в файлах, или их не было.

**Создание коммитов**
Для того, чтобы создать коммит(сохранение) необходимо выполнить команду git commit. Выполняется она так: git commit -m "<сообщение к коммиту>. Все файлы для коммита должны быть ДОБАВЛЕНЫ и сообщение к коммиту писать ОБЯЗАТЕЛЬНО.

**Перемещение между сохранениями**
Для того, чтобы перемещаться между коммитами, используется команда git checkout. Используется она в папке с пепозиторием следующим образом: git checkout <номер коммита>

**Журнал изменений**
Для того, чтобы посмтреть все сделанные изменения в репозитории, используется команда git log. Для этого достаточно выполнить команду git log в папке с репозиторием

**Ветки в Git**
Создание ветки
Для того, чтобы создать ветку, используется команда git branch. Делается это следующим образом в папке с репозиторием: git branch <название новой ветки>

**Слияние веток**
Для того чтобы дабавить ветку в текущую ветку используется команда git merge

**Удаление веток**
Для удаления ветки ввести команду "git branch -d 'name branch'"
----
Новые записи - уже в ветке test


---
Домашнее задание к Семинару 2.
---
Первый коммит на ветке Master.
Добавление в текст рисунка кота.
![Добавление рисунка кота](kat.jpg)
---
Добавление ненумерованной таблицы
* Первая запись в таблице
* Вторая запись в таблице
* Третья запись в таблице
---
Добавление нумерованной таблицы
1. Первая запись в таблице
2. Вторая запись в таблице
3. Третья запись в таблице
Второй коммит на ветке Master.
---
Создание и добавление контента в ветке Vetka1
Здесь текст в новой ветке
Коммит в ветке Vetka1
---
Создание и добавление контента в ветке Vetka2
Здесь текст в новой ветке
Коммит в ветке Vetka2
--- 
Создание и добавление контента в ветке Vetka3
Здесь текст в новой ветке 
Коммит в ветке Vetka3
--- 
Создание и добавление контента в ветке Vetka4
Здесь текст в новой ветке 
Коммит в ветке Vetka4
---
Создание конфликта текста в ветках Master и Vetka4
Коммит в ветке Vetka4
Переход в ветку Master
Добавление текста
Коммит в ветке Master
Переход в ветку Vetka4
Создание конфликта текста в ветках Master и Vetka4
Коммит в ветке Vetka4
Переход в ветку Master
Мерж с веткой Vetka4 - возникновение конфликта версий в тексте
Решение конфликта
Коммит в ветке Master
---
Мерж с веткой Vetka3
Мерж с веткой Vetka2
Мерж с веткой Vetka1
---
Коммит в ветке Master
Проверка и итоговая правка текста
Коммит в ветке Master
End

**Работа с удаленными репозиториями**

Копировать внешний репозиторий на свой ПК можно командой 
**git clon**

Команда git clone составная: она не только
загружает все изменения, но и пытается слить
все ветки на локальном компьютере и в
удаленном репозитории.
Эта команда позволяет скачать все
из текущего репозитория и автоматически
сделать **merge** с нашей версией

**git push**
Отправить свою версию репозитория во
внешний репозиторий поможет команда **git
push**. При первом её использовании нужна
**git pull** авторизация.
Эта команда позволяет отправить нашу
версию репозитория на внешний
репозиторий. ТРЕБУЕТ АВТОРИЗАЦИИ
на внешнем репозитории.

**Как настроить совместную работу**
1. Создать аккаунт на GitHub.com
2. Создать локальный репозиторий
3. “Подружить” ваш локальный и удалённый репозитории. 

 GitHub при создании нового репозитория подскажет, как это можно сделать
4. Отправить (push) ваш локальный репозиторий в удалённый (на GitHub), при этом, возможно,
вам нужно будет авторизоваться на удалённом репозитории
5. Провести изменения “с другого компьютера”
6. Выкачать (pull) актуальное состояние из удалённого репозитория.

**pull request**
- команда для предложения изменений
- запрос на вливание изменений в репозиторий

В больших компаниях один ответственный за проект создает аккаунт. Другие пользователи дают
команду **pull request**. Предлагать изменения на GitHub нужно в отдельной ветке. Сначала пользователь копирует репозиторий на свой компьютер, делает **fork** репозитория, затем
клонирует версию на своём ПК, создаёт ветку с предлагаемыми изменениями, отправляет изменения командой push в свой аккаунт на GitHub и даёт команду **pull request**.

Как сделать **pull request**
Делаем   (ответвление) репозитория **fork**
Делаем **git clone** версии репозитория СВОЕЙ версии репозитория.
Создаем новую ветку и в НЕЕ вносим свои изменения.
Фиксируем изменения (делаем коммиты).
Отправляем свою версию в свой GitHub.
На сайте GitHub нажимаем кнопку **pull request**.

End
Коммит в ветке Master
