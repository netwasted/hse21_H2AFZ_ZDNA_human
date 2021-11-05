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

Построение гистограммы и другой анализ производился в Google Colab: https://colab.research.google.com/drive/1bwpJatLXOj8ROi9vDaKIjQyLsQ_ZB05k?usp=sharing

Выяснилось, что число пиков в первом эксперименте равно 142121, а во втором - 125410.

Гистограммы:

![Screenshot (1397)](https://user-images.githubusercontent.com/60008375/140524783-5369de7b-e6fa-4dbd-be96-39787712ff37.png)

![Screenshot (1398)](https://user-images.githubusercontent.com/60008375/140524807-1fd22988-db9a-4d19-9d7d-1abf3fe6e39c.png)
