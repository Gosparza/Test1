Техническое задание №1 (ТЗ1)

Пишем скрипт на bash

Легенда задания

Вам нужно написать скрипт на bash, который на вход принимает два параметра - две директории (входная директория и выходная директория). Во входной директории могут находиться как файлы, так и вложенные директории (внутри которых тоже могут быть как файлы, так и папки) - уровень вложенности может быть любой. Задача скрипта - "обойти" входную директорию и скопировать все файлы из нее (и из всех сложенных директорий) в выходную директорию - но уже без иерархии, а просто все файлы - внутри выходной директории.

Пример:

Входная директория = /home/input_dir; Выходная директория = /home/output_dir.

/home/output_dir изначально пустая.

Структура /home/input_dir:

input_dir

	a.txt
 
	dir2
 
		b.txt
	dir3
 
		c.txt
  
Тогда после работы вашего скрипта структура /home/output_dir должна быть следующая:

output_dir

	a.txt
 
	b.txt
 
	c.txt
 
Обратите внимание: в разных поддиректориях входной директории могут быть файлы с одинаковым названием. В момент копирования в выходную аудиторию необходимо такие ситуации каким-либо образом разрешить без потери файлов и содержания файлов (как именно - на ваше усмотрение).
Требования и критерии оценки

За задание вы можете получить максимум 10 баллов.

Семинарист при проверке может выставить за какой-либо пункт частичный балл, если требования пункта выполнены не полностью.

1 балл Скрипт запускается и принимает два параметра

1 балл Реализовано получение списка файлов, находящихся непосредственно во входной директории (не во вложенных в нее директориях)

1 балл Реализовано получение списка директорий, находящихся во входной директории

3 балла Реализовано получение списка всех файлов, вложенных во входную директорию

1 балла Реализовано копирование всех файлов, вложенных во входную директорию в выходную директорию

3 балла Решена проблема с файлами, имеющими одинаковое название

Как запускать скрипт:

	Перед запуском скрипта нужно добавить в PATH путь до папки со скриптом командой:
 
	PATH=$PATH:путь до папки со скриптом (команда для iOS)
 
	Затем команда для разрешения:
 
	chmod +x путь до самого файла скрипта
 
Скрипт вызывается командой tz1 и принимает на вход два аргумента: входную и выходную дирректории
