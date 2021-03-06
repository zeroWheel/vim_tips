Когда я закрываю VIM, теряю все вкладки и буфферы. Устал ходить по файлам и снова открывать нужные
файлы. Хорошо, что у VIM есть для этого решение - mks (что-то на космос потянуло).

Итак, сессии в VIM.

Комманда mksession или mks:

```
:mks filename.vim
```

запоминает текущую директорию работы, табы, буфферы, сплиты, set настройки.

Таким образом мы сохраняем "холст" для последующей работы.

Открывает сессию

```
vim -S filepath/filename.vim
```

и получаем "холст", который сохранили.

Если нужно открыть сессию внутри VIM используем

```
source filepath/filename.vim
```

Если нужно править сохраненную сессию, то сначала мы ее открываем, добавляем нужные
настройки и вызываем сохранение с восклицательным знаком:

```
:mks! filepath/sessionname.vim
```

Подробнее:

Полезно, когда хочешь продолжить с того же места, на котором остановился.
В любом другом редакторе (VSCode, JetBrains Products) изначально открытые вкладки проекта сохраняются по закрытию приложения. Удобно.

И всё-таки не всегда нужно запоминать последние открытые файлы. Мы не можем создать себе подготовить
набор открытых файлов для правки фичи - добавление валюты, например. Или мы не можем создать несколько
таких раскладок в одном моменте ( подробнее об этом в посте "Табы и буфферы как Млечный путь и звёзды" ).

В вышеуказанных редакторах и IDE это решается рабочими областями (work spaces) куда можно добавить файлы, папки и
всё что хочешь.

В VIM нам нужно меньше времени на это: открыли то, что нужно и сохранили в файл. Если посмотреть в конечный файл сессии, то
там не будет ничего магического только настройки и пути, отмеченные сущностями VIM'а.
