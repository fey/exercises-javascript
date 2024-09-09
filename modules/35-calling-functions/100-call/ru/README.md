
Сложение, конкатенация, нахождение остатка от деления и остальные рассмотренные операции – все это довольно базовые возможности языков программирования. Математика не ограничена арифметикой, кроме нее есть и множество других разделов со своими операциями, например, геометрия. То же самое касается и строк: их можно переворачивать, менять регистр букв, удалять лишние символы — и это только самое простое. И, наконец, на более высоком уровне есть прикладная логика конкретного приложения. Программы списывают деньги, считают налоги, формируют отчеты. Количество подобных операций бесконечно и индивидуально для каждой программы. И все они должны быть как-то выражены в коде.

Для выражения любой произвольной операции в программировании существует понятие *функция*. Функции бывают как встроенные, так и добавленные программистом. С одной встроенной функцией мы уже знакомы, это `console.log()`.

Функции — одна из ключевых конструкций в программировании, без них невозможно сделать практически ничего. Знакомство с ними мы начинаем как можно раньше, так как весь дальнейший материал оперирует функциями по максимуму. Сначала мы научимся пользоваться уже созданными функциями, а уже потом научимся создавать свои собственные.

Начнем с простых функций для работы над строками. Ниже пример вызова функции `length()`, которая считает количество символов в строке:

```javascript
// length это функция
import { length } from 'hexlet-basics/string';

// Вызов функции length с параметром 'Hello!'
const result = length('Hello!');
console.log(result); // => 6
```

Лирическое отступление. Первая строчка в этом коде - импорт функции из другого модуля. Импорты и модули изучаются на Хекслете, здесь же они будут присутствовать в задании «как есть», так как без них невозможно использовать функции, определенные в других файлах. Не заморачивайтесь, если вам не понятен смысл этого действия, подробнее о нем можно узнать из курса [введение в программирование](https://ru.hexlet.io/courses/introduction_to_programming).

Параметры (или аргументы) — это информация, которую функция получает при вызове. Именно на основе этой информации функция, как правило, вычисляет что-то и выдает результат.

Мы создали константу `result` и указали интерпретатору записать в неё результат, **возвращаемый** функцией `length()` при её вызове. В этом смысле функции подобны операциям - они всегда возвращают результат своей работы.

```javascript
// Вызов length возвращает результат (длину строки)
// который записывается в константу с именем result
const result = length('Hello!');
```

Запись `length('Hello!')` означает, что вызывается функция с именем *length*, в которую был передан параметр `'Hello!'`. Функция `length()` считает длину именно той строки, которая ей была передана.

Вызов функции всегда обозначается скобками `()`, идущими сразу за именем функции. В скобках может быть любое количество параметров, а иногда — вообще ни одного. Количество зависит от используемой функции. Возьмем для примера функцию `pow()`, которая возводит указанное число в нужную степень. Она принимает на вход два параметра и возводит число, переданное первым параметром, в степень, переданную вторым параметром.

```javascript
import { pow } from 'hexlet-basics/math';

// Вызов pow(2, 3) возвращает значение 2 в 3 степени
const result = pow(2, 3); // 2 * 2 * 2
console.log(result); // => 8
```

По большому счету, операторы и функции — это одно и то же. Ключевая разница только в том, как они записываются. Если представить (гипотетически) сложение как функцию, то она будет выглядеть так:

```javascript
// Обычное сложение
3 + 5; // 8
// Сложение представленное как функция
// Выглядит странновато, но передает смысл функций
+(3, 5);
```

## Резюме

Функции вызываются и возвращают результат, который затем может быть использован в дальнейших вычислениях или, например, выведен на экран.

Вопрос на самопроверку. Как узнать, что возвращает вызов функции `console.log()`? Проверьте.

<details>
<summary>Ответ</summary>

Вызов функции `console.log()` возвращает `undefined`.

</details>