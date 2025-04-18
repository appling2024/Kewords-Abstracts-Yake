# Kewords Abstracts Yake + RRuTermExtract
This repository contains code that extracts key words from abstracts and csv file with extracted keywords from our corpus of articles

 # Авторы:
 Александра Мурашко, Полина Павлухина, Елизавета Логачева, Алёна Берлин. 

# База данных
Мы извлекли ключевые слова из 392 аннотаций статей, написанных в 2013-2024 годах, которые хранятся в архиве IMS2013-2024-20250318T190010Z-001. zip. Аннотации, которые мы обрабатывали, встречались как на русском так и на английском языках. 

# Результат извлечения хранится в таблице — keywords_abstracts.csv
Таблица представляет собой файл csv, где первый элемент в строке - имя файла, из которого извлекались КС, второй элемент — КС на русском (для аннотаций на русском), третий элемент — КС на английском (для аннотаций на английском). Так для каждого документа есть КС на русском ИЛИ на английском. 

# Алгоритм извлечения: 
Для извлечения КС был выбран Yake, который по мнению большинства авторов работает лучше других алгоритмов для этой задачи. Позднее был добавлен RuTermExtrcat только для русских аннотаций. Итеративный проход по архиву собрал документы, которые заканчиваются на Abstract_rus или Abstract_eng, определял язык и, в соответствии с языком аннотации, извлекал КС. Из каждого документа было извлечено не более 10 ключевых слов. Мы учитывали не только отдельные слова, но и биграммы. Однако, для английского языка Yake чаще извлекал униграммы. Наш код можно найти в этом репозитории под именем: КНВ.ipynb
