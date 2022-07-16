# Инструкция по работе с Git

## Что такое git?
Git - это одна из реализаций распределённых систем контроля версий, что позволяет иметь версионность как в локальном репозитории, так и в удалённом репозитории (общем для всех). Git является на данный момент самой популярной системой контроля версий.

## Подготовка репозитория
Для создания репозитория используется команда *git init*. В терминале в папке с будующим репозиторием достаточно написать *git init*, и эта папка станет репозиторием.

## Создание коммита
Можно создать коммит одной командой, но только для отслеживаемых файлов. В данном случае в индекс добавляются все изменения файлов, но только тех файлов, которые уже когда-либо были добавлены в Git репозиторий — отслеживаемые файлы. То есть новые неотслеживаемые файлы данной командой игнорируются.

### Просмотр состояния репозитория
Команда *git status* показывает состояния файлов в рабочем каталоге и индексе: какие файлы изменены, но не добавлены в индекс; какие ожидают коммита в индексе. Вдобавок к этому выводятся подсказки о том, как изменить состояние файлов. 

### Добавление файла к сохранению
Для добавления файла в текущий коммит используется команда *git add*. Для этого достаточно в терминале с папкой текущего репозитория написать *git add <название файла>*.

### Фиксация изменений
Сохранить коммит очень просто. Для сохранения коммита используется команда *git commit*. Для этого в терминале с папкой репозитория, необходимо написать комманду *git commit -m "<сообщение к коммиту>"*. Сообщение к коммиту писать ***ОБЯЗАТЕЛЬНО***.

## Просмотр изменений до коммита
Можно просматривать список изменений, внесённых в репозиторий, используя команду *git diff*.
По умолчанию отображаются только изменения, не подготовленные для фиксации.

## Журнал изменений
Для просмотра истории коммитов, то есть истории наших изменений используется команда *git log*. Для этого необходимо в терминале с папкой-репозиторием написать *git log*.

## Перемещение между коммитами
Для того, чтобы перемещаться между коммитами, необходимо использовать команду *git checkout*. Для этого в терминале с папкой репозитория необходимо написать *git checkout <номер коммита>*. Номер коммита берётся из истории изменения. После такого "перемещения" мы попадаем в состояние *Detached head*. Для возвращения в обычное состояние используется команда *git checkout master*.

## Ветки в Git
По умолчанию, имя основной ветки в git — master (main). Для того, чтобы создать ответвление в git, необходимо использовать комманду *git branch <имя ветки>*. Для того, чтобы перемещаться между ветками, необходимо использовать команду *git checkout <имя ветки>*. Для возвращения на основную ветку используется команда *git checkout master*.

## Слияние веток и решение конфликтов 
Для того, чтобы произвести слияние веток, необходимо переключиться на ветку, в которую вы хотите включить изменения, и выполнить команду *git merge*. Слияние и конфликты являются неотъемлемой частью работы с Git. Git позволяет выполнять слияния очень просто. В большинстве случаев Git самостоятельно решает, как автоматически интегрировать новые изменения, также конфликты можно решать вручную

## Удаление веток
Удалить ветку очень просто. Для удаления ветки используется команда *git branch -d <имя ветки>*. 

## Получение удалённого репозитория
Для того, чтобы скачать удалённый репозиторий, необходимо использовать команду *git clone*.  

## Отправка измений в удалённый репозиторий
Для отправки изменений в удаленный репозиторий, необходимо использовать команду *git push*