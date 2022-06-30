# Задача "Исследование JVM через VisualVM"
## Вывод консоли:
_**Строки, выводимые в консоли пронумерованы, на изображениях (Metaspace.jpg и Heap.jpg) отмечены номера событий на графиках.**_  
_**Ниже под ростом размера Metaspace и Heap подразумевается рост используемого пространства области памяти**_
_**ввиду записи новых данных (синий график в VisualVM),**_
_**также параллельно происходит увеличение выделенного под запись пространства (желтый график в VisualVM).**_
    
12:42:06: Executing ':JvmExperience.main()'...

*>* Task :compileJava  
*>* Task :processResources NO-SOURCE  
*>* Task :classes

*>* Task :JvmExperience.main()  
*>* Please open 'ru.netology.JvmExperience' in VisualVm  
_См. график области памяти Metaspace (Metaspace.jpg)_
1. 12:42:58.919646300: loading io.vertx  
_Размер Metaspace начинает "расти" - в Metaspace записываются данные о классах пакета io.vertx_
1. 12:42:59.847052500: loaded 529 classes  
_Рост Metaspace останавливается - в Metaspace записаны все данные о классах пакета io.vertx_
1. 12:43:02.862730300: loading io.netty  
_Размер Metaspace начинает "расти" - в Metaspace записываются данные о классах пакета io.netty_
1. 12:43:04.076217200: loaded 2117 classes  
_Рост Metaspace останавливается - в Metaspace записаны все данные о классах пакета io.netty_
1. 12:43:07.076253600: loading org.springframework  
_Размер Metaspace начинает "расти" - в Metaspace записываются данные о классах пакета org.springframework_
1. 12:43:07.482508400: loaded 869 classes  
_Рост Metaspace останавливается - в Metaspace записаны все данные о классах пакета org.springframework_
1. 12:43:10.482980600: now see heap  
_Переходим к куче (Heap.jpg)_
1. 12:43:10.482980600: creating 5000000 objects  
_Размер Heap начинает "расти" - В Heap создаются объекты класса SimpleObject_
1. 12:43:11.147452800: created  
_Рост Heap останавливается - В Heap создано 5_000_000 объектов класса SimpleObject_
1. 12:43:14.149112500: creating 5000000 objects  
_Размер Heap начинает "расти" - В Heap создаются объекты класса SimpleObject_
1. 12:43:14.740493200: created  
_Рост Heap останавливается - В Heap создано 5_000_000 объектов класса SimpleObject_
1. 12:43:17.837689900: creating 5000000 objects  
_Размер Heap начинает "расти" - В Heap создаются объекты класса SimpleObject_
1. 12:43:18.710308900: created  
_Рост Heap останавливается - В Heap создано 5_000_000 объектов класса SimpleObject_

BUILD SUCCESSFUL in 1m 14s  
2 actionable tasks: 2 executed  
12:43:22: Execution finished ':JvmExperience.main()'.