# hse22_project_Ascomycetes1 
Код находится в [Google colab](https://colab.research.google.com/drive/1myWxls72ZCpo1IuQsPOtPUtDFzogMF-M?usp=sharing)  
## 1. Создание ортологичных кластеров внутри таксона
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

После того, как ```proteinortho5``` отработала (результат в [файле](https://github.com/kseniashilova/hse22_project_Ascomycetes1/blob/main/clusters/myproject.proteinortho)) необходимо совместить кластеры по 50-ти геномам в один файл ([файл с кластерами для 50-ти геномов]()).  
Файлы участников команды, полученные после команды ```intersectBed``` предварительно были обработаны (код для обработки в ![другом гугл колабе](https://colab.research.google.com/drive/1TMzOUMdtznN3huHGIf2hfPHIz9FUUzGr?usp=sharing)).  
Затем были найдены кластеры, где участвуют по крайней мере 25 (половина) видов. Полностью таблицу можно увидеть в [файле]().   
# 2. Статистика по кластерам  
### a) Названия кластеров  
### b) Количество генов  
### c) Количество родов  
### d) Количество генов, у которых есть z-dna в промотере  
### e) Максимальный ZH-Score
### f) Средний ZH-Score
