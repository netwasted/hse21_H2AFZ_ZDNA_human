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

После анализа гистограмм было принято решение выкинуть пики длиной больше 1500.

После фильтрации получили следующие гистограммы:

![Screenshot (1399)](https://user-images.githubusercontent.com/60008375/140528014-af7bdcab-bb99-425e-877d-f9ad3ef86fda.png)

![Screenshot (1400)](https://user-images.githubusercontent.com/60008375/140528039-5a6be096-3035-4e63-abf2-e48abb0b8ce8.png)

Число пиков теперь составляет 141117 и 123301 для первого и второго экспериментов соответственно.

На основе кода на R отсюда: https://github.com/vanya-antonov/hse21_H3K4me3_ZDNA_human/blob/main/src/chip_seeker.R

Строим графики Pie-Chart расположения пиков в аннотированных генах

![chip_seeker ENCFF271JBK_filtered plotAnnoPie](https://user-images.githubusercontent.com/60008375/140614265-1f98797e-1173-4d55-9f6a-9468ee1333fe.png)

![chip_seeker ENCFF534KJU_filtered plotAnnoPie](https://user-images.githubusercontent.com/60008375/140614269-d7c89f46-0503-4a54-9ae6-d0e47dd7f055.png)

Визуализация отфильтрованных пиков и их пересечения в геномном браузере UCSC: https://genome.ucsc.edu/cgi-bin/hgTracks?db=hg19&lastVirtModeType=default&lastVirtModeExtraState=&virtModeType=default&virtMode=0&nonVirtPosition=&position=chr1%3A713777%2D714105&hgsid=1207219651_cbSwjRnpQXKQr8zCQfkZEb9iFmVg

### Анализ участков вторичной структуры ДНК

В качестве вторичной структуры ДНК была выбрана Z-DNA, разметка DeepZ.bed.

Гистограмма распределения длин участков вторичной структуры ДНК:

![Screenshot (1411)](https://user-images.githubusercontent.com/60008375/140619175-1b48c0ab-01aa-4171-ada1-b09180c1d65d.png)

Количество пиков: 19394.

График Pie-Chart расположения участков вторичной структуры ДНК относительно аннотированных генов:

### Анализ пересечений гистоновой метки и структуры ДНК
