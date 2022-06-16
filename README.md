# hse22_project_Ascomycetes1 
# 0. Команда и ссылка на полные данные  
|Участник|Род| Индивидуальная часть|
|----|----|----|
|Абу Аль Лабан	Надя | Kazachstania	| https://github.com/nadialaban/hse22_project |
|Зелина	Полина	| Lachancea |	https://github.com/LittlePolly/hse22_project_Lachancea |
| Коновалов	Егор	|	Ogataea, Alternaria |	https://github.com/konovalowo/hse22_project|
|Крымов	Александр	| Bipolaris |	https://github.com/apkrymov/hse22_project|
|Михайлова	Ксения	| Trichophyton |	https://github.com/t0pcup/hse22_project|
|Петропавловский	Андрей	|	Hanseniaspora, Pneumocystis|	https://github.com/alf3ratz/hse22_project|
|Сесикова	Ксения|	Fusarium |	https://github.com/ksenii/BIO_FINAL_PROJECT|
|Чекова	Милена	|	Aspergillus |	https://github.com/MilenaChekov/project_Aspergillus|
|Шагалкина	Дарья| Candida, Eremothecium |	https://github.com/adriadar/hse22_project|
|Шилова	Ксения	| Saccharomyces, Naumovozyma |	https://github.com/kseniashilova/hse22_project |    
  
