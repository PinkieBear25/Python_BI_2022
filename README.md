# Python_BI_2022
#Homework_2 \
Код помогает проанализировать содержимое  файла формата fastq и отфильтровать содержащиеся в нем риды по GC-составу, качеству или длине. \
В качестве аргументов код принимает: \
*input_fastq* - путь к fastq-файлу; \
*output_file_prefix*- католог, в котором пользователь планирует обнаружить выходные файлы; \
*gc_bounds* - параметр, которым задаются границы фильтрации GC-состава (в процентах), по-умолчанию равен (0, 100), границы включаются. При передаче в аргумент одного числа считается, что это верхняя граница; \
*length_bounds* - параметр, которым задаются границы фильтрации длины рида, по-умолчанию равен (0, 2^32), границы включаются. При передаче в аргумент одного числа считается, что это верхняя граница; \
*quality_threshold* - пороговое значение для фильтрации среднего качества рида, по-умолчанию равен 0. Риды со средним качеством по всем нуклеотидам ниже порогового не учитываются; \
*save_filtered* - устаналивает, нужен ли файл с неподошедшими ридами. Принимает значения True или False. \

Так как программа фильтрует риды только по одному значению единовременно, в результате ее исполнения пользователь получает 6 файлов - три файла с фильтрацией по GC-составу, качеству и длине, а также 3 файла с неподошедшими ридами (информация в этих файлах будет представлена только в том случае, если save_filtered = True)

P.S. понятия не имею, зачем кому-то может понадобиться плодить столько сущностей, но это мое костыльное решение. Подскажите, пожалуйста, как можно было сделать лучше?
