# Инструкция для работы с Markdown

## Выделение текста

 Заголовок – выделение заголовков (#). Количество символов “#” задаёт уровень заголовка  (поддерживается 6 уровней).


Чтобы выделить текст курсивом нужно обрамить его звездочками
без пробелов (*) или знаком нижнего подчеркивания (_), 
пример *вот так* или _вот так_

Чтобы выделить текст полужирным нужно обрамить его двумя звездочками 
без пробелов(**) или знаком двойного нижнего подчеркивания (__), 
пример **вот так** или __вот так__ 

Альтернативный способ выделения текста курсивом или полужирным, 
нужен нам для совмещения оба этих способа, когда необходимовыделить и полужирным и курсивом, пример: текст может быть выделен _курсивом_ и быть _**полужирным курсивом**_ или ***полужирное курсивное начертание***

Чтобы выделить текст перечеркивающей линией, нужно обрамить наш текст двумя символами (~). Пример: ~~Зачёркнутый текст~~

Подстрочные и надстрочные символы - Подстрочные и надстрочные символы следует использовать только при необходимости для технической точности, например при написании математических формул. Не используйте их для нестандартных стилей, например сносок. Пример написания:

Привет <sub>это подстрочный текст!</sub>     или    
Привет <sup>это надстрочный текст!</sub>

## Работа со списками
Чтобы добавить не нумерованные списки, 
нужно пункты выделить звездочкой (*) или (+) и (-), после звездочки пробел, пример:
* Пункт 1
  - вложенный пунт 1
  - вложенный пунт 2
  - вложенный пунт 2
* Пункт 2
* Пункт 3
+ Пункт 4 

Чтобы добавить нумерованые списки, необходимо их просто пронумеровать, 
пример:
1. Пункт 1
2. Пункт 2
3. Пункт 3

Контрольный список сочетание символов (>*), пример
> * Пункт 1
> * Пункт 2
> * Пункт 3

## Работа с изображениями
Чтобы вставить изображение в текст, необходимо сделать следующее
![Привет, это ХРЮНЯ](Hruna.jpeg)

## Работа с ссылками
![ссылка на справочник языка **Markdown**] (https://learn.microsoft.com/ru-ru/contribute/markdown-reference)

## Работа с таблицами
* Чтобы создать стандартную таблицу с заголовком, вставьте пунктирную линию после первой строки. Чтобы выровнять столбцы, нужно поставить двоеточие (:) перед --- (:--), если нужно выровнять текст по левому краю, если по центру (:---:), если по правому (---:). Пример

>|Это        | заголовок | таблицы    |
>|:----------|----------:|-----------:|
>|здесь      | табличные | значения   |
>|здесь      | еще       | значения   |

* Разрывы строк внутри слов в любой ячейке таблицы
Длинные слова в таблице Markdown могут привести к тому, что таблица сдвинется вправо и станет нечитаемой. Эту проблему можно решить, разрешив отрисовке на сайте документации автоматически вставлять разрывы строк внутри слов при необходимости. Нужно просто заключить таблицу в настраиваемый класс **[!div class="mx-tdBreakAll"]**.

[!div class="mx-tdBreakAll"]
> |Name|Syntax|Mandatory for silent installation?|Description|
> |-------------|----------|---------|---------|
> |Quiet|/quiet|Yes|Runs the installer, displaying no UI and no prompts.|
> |NoRestart|/norestart|No|Suppresses any attempts to restart. By default, the UI will prompt before restart.|
> |Help|/help|No|Provides help and quick reference. Displays the correct use of the setup command, including a list of all options and behaviors.|

* Разрывы строк внутри слов в ячейках второго столбца
Разрывы строк могут вставляться автоматически внутри слов только во втором столбце таблицы. Чтобы разрешить разрывы только во втором столбце, примените класс **mx-tdCol2BreakAll** с помощью синтаксиса переноса **div**, как показано выше.

* Несогласованные значения ширины столбцов между таблицами
Вы можете заметить, что ширина столбцов в таблицах ваших статей не одинаковая или настроена непоследовательно. Такое поведение обусловлено тем, что длина текста в ячейках определяет макет таблицы. К сожалению, нет способа управлять визуализацией таблиц. Это ограничение Markdown. Хотя было бы лучше, если бы ширина столбцов таблицы была согласованной, такое поведение также не лишено некоторых недостатков:
  - Чередование HTML-кода с Markdown делает темы более сложными и может озадачивать участников сообщества.
  - Таблица, которая хорошо выглядит для определенного размера экрана, может в кнечном итоге выглядеть нечитаемой при разных размерах экрана, так как это противоречит принципам адаптивной визуализации.

* Таблицы матриц данных
Таблица матрицы данных содержит заголовок и взвешенный первый столбец. Она позволяет создать матрицу с пустой ячейкой в верхнем углу слева. 

>|                    |Заголовок 1  |Заголовок 2|
>|--------------------|-------------|-----------|
>|**Первый столбец A**|Ячейка 1A    |Ячейка 2A  |
>|**Первый столбец B**|Ячейка 1B    |Ячейка 2B  |

Для каждой запись в первом столбце нужно задать полужирное начертание (**bold**). Иначе таблицы будут недоступны для средств чтения с экрана или недопустимы для сайта документации.

## Работа с цитатами

Блоки цитирования создаются с помощью символа (>) вставляемого перед текстом, пример:
>Блок цитирования

## Основные команды Git

**git init** – инициализация локального репозитория (testovyi vvod)

**git status** – получить информацию от git о его текущем состоянии

**git add** – добавить файл или файлы к следующему коммиту

**git add .** - добавляет все файлы в проекте в отслеживание

**git commit -am “message”**- git add + git commit (Работает только после 1-го ручного добавления в отслеживание)

**git commit -m “message”** – создание коммита.

**git log** – вывод на экран истории всех коммитов с их хеш-кодами

**git checkout** – переход от одного коммита к другому

**git checkout master** – вернуться к актуальному состоянию и продолжить работу

**git diff** – увидеть разницу между текущим файлом и закоммиченным файлом

## Основные команды работы с ветками
- **git branch** – посмотреть список веток в репозитории
   - **git branch** <название ветки> – создать новую ветку
   - **git branch -d <название ветки>** – удалить ветку
- **git checkout <название ветки>** – переход к другой ветке
   - **git checkout -b <название ветки>** – создать новую ветку перейти сразу в нее  
   - **git checkout <название ветки>^** – символ **"^"** или **"~"** в данной команде означает, что мы хотим перейти и просмотреть предпоследний коммит на указанной ветке. А если указать два символа **^^** или **~~**, то просмотрим 3-й с конца коммит и т.д.
- **git log –-graph** - визуализирует коммиты
- **git merge** -используется для слияния одной или нескольких веток в текущую. Затем она устанавливает указатель текущей ветки на результирующий коммит. Т.е. выполняет слияние отдельных направлений разработки, созданных с помощью команды git branch , в единую ветку.


## Работа с сервисом GitHub
>1. Создать аккаунт на сайте GitHub.com. Аккаунт можно назвать как угодно. Затем в правом верхнем углу надо нажать плюсик, выбрать новый репозиторий и дать ему какое-то имя. Остальные параметры оставляем по умолчанию, ничего не редактируем, создаём новый репозиторий. GitHub предлагает советы. Он подсказывает, что можно сделать, чтобы начать работать с этим репозиторием. У нас есть три варианта. 
>   - Можно создать новый репозиторий через терминал и начать с этим работать.
>   - Уже существующий репозиторий привязать к удалённому репозиторию.
>   - Импортировать код из другого репозитория
>2. Создать локальный репозиторий. Для этого надо создать папку, внутри неё вызвать команду **git init**, совершить какие-то действия, создать файлы, внести в них изменения, чтобы появился хотя бы один коммит.
>3. «Подружить» наш локальный и удалённый репозитории. GitHub при создании нового репозитория подскажет, как это можно сделать.
>4. Отправить **(push)** наш локальный репозиторий в удалённый (на GitHub), при этом нам,возможно, потребуется авторизоваться на удалённом репозитории. Если сделаеть это один раз, «подружим» наш редактор **VS Code с GitHub**, в дальнейшем эту операцию
проводить уже не понадобится.
>5. Провести изменения «с другого компьютера» или можно сделать это на GitHub
>6. Выкачать **(pull)** актуальное состояние из удалённого репозитория.

## Полезные команды приработе с удаленным репозиторием
**git clone** - Команда ***git clone*** позволяет копировать или клонировать к себе репозитории из интернета. Для этого мы обращаемся к программе Git, указываем параметр clone и после этого даём адрес того репозитория, который надо скачать. Далее в папке, где вызывается команда ***git clone***, появляется новая папка. И уже внутри этой папки будет лежать полная копия указанного нами репозитория.

**git pull** - Эта команда позволяет получить из интернета актуальное состояние удалённого репозитория и скачать его на наш репозиторий. Обратите внимание, что ***pull*** — составная команда. Помимовыкачивания из интернета, она ещё и мержит, то есть сливает, изменения с нашими. Если возникают какие-то конфликты, то окошко будет таким же, как при конфликтах обычного ***git merge***. То есть коменда состоит из двух частей: первая часть скачивает изменения с удалённого репозитория, а вторая — сливает эти изменения с текущим репозиторием.

**git push** - Эта команда позволяет отправить то, что есть на нашем репозитории, на удалённый репозиторий. Требует авторизации. Если у нет прав на внесение изменений в репозиторий, Git не позволит это делать. На слайде команда указана в усечённом виде, она так работает, когда всё настроено. Если ещё не до конца всё настроено, Git подскажет, как сделать это правильно.

## Групповая работа над большим проектом в GitHub
1. Делаем копию аккаунта, который интересен, к себе.
2. Создаём локальный репозиторий, то есть через ***git clone*** берём его на свой локальный компьютер.
3. Создаём ветку, где делаем изменения, которые хотели бы предложить.
4. Направляем свои изменения в собственный аккаунт, и появляется кнопка для отправки — ***pull request***.

## Создание кнопки pull request
1. Делаем форк (fork "вилка"- переносим на наш акаунт в GitHub) интересующего нас репозитория.
2. Делаем git clone для нашей версии этого репозитория. Так появляется версия на нашем аккаунте, и именно эту версию мы клонируем.
3. Создаём ветку с предлагаемыми изменениями.
4. Производим все изменения только в этой ветке.
5. Отправляем эти изменения на свой аккаунт (push).
6. В окне на GitHub появляется возможность отправить pull request

#


## Заключение
Подводя итоги, можно сказать, что мы познакомились и немного освоили многогранный и бесконечно сложный терминал GIT, SVCod и удаленный сервис gitHub. 
Мы лишь находимся в начале нашего пути........

