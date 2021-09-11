# Счетчики покрытия

JaCoCo использует набор различных счетчиков для расчета показателей покрытия. Все эти счетчики выводятся из информации, содержащейся в файлах классов Java, которые в основном представляют собой инструкции байтового кода Java и отладочную информацию, необязательно встроенную в файлы классов. 

## Instructions (Инструкции)

Наименьшая единица отсчета JaCoCo - это инструкции с одним байтовым кодом Java. Покрытие инструкций предоставляет информацию об объеме кода, который был выполнен или пропущен. Эта метрика полностью независима от исходного форматирования и всегда доступна, даже при отсутствии отладочной информации в файлах классов.

## Branches (Ветви)

JaCoCo вычисляет охват ветвей для if и switch конструкций. Эта метрика подсчитывает общее количество таких ветвей в методе и определяет количество выполненных или пропущенных ветвей. Покрытие веток всегда доступно, даже при отсутствии отладочной информации в файлах классов. Обработка исключений не считается ветвями в контексте этого определения счетчика.

## Lines (Линии)

Для всех файлов классов, которые были скомпилированы с отладочной информацией, можно рассчитать информацию о покрытии для отдельных строк. Исходная строка считается выполненной, если была выполнена хотя бы одна инструкция, назначенная этой строке.

## Complexity (Сложность)

JaCoCo также вычисляет цикломатическую сложность для каждого неабстрактного метода и суммирует сложность для классов, пакетов и групп. Согласно определению McCabe1996 цикломатическая сложность - это минимальное количество путей, которые могут в (линейной) комбинации генерировать все возможные пути с помощью метода. Таким образом, значение сложности может служить индикатором количества примеров модульного тестирования, которые полностью охватывают определенную часть программного обеспечения. Показатели сложности всегда можно вычислить, даже при отсутствии отладочной информации в файлах классов.