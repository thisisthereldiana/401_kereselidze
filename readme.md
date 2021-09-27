Задание 1 

Необходимо обнаружить все известные объекты на изображениях, находящихся в некоторой директории на диске.  

Критерий выполнения: Консольное приложение .NET (Framework или Core) обрабатывает указанную пользователем директорию выдаёт на экран информацию о найденных на изображениях объектах. 

Вариант 1: Программа печатает список найденных на изображении объектов по мере обработки каждого объекта. 
 

Требования к реализации: 

a. Компонент для распознавания должен принимать в качестве входных данных полный путь к директории, в качестве выходных данных выдавать информацию о классах объектов и ограничивающих прямоугольниках для каждого файла с изображением. 

b. Компонент размещен в отдельной библиотеке классов и должен быть переиспользован в других заданиях. 

c. Для распознавания изображений применяются заранее обученные модели из репозитория https://github.com/onnx/models. Пример исходного кода для работы с моделью YOLOv4: https://github.com/BobLd/YOLOv4MLNet. 

d. Распознавание выполняется асинхронно и результаты генерируются по мере обработки данных в директории. 

e. Распознавание нескольких файлов запускается одновременно с целью максимального использования всех ядер всех процессоров в системе. 

f. Компонент позволяет прекратить процесс распознавания и остановить все запущенные потоки. 

g. Для реализации многопоточности и асинхронности применяются: 

Вариант "b" - средства TPL Flow 

 