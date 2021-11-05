# Anastasia Kolchina 191
## HSE Bioinformatics Elective 2021 - Homework №1

## hse21_H2AFZ_ZDNA_human

### Анализ пиков гистоновой метки

Для исследования были выбраны следующие гистоновые метки:

* [ENCFF271JBK](https://www.encodeproject.org/files/ENCFF271JBK/)
* [ENCFF534KJU](https://www.encodeproject.org/files/ENCFF534KJU/)

Типа human hg19, тип клеток - brain (astrocyte).

С помощью команд:

* ```zcat ENCFF271JBK.bed.gz | cut -f1-5 > H2AFZ_brain.ENCFF271JBK.hg19.bed```
* ```zcat ENCFF534KJU.bed.gz | cut -f1-5 > H2AFZ_brain.ENCFF534KJU.hg19.bed```

Оставляем первые 5 столбцов файлов и распаковываем их.
