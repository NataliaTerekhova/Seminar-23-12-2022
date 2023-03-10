# Инструкция для работы с Git

## Что такое Git?
***Git*** - самая популярная реализация респределенной системы контроля версий (версионность поддерживается и на сервере, и у каждого клиента). Самой распространенной реализацией ***Git*** является (GitHub)[http://github.com]

## Подготовка репозитория
Для создания репозитория используется команда *git inint* . для этого необходимо открыть в терминале папку с будущим репозиторием и написать *git init*.

## Создание коммитов

Для создания новой фиксации (коммита) используется команда *git commit* . В терминале с папкой-репозиторием пишем: *git commit -m <сообщение к коммиту>* Сообщение к коммиту писать ***обязятельно***

### Добавление файлов к коммиту
Для добавления файла к новому коммиту используется команда *git add*. В терминале с папкой репозитория нужно написать: *git add <название файла>*

## Перемещение между коммитами
Для перемещения на другую фиксацию (коммит) используется команда *git checkout*. Для этого необходимо, как показано в прошлом пункте, в журнале изменений найти необходимый коммит и его хэш (номер), после чего в терминале с папкой-репозиторием надо написать *git checkout <хэш коммита>*. После выполнения этой команды мы попадаем в состояние **detached head**, в котором никакие следующие коммиты сохраняться не будут. Для выхода из этого состояния необходимо написать *git checkout master*.

## Журнал изменений
Для просмотра истории изменений используется команда *git log*. В терминале с папкой-репозиторием необходимо написать *git log*.

## Ветки в Git

Ветка в *Git* — это простой перемещаемый указатель на один коммитов. По умолчанию, имя основной ветки в *Git* — master .

### Создание веток в *Git*
Для создания новой ветки используется команда *git branch <имя ветки>*

### Просмотр списка веток
Для просмотра списка веток в терминале с папкой-репозиторием введите комнаду *git branch* . Выделенная зеленым ветка со звездочкой - это ветка, на которой мы нахлдимся в данный момент. 

### Перемещение между ветками
Для перехода на другую ветку введите в терминале с папкой-репозиторием команду *git checkout <имя ветки>. Такая ветка должна ***существовать***.


## Слияние веток и разрешение конфликтов

Для слияния веток сначалf перейдите в основную ветку (master) при помощи команды *git checkout master*, затем используйте команду *git merge <имя ветки, которую хотите присоединить>*

Обычно конфликты возникают, когда два человека изменяют одни и те же строки в файле или один разработчик удаляет файл, который в это время изменяет другой разработчик. В таких случаях *Git* не может автоматически определить, какое изменение является правильным. Конфликты затрагивают только того разработчика, который выполняет слияние. *Git* сделает все возможное, чтобы объединить файлы, но оставит конфликтующие участки, чтобы вы разрешили их вручную.


## Удаление веток
Чтобы удалить лишние ветки после слияния используйте команду *git branch --d <имя ветки>* 
