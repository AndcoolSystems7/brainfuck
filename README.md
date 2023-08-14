# Python BrainFuck interpreter

Интерпретатор языка BrainFuck, написанный на языке Python

## Использование
Для запуска вам не нужны сторонние модули, что бы запустить .bf скрипт просто выполните в консоли следующую команду:
> python interpreter.py main.bf

После названия скрипта интерпретатора идёт название файла со скриптом brainfuck.
Поддерживаемые расширения файлов: 
- .bf 
- .b

## Параметры интерпретатора
После первого запуска скрипта в папке с интерпретатором создастся файл **params.json**, открыв его Вы сможете найти в нём следующие параметры:

|Параметр        |Значение по умолчанию          |Возможные значения | Описание|
|----------------|-------------------------------|-------------------|---------|
|`memorySize`    |30.000            			 |Любое числовое значение. |Количество ячеек памяти, выделенных под программу    |
|`memoryManagement` |OFF            |`OFF`/`AUTO`/`JUMP` | `OFF` - строгое выделение памяти, при вводе некорректного индекса ячейки вызывает ошибку.<br> `AUTO` - 1 ячейка по умолчанию, при использовании оператора `>` при несуществующем индексе ячейки памяти добавляется новая со значением, равным 0.<br> `JUMP` - При выборе ячейки памяти менее 0 или более выделенного размера происходит перенос выбора ячейки с нулевой на последнюю, с последней на нулевую.