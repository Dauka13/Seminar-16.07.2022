# Инструкция по работе с Git

## Что такое git?
Git - это одна из реализаций распределённых систем контроля версий, что позволяет иметь версионность как в локальном репозитории, так и в удалённом репозитории (общем для всех). Git является на данный момент самой популярной системой контроля версий.

## Подготовка репозитория
Для создания репозитория используется команда *git init*. В терминале в папке с будующим репозиторием достаточно написать *git init*, и эта папка станет репозиторием.

## Создание коммитов

### Просмотр состояния репозитория
Команда *git status* показывает состояния файлов в рабочем каталоге и индексе: какие файлы изменены, но не добавлены в индекс; какие ожидают коммита в индексе. Вдобавок к этому выводятся подсказки о том, как изменить состояние файлов. 

### Добавление файла к сохранению
Для добавления файла в текущий коммит используется команда *git add*. Для этого достаточно в терминале с папкой текущего репозитория написать *git add <название файла>*.

### Фиксация изменений
Сохраниить коммит очень просто. Для сохранения коммита используется команда *git commit*. Для этого в терминале с папкой репозитория, необходимо написать комманду *git commit -m "<сообщение к коммиту>"*. Сообщение к коммиту писать ***ОБЯЗАТЕЛЬНО***.

## Журнал изменений
Для просмотра истории коммитов, то есть истории наших изменений используется команда *git log*. Для этого необходимо в терминале с папкой-репозиторием написать *git log*.

## Перемещение между коммитами
Для того, чтобы перемещаться между коммитами, необходимо использовать команду *git checkout*. Для этого в терминале с папкой репозитория необходимо написать *git checkout <номер коммита>*. Номер коммита берётся из истории изменения. После такого "перемещения" мы попадаем в состояние *Detached head*. Для возвращения в обычное состояние используется команда *git checkout master*.

## Ветки в Git

## Слияние веток и решение конфликтов 

## Удаление веток
Удалить ветку очень просто. Для удаления ветки используется команда *git branch -d <имя ветки>*. 