Код находится в [Google colab](https://colab.research.google.com/drive/1myWxls72ZCpo1IuQsPOtPUtDFzogMF-M?usp=sharing)  
Все файлы, использовавшиесяв процессе работы, находятся на [гугл диске](https://drive.google.com/drive/folders/1r5IfjANJg3Nt-GnA2TBUgyQXWJoYUtfy?usp=sharing)    
# 1. Создание ортологичных кластеров внутри таксона
Для кластеризации были использованы следующие файлы (10 файлов):  
* Абу Аль Лабан Надя - Kazachstania_barnettii_protein.faa  
* Зелина Полина - protein1.faa  
* Коновалов Егор - protein_op.faa  
* Крымов Александр - Bipolaris_oryzae_ATCC_44560.faa  
* Михайлова Ксения - Trichophyton_interdigitale.faa
* Петропавловский Андрей - GCA_001749795.1.protein.faa  
* Сесикова Ксения - GCA_000303195.2_FP7_protein.faa  
* Чекова Милена - GCF_000002655.1_ASM265v1_protein.faa  
* Шагалкина Дарья - GCF_000235365.1_protein.faa  
* Шилова Ксения - GCA_000292725.1.faa    

После того, как ```proteinortho5``` отработала (результат в [файле](https://github.com/kseniashilova/hse22_project_Ascomycetes1/blob/main/clusters/myproject.proteinortho)) необходимо совместить кластеры по 50-ти геномам в один файл.  
Файлы участников команды, полученные после команды ```intersectBed``` предварительно были обработаны (код для обработки в [другом гугл колабе](https://colab.research.google.com/drive/1TMzOUMdtznN3huHGIf2hfPHIz9FUUzGr?usp=sharing)).  
Затем были найдены кластеры, где участвуют по крайней мере 25 (половина) видов.  
* **Полностью таблицу можно увидеть в [.txt файле](https://drive.google.com/file/d/171tNxe6vZkWm6lJkNMI3cg0HvrGfJhFb/view?usp=sharing) и в [.csv файле](https://drive.google.com/file/d/1--TKCONqmjJA0y3wkSs7H5779GAFDrik/view?usp=sharing)**.   
# 2. Статистика по кластерам, где участвуют по крайней мере 25 (половина) видов  
### Информация о геномах (собрана из индивидуальных частей)  
|Номер|Название| Длина генома|GC% | Доля аннотированных генов | Кол-во Z-DNA | Кол-во генов, которые имели Z-DNA в промотере |
|--|--------|--------------------|------------|-----------------------|------------------|---------------------------------------------------|
|1. |Kazachstania africana CBS 2517|11,130,140|36,3068|0.710668	|3622||
|2. |Kazachstania naganishii CBS 8797|10,845,821|45,8879|0.740008|19026||
|3. |Kazachstania barnettii|12,616,033|33,7|0.644475|4443||
|4. |Kazachstania saulgeensis|12,935,755|32,2|0.646064|6046||
|5. |Kazachstania exigua|13,507,013|33,3|0.619264|5467||
|6. |Lachancea thermotolerans CBS 6340|10392862|47,2838	|0.73|42003||
|7. |Lachancea fermentati|10264457|42,582|0.77|22475||
|8. |Lachancea lanzarotensis|11092131|44,3|0.68|13887||
|9. |Lachancea mirantina|10117267|45,1112|0.74|22109||
|10. |Lachancea quebecensis|10229370|46,7|0.74|36547||
|11. |Alternaria atra|78177382|39,6|0.31|132920||
|12. |Alternaria rosae|84993594|33,8|0.38|139812||
|13. |Ogataea angusta|30596185|49,4|0.41|28353||
|14. |Ogataea haglerorum|30377204|49,3|0.39|28766||
|15. |Ogataea polymorpha|37588682|47,9|0.51|21991||
|16. |Bipolaris maydis ATCC 48331|32 929 167|50,7|0.60|136 035||
|17. |Bipolaris oryzae ATCC 44560|31 362 097|50,5|0.56|129 409||
|18. |Bipolaris sorokiniana ND90Pr|34 409 167|49,8|0.60|127 672||
|19. |Bipolaris victoriae FI3|32 829 575|50,1|0.56|129 053||
|20. |Bipolaris zeicola 26-R-13|31 267 936|	50,8|0.58|125 028||
|21. |Trichophyton verrucosum	|22540967|48.2|0.52|29315||
|22. |Trichophyton rubrum|22530013|48.3|0.77|28033||
|23. |Trichophyton interdigitale|22044533|48.7|0.51|29838||
|24. |Trichophyton equinum|24158205|49,8|0.49|30115||
|25. |Trichophyton tonsurans|22988586|48.1|0.52|29564||
|26. |Hanseniaspora opuntiae|8831957| 34,7| 0.727557|1552||
|27. |Hanseniaspora osmophila|11458415|36,7|0.673249|10130||
|28. |Hanseniaspora valbyensis NRRL Y-1626|11464036|22,6|0.617387|994||
|29. |Pneumocystis canis|7939452|26,3|0.594793|1396||
|30. |Pneumocystis oryctolagi|7639465|27,8|0.582478|5548||
|31. | Fusarium musae |44016361|47.2|0.43|64408||
|32. | Fusarium poae |44001690|46.6|0.44|52940||
|33.|Fusarium venenatum|38660641|47.6|0.55|55322||
|34. |Fusarium pseudograminearum CS3096|47.7|0.48|56515||
|35. |Fusarium verticillioides 7600|36567790|47.7|54660||
|36. |Aspergillus fumigatus|29384958|49,8105|0.48|59749||
|37. |Aspergillus flavus|36995582|48,0323|0.5|61829||
|38. |Aspergillus luchuensis IFO|37287723|48,876|0.47|83580||
|39. |Aspergillus chevalieri M1|29697343|49,2293|0.48|63852||
|40. |Aspergillus puulaauensis MK2|34318862|49,754|0.57|79369||
|41. | Candida dubliniensis | 14618422 || 0.62 | 1064
|42. | Eremothecium gossypii | 9119312||0.8 | 5121
|43. | Candida albicans | 14282666||0.63 | 1100
|44. | Eremothecium cymbalariae| 9669424||0.73| 1127||
|45. | Candida orthopsilosis|12659401||0.67| 1134|
|46. ||||||
|47. ||||||
|48. ||||||
|49. ||||||
|50. ||||||



### a) Названия кластеров  
Таблицы с названиями для кластеров можно увидеть в [файле](https://github.com/kseniashilova/hse22_project_Ascomycetes1/blob/main/clusters/features2.csv)  
Функции были взяты из поля ```product``` в файлах с аннотациями.  
### b) Количество генов   
Гистограмма распределения количества генов в кластерах:  
![](https://github.com/kseniashilova/hse22_project_Ascomycetes1/blob/main/pic/genes.png)
### c) Количество видов  
Гистограмма распределения количества видов в кластерах:  
![](https://github.com/kseniashilova/hse22_project_Ascomycetes1/blob/main/pic/species.png)
### d) Количество генов, у которых есть z-dna в промотере  
Гистограмма распределения количества генов с предсказанной Z-DNA в районе промотера:  
![](https://github.com/kseniashilova/hse22_project_Ascomycetes1/blob/main/pic/zdna_in_promoters.png)
### e) Максимальный ZH-Score  
Гистограмма распределения максимальных ZHUNT Scores по всем кластерам:  
![](https://github.com/kseniashilova/hse22_project_Ascomycetes1/blob/main/pic/max_zh.png)  
### f) Средний ZH-Score  
Гистограмма распределения средних ZHUNT Scores по всем кластерам:  
![](https://github.com/kseniashilova/hse22_project_Ascomycetes1/blob/main/pic/mean_zh.png)  

# 3. Выбор кластеров с наибольшим количеством генов с консервативной Z-DNA в промотере  
  Все кластеры были отсортированы по количеству генов в них с Z-DNA в районе промотера. В случае одинакового количества таких генов (второй уровень сортировки) - по среднему ZHunt Score среди генов кластера.  
[Таблица](https://github.com/kseniashilova/hse22_project_Ascomycetes1/blob/main/tables_of_50_genomes/clusters.txt) с информацией о кластерах выглядит следующим образом:  
Количество видов которые участвуют в создании кластера, Количество генов, Сколько из видов имеют предсказанную ZDNA в промотере, Cредний Zhunt Score, Максимальный Zhunt Score в кластере.  
Затем в таблице находятся 50 столбцов, где написан белок из файлов myproject.proteinortho, Затем 0 или 1 (0 - нет Z-DNA в промотере, 1 - есть) и если было 1, то описание этой Z-DNA. 
  ![](https://github.com/kseniashilova/hse22_project_Ascomycetes1/blob/main/pic/table%20example.PNG)    
# 4. Тепловая карта  
Тепловая карта, где по строкам располагаются геномы, а по столбцам выбранные кластеры.  
Белый цвет ячейки означает, что в данном гене нет предсказанной Z-DNA в промотере.  
Серый цвет ячейки означает, что этот геном не представлен в кластере.   
![](https://github.com/kseniashilova/hse22_project_Ascomycetes1/blob/main/pic/heat_map.jpg)    
# 5. Названия (наиболее частые функции) для выбранных 10-ти кластеров
|cluster| function |
|--|--|
|0|    Exosome complex component, Exosome exonuclease subunit|
|1|   Nucleolar protein, rRNA processing protein, alcohol dehydrogenase, ion of 18S rRNA and assembly of small ribosoma|
|2|    transcription elongation factor, RNA polymerase II elongation factor|
|3|                         (pre-) mRNA splicing protein|
|4|               small nucleolar RNA-associated protein|
|5|              Lysophosphatidylcholine acyltransferase|
|6|                    mRNA-capping enzyme subunit alpha|
|7|                                  histone deacetylase|
|8|           Ribosome-releasing factor 2, mitochondrial|
|9|                  putative copper-transporting ATPase|    
# 6. Выбор нескольких кластеров и дополнительная информация по ним
### a) Визуализация с помощью Dna Features Viewer  
![](https://github.com/kseniashilova/hse22_project_Ascomycetes1/blob/main/pic/clust2_vis.png)  
![](https://github.com/kseniashilova/hse22_project_Ascomycetes1/blob/main/pic/clust5_vis.png)  
![](https://github.com/kseniashilova/hse22_project_Ascomycetes1/blob/main/pic/clust7_vis.png)
### b) Нуклеотидное выравнивание с Z-DNA  
Файлы: [clust2](https://github.com/kseniashilova/hse22_project_Ascomycetes1/blob/main/clusters/clusters/clust2_nucleotide_align_ZDNA.fas),  
[clust5](https://github.com/kseniashilova/hse22_project_Ascomycetes1/blob/main/clusters/clusters/clust5_nucleotide_align_ZDNA.fas),  
[clust7](https://github.com/kseniashilova/hse22_project_Ascomycetes1/blob/main/clusters/clusters/clust7_nucleotide_align_ZDNA.fas)  
### c) Аминокислотное выравнивание  
Файлы: [clust2](https://github.com/kseniashilova/hse22_project_Ascomycetes1/blob/main/clusters/clusters/clust2_aminoacid_align.fas),  
[clust5](https://github.com/kseniashilova/hse22_project_Ascomycetes1/blob/main/clusters/clusters/clust5_aminoacid_align.fas),  
[clust7](https://github.com/kseniashilova/hse22_project_Ascomycetes1/blob/main/clusters/clusters/clust7_aminoacid_align.fas)    
# Выводы  

1) Было найдены свыше 10 тысяч кластеров, объединивших хотя бы половину (25) геномов с наличием z-днк

2) Из них были отобраны 10 с учетом наибольшего покрытия видов и zh-score

3) Исходя из нескольких факторов (функций, скора proteinortho, zh-score), выбрали 3 кластера и провели их более подробный анализ

4) Подводя итоги, нам удалось найти консервативную z-dna в генах, кодирующих значимые белки для данных родственных видов

# Бонус. Анализ квадруплексов  
* Количество генов   
Гистограмма распределения количества генов в кластерах:  
![](https://github.com/kseniashilova/hse22_project_Ascomycetes1/blob/main/quadruplex/pic/genes.png)
* Количество видов  
Гистограмма распределения количества видов в кластерах:  
![](https://github.com/kseniashilova/hse22_project_Ascomycetes1/blob/main/quadruplex/pic/scecies.png)
* Количество генов, у которых есть квадруплекс в промотере  
Гистограмма распределения количества генов с предсказанным квадруплексом в районе промотера:  
![](https://github.com/kseniashilova/hse22_project_Ascomycetes1/blob/main/quadruplex/pic/quads_in_promoter.png)
* Максимальный Quadruplex Score  
Гистограмма распределения максимальных Scores по всем кластерам:  
![](https://github.com/kseniashilova/hse22_project_Ascomycetes1/blob/main/quadruplex/pic/max.png)  
* Средний Quadruplex Score  
![](https://github.com/kseniashilova/hse22_project_Ascomycetes1/blob/main/quadruplex/pic/mean.png)    
# Выбор кластеров
Кластеры выбраны с наибольшем количеством генов, у которых есть квадруплекс в промотере. Второй уровень сортировки по mean score.  
Кластеры можно посмотреть [здесь в файле](https://github.com/kseniashilova/hse22_project_Ascomycetes1/blob/main/quadruplex/clusters.txt).   
# Тепловая карта. Квадруплексы
Тепловая карта, где по строкам располагаются геномы, а по столбцам выбранные кластеры.  
Белый цвет ячейки означает, что в данном гене нет предсказанного квадруплекса.  
Серый цвет ячейки означает, что этот геном не представлен в кластере.   
![](https://github.com/kseniashilova/hse22_project_Ascomycetes1/blob/main/quadruplex/pic/heatmap.png)   
