# urfu-fp-intro-20

Спецкурс "Введение в функциональное программирование" в УрФУ в 2020.

# Подготовка среды

## Установите Haskell

### MacOS

https://www.haskell.org/platform/mac.html или

```
brew install ghc cabal-install
```
Также добавьте `.cabal/bin` в `PATH`:
```
export PATH=$PATH:~/.cabal/bin
```
### Linux

https://www.haskell.org/downloads/linux/

### Windows

https://www.haskell.org/platform/windows.html.

## Проверьте, что всё работает

Проверьте, что установлен компилятор `ghc >= 8.2`

```
ghc --version
The Glorious Glasgow Haskell Compilation System, version 8.8.1
```

Чтобы убедиться, что всё установлено верно, запустите тест:

```
cd urfu-fp-intro-20
cabal update
cabal new-run spec -- --match "Lecture00"
```

Вы должны увидеть, что "всё работает":

![setup is ok](./assets/SetUpIsDone.jpg)

По любым вопросам можно обратиться к официальной [документации](https://www.haskell.org/documentation/) или к преподавателям в чате [https://teleg.run/urfu_fp_intro_20_chat](https://teleg.run/urfu_fp_intro_20_chat).

## Среда разработки

Курс рассчитан на использование редактора с подсветкой кода и терминалом.

При желании можно настроить среду разработки для подсветки типов в редакторе. На это потребуется время и не факт, что все получится, поэтому это опционально.

Для Haskell есть интеграции с разными редакторами, но большинство использует [GHC IDE](https://github.com/digital-asset/ghcide). Пока нет скриптов для установки, поэтому нужно собирать ее вручную, что тоже описано в доке.

Важно — перед установкой выполните команду `cabal update`, чтобы подгрузить информацию о доступных пакетах.
После успешной установки `ghcide` нужно поставить [плагин в VS Code](https://marketplace.visualstudio.com/items?itemName=DigitalAssetHoldingsLLC.ghcide) или нужный редактор.

Про IntelliJ IDEA: для IDE от Jetbrains есть плагин для Хаскеля, но он рассчитан на работу со Stack — другим менеджером пакетов, обратите внимание.

# Как сдавать задачи

Для сдачи задач вам потребуются базовые навыки работы с `git`. 
Если до этого вы с ним не работали, можете изучить материалы из [kontur-courses/git](https://github.com/kontur-courses/git).

Создайте отдельную ветку, закоммитив изменения:

```
git checkout -b lecture01
git add src/Lecture01.hs
git commit -m "add lecture01"
```

Далее, вам необходимо форкнуть этот репозиторий и запушить в него свои изменения:

```
git remote add fork git@github.com:<ваш_юзернейм>/urfu-fp-intro-20.git 
git push fork lecture01
```

После этого создайте pull request. Поздравляю, вы великолепны. 👌 

# Расписание

Неделя | Дата   | Тема 
-------|--------|------
1      | 27 фев | Введение в Haskell
2      | 05 мар | Списки и строки
3      | 12 мар | Лямбда-исчисление (untyped/stlc)
4      | 19 мар | ADTs
5      | 26 мар | Ленивость
6      | 02 апр | Параметрический полиморфизм
7      | 09 апр | Структуры данных
8      | 16 апр | Классы типов
9      | 23 апр | Монады IO и Random
10     | 30 апр | Остальные монады
11     | 07 мая | Трансформеры
12     | 14 мая | Архитектура функциональных приложений
13     | 21 мая | 🤔
14     | 28 мая | 🤔

# Спонсоры

Курс проводится при поддержке компании [Typeable](http://typeable.io) и компании [СКБ Контур](https://kontur.ru/).
