# LanguageTool API NLP UK

This is a project to demonstrate NLP API from LanguageTool for Ukrainian language.

Це — проект демонстрації API для обробляння природної мови в LanguageTool для української мови.

Використовує мову [groovy](http://www.groovy-lang.org/), засоби для токенізації та тегування мають скрипти для python3.

## Використання

### Демонстрація можливостей для простих речень:
`groovy src/org/nlp_uk/demo/NlpUkExample.groovy`

* Показує розбиття тексту на речення
* Показує аналіз лексем у тексті
* Показує перевірку граматики та стилю

### Демонстрація аналізу тексту вебсторінки:
`groovy src/org/nlp_uk/demo/NlpUkWebPage.groovy`

* Звантажує текст з архіву статті журналу «Тиждень» і виводить частоту вживання лем та тег частини мови

###Утиліта розбиття тексту:
`groovy TagText.groovy -w -u -i <input_file> -o <output_file>`

* Аналізує текст і записує результат у виходовий файл:
  - розбиває на речення (`-s`) 
  - розбиває на токени (`-w`) (включно з пунктуацією) або на слова (`-w -u`)


###Утиліта лематизації тексту:
`groovy LemmatizeText.groovy -w -u -i <input_file> -o <output_file>`

* Аналізує текст і записує результат у виходовий файл:
  - розбиває на токени і видає на вході леми
  - залишає омоніми

Опція `-f` лишає тільки першу лему (в планах додати інформацію про частоти, щоб лишати тільки найчастотнішу)

###Утиліта аналізу тексту:
`groovy TagText.groovy -i <input_file> -o <output_file>`

* Аналізує текст і записує результат у виходовий файл:
  - розбиває на речення
  - розбиває на лексеми
  - проставляє теги для лексем
  - робить зняття омонімії (наразі алгоритм зняття омонімії досить базовий)

Для тегування лексем використовується версія словника української мови з проекту [ВЕСУМ](https://github.com/brown-uk/dict_uk)

## Ліцензія

Проект LanguageTool API NLP UK розповсюджується за умов ліцензії [GPL версії 3](https://www.gnu.org/licenses/gpl.html)
