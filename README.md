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
1 | Heterochromatin | -Показывает слабый сигнал на большинстве меток  -Чаще ассоциировано с laminB1lads
2 | Transcribed | -Показывает слабый сигнал на большинстве меток  -Чаще ассоциировано с Genome, laminB1lads 
3 |Heterochromatin | -Более сильный сигнал на метке H3K9me3  -Чаще ассоциировано с laminB1lads
4 | Transcribed| -Более сильный сигнал на метке H3K36me3 
-Чаще ассоциировано с RefSeqTES
5 | Enhancer | -Более сильный сигнал на метках H3K36me3, H3K79me2  -Чаще ассоциировано с RefSeqGene
6 | Transcribed | -Cильный сигнал на H3K79me2  -Чаще ассоциировано с RefSeqGene  
7 | Promoter | -Сильный сигнал на метках H3K4me1, H3K79me2  -Чаще ассоциировано с RefSeqGene, RefSeqTES
8 | Enhancer| -По сравнению с другими более сильный сигнал на метке H3K4me1  -Чаще всего ассоциировано с laminB1lads 
9 | Repressed| -Сильный сигнал на метках H3K4me1, H3K27ac -Ассоциировано с laminB1lads -Не попадает на ген 
10 | Enhancer | -Cильный сигнал на метках H3K9ac, H3K4me2, H3K4me3  -Чаще ассоциировано с CpGIsland, RefSeqExon, RefSeqTSS, RefSeqTSSK2b  



