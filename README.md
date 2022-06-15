# hse22_project_Ascomycetes1 
# 0. Команда и ссылка на полные данные  
|Участник|Род| Индивидуальная часть|
|----|----|----|
|Абу Аль Лабан	Надя |Ascomycetes	Kazachstania	| https://github.com/nadialaban/hse22_project |
|Зелина	Полина	| Ascomycetes	Lachancea |	https://github.com/LittlePolly/hse22_project_Lachancea |
| Коновалов	Егор	|	Ascomycetes	Ogataea, Alternaria |	https://github.com/konovalowo/hse22_project|
|Крымов	Александр	|Ascomycetes	Bipolaris |	https://github.com/apkrymov/hse22_project|
|Михайлова	Ксения	|Ascomycetes	Trichophyton |	https://github.com/t0pcup/hse22_project|
|Петропавловский	Андрей	|	Ascomycetes	Hanseniaspora, Pneumocystis|	https://github.com/alf3ratz/hse22_project|
|Сесикова	Ксения|	Ascomycetes	Fusarium |	https://github.com/ksenii/BIO_FINAL_PROJECT|
|Чекова	Милена	|	Ascomycetes	Aspergillus |	https://github.com/MilenaChekov/project_Aspergillus|
|Шагалкина	Дарья|	Ascomycetes	Candida, Eremothecium |	https://github.com/adriadar/hse22_project|
|Шилова	Ксения	|	Ascomycetes	Saccharomyces, Naumovozyma |	https://github.com/kseniashilova/hse22_project |    
  
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
### a) Названия кластеров  
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
Таблица с информацией о кластерах выглядит следующим образом:  
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
