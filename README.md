**GitHub** платформа для совместной разработки, также называемая форжингом. То есть платформа, ориентированная на сотрудничество между разработчиками для распространения и поддержки их программного обеспечения (хотя постепенно она использовалась для других проектов, помимо программного обеспечения).

Как следует из названия, он опирается на Система контроля версий Git. Таким образом, можно работать с исходным кодом программ и проводить упорядоченную разработку. Также эта платформа написана на Ruby on Rails.

Он имеет огромное количество проектов с открытым исходным кодом, хранящихся на его платформе и общедоступных. Такова его ценность, что Microsoft решила купить эту платформу в 2018 году - не менее 7500 миллиардов долларов.

> **преимущество**
Бесплатное обслуживание, хотя есть и платные.
Очень быстрый поиск в структуре репозиториев.
Большое сообщество и легко найти помощь.
Он предлагает практические инструменты для сотрудничества и хорошую интеграцию с Git.
Легко интегрируется с другими сторонними сервисами.
Он также работает с TFS, HG и SVN.

> **недостатки**
Это не совсем открыто.
У него есть ограничения по пространству, так как вы не можете превышать 100 МБ в одном файле, в то время как репозитории ограничены 1 ГБ в бесплатной версии.

## Основные языки, поддерживаемые функциями GitHub
Основные языки для функций GitHub включают C, C++, C#, Go, Java, JavaScript, PHP, Python, Ruby, Scala и TypeScript. Для функций, поддерживающих диспетчеры пакетов, поддерживаемые сейчас диспетчеры пакетов включены в таблицу с соответствующими языками.

Некоторые функции поддерживаются для дополнительных языков или диспетчеров пакетов. Если вы хотите узнать, поддерживается ли другой язык для функции или запросить поддержку языка, см. обсуждения GitHub Community.

## Отправка фиксаций в удаленный репозиторий
О git push
Переименование ветвей
Обработка ошибок не быстрого перемещения вперед
Отправка тегов
Удаление удаленных ветви или тега
Удаленные репозитории и вилки
Дополнительные материалы
Используйте git push для отправки фиксаций в локальной ветви в удаленный репозиторий.

#### О git push
Команда git push принимает два аргумента:

имя удаленного репозитория, например, origin;
Имя ветви, например main
Пример:

*git push REMOTE-NAME BRANCH-NAME*
Например, вы обычно выполняете команду *git push origin main* для отправки локальных изменений в веб-репозиторий.

#### Переименование ветвей
Чтобы переименовать ветвь, используйте ту же команду git push, добавив к ней еще один аргумент: имя новой ветви. Пример:

*git push REMOTE-NAME LOCAL-BRANCH-NAME:REMOTE-BRANCH-NAME
LOCAL-BRANCH-NAME* отправляется в REMOTE-NAME, но при этом переименовывается в REMOTE-BRANCH-NAME.

#### Обработка ошибок не быстрого перемещения вперед
Если локальная копия репозитория не синхронизирована с вышестоящим репозиторием, в который выполняется отправка, вы получите следующее сообщение: non-fast-forward updates were rejected. В таком случае перед отправкой локальных изменений необходимо извлечь или "получить" изменения из вышестоящего репозитория.

Дополнительные сведения об этой ошибке см. в разделе Обработка ошибок не быстрого перемещения вперед.

#### Отправка тегов
По умолчанию команда *git push* без дополнительных параметров отправляет все ветви, имена которых соответствуют именам удаленных ветвей.

Чтобы отправить отдельный тег, можно использовать ту же команду, что и для отправки ветви:

*git push REMOTE-NAME TAG-NAME*
Чтобы отправить все теги, можно ввести следующую команду:

*git push REMOTE-NAME --tags*

#### Удаление удаленных ветви или тега
На первый взгляд синтаксис удаления ветви может показаться непонятным:

*git push REMOTE-NAME:BRANCH-NAME*
Обратите внимание на пробел, стоящий перед двоеточием. Эта команда напоминает ту, которая используется для переименования ветви. Тем не менее, она указывает Git выполнить пустую отправку в ветвь BRANCH-NAME в репозитории REMOTE-NAME. Таким образом, команда git push удаляет ветвь в удаленном репозитории.

#### Удаленные репозитории и вилки
Безусловно, вы уже знаете, что на GitHub можно создавать "вилки" (Fork) репозиториев.

При клонировании собственного репозитория вы предоставляете ему удаленный URL-адрес, который Git использует для получения и отправки обновлений. Для совместной работы с исходным репозиторием следует добавить в локальный клон Git новый удаленный URL-адрес (обычно называется upstream):

*git remote add upstream THEIR_REMOTE_URL*
Теперь вы можете получать обновления и ветви из их вилки:

>git fetch upstream
Grab the upstream remote's branches
remote: Counting objects: 75, done.
remote: Compressing objects: 100% (53/53), done.
remote: Total 62 (delta 27), reused 44 (delta 9)
Unpacking objects: 100% (62/62), done.
From https://github.com/OCTOCAT/REPO
 \* [new branch]      main     -> upstream/main

После внесения локальных изменений вы можете отправить локальную ветвь в GitHub и инициировать запрос на вытягивание.
