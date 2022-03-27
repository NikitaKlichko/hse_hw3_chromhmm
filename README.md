# Домашнее задание №3. Разбивка генома на разные типы эпигенетических состояний 

###### Кличко Никита 

*Ссылка на* [google colab](https://colab.research.google.com/drive/1v-smd_Yokef_HCCvBledz4dR8qOCRzhs?usp=sharing) 

## Гистоновые метки с соотвествующими именами файлами
| Метки| Имена файлов | 
--- | ---  
H2AFZ | wgEncodeBroadHistoneDnd41H2azAlnRep1.bam | 
H3K27ac | wgEncodeBroadHistoneDnd41H3k27acAlnRep1.bam | 
H3K27me3 | wgEncodeBroadHistoneDnd41H3k27me3AlnRep1.bam | 
H3K36me3 | wgEncodeBroadHistoneDnd41H3k36me3AlnRep1.bam | 
H3K4me1 | wgEncodeBroadHistoneDnd41H3k04me1AlnRep1.bam | 
H3K4me2 | wgEncodeBroadHistoneDnd41H3k04me2AlnRep1.bam | 
H3K4me3 | wgEncodeBroadHistoneDnd41H3k04me3AlnRep1.bam | 
H3K79me2 | wgEncodeBroadHistoneDnd41H3k79me2AlnRep1.bam | 
H3K9ac | wgEncodeBroadHistoneDnd41H3k09acAlnRep1.bam | 
H3K9me3 | wgEncodeBroadHistoneDnd41H3k09me3AlnRep1.bam | 

[cellmarkfiletable]( https://github.com/NikitaKlichko/hse_hw3_chromhmm/blob/main/cellmarkfiletable.txt) 

## ChromHMM

[Папка с выдачей]( https://github.com/NikitaKlichko/hse_hw3_chromhmm/tree/main/Learn_chromhmm) 

| | | | 
--- | --- | --- 
![](https://github.com/NikitaKlichko/hse_hw3_chromhmm/blob/main/Learn_chromhmm/emissions_10.png) | ![](https://github.com/NikitaKlichko/hse_hw3_chromhmm/blob/main/Learn_chromhmm/DND-41_10_overlap.png)| ![](https://github.com/NikitaKlichko/hse_hw3_chromhmm/blob/main/Learn_chromhmm/transitions_10.png) | 

| | | 
--- | ---
![](https://github.com/NikitaKlichko/hse_hw3_chromhmm/blob/main/Learn_chromhmm/DND-41_10_RefSeqTES_neighborhood.png) | ![](https://github.com/NikitaKlichko/hse_hw3_chromhmm/blob/main/Learn_chromhmm/DND-41_10_RefSeqTSS_neighborhood.png) | 

## Эпигенетические типы 

>Картинка будет в приемлемом качестве, если нажать на нее 

| | | 
--- | --- 
| ![](https://github.com/NikitaKlichko/hse_hw3_chromhmm/blob/main/imgs/1.png) |![](https://github.com/NikitaKlichko/hse_hw3_chromhmm/blob/main/imgs/2.png) | 

>Анализ проведен по скриншотам выше 

| Состояние | Тип | Описание | 
--- | --- | --- 
1 | Heterochromatin | <ul><li>Показывает слабый сигнал на большинстве меток </li><li>Чаще ассоциировано с laminB1lads</li></ul>
2 | Transcribed | <ul><li>Показывает слабый сигнал на большинстве меток </li><li>Чаще ассоциировано с Genome, laminB1lads</li></ul>
3 |Heterochromatin | <ul><li>Более сильный сигнал на метке H3K9me3  </li><li>Чаще ассоциировано с laminB1lads</li></ul>
4 | Transcribed| <ul><li>Более сильный сигнал на метке H3K36me3 </li><li>Чаще ассоциировано с RefSeqTES</li></ul>
5 | Enhancer | <ul><li>Более сильный сигнал на метках H3K36me3, H3K79me2  </li><li>Чаще ассоциировано с RefSeqGene</li></ul>
6 | Transcribed | <ul><li>Cильный сигнал на H3K79me2  </li><li>Чаще ассоциировано с RefSeqGene</li></ul>  
7 | Promoter | <ul><li>Сильный сигнал на метках H3K4me1, H3K79me2  </li><li>Чаще ассоциировано с RefSeqGene, RefSeqTES</li></ul>
8 | Enhancer| <ul><li>По сравнению с другими более сильный сигнал на метке H3K4me1  </li><li>Чаще всего ассоциировано с laminB1lads</li></ul> 
9 | Repressed| <ul><li>Сильный сигнал на метках H3K4me1, H3K27ac </li><li>Ассоциировано с laminB1lads </li><li>Не попадает на ген</li></ul> 
10 | Enhancer | <ul><li>Cильный сигнал на метках H3K9ac, H3K4me2, H3K4me3  </li><li>Чаще ассоциировано с CpGIsland, RefSeqExon, RefSeqTSS, RefSeqTSSK2b</li></ul>  


**Код см в колабе** 

## Бонус 

![](https://github.com/NikitaKlichko/hse_hw3_chromhmm/blob/main/imgs/name.png)   

[файл](https://github.com/NikitaKlichko/hse_hw3_chromhmm/blob/main/new_dense.bed) 




