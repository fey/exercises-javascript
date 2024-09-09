
Объявление переменных возможно и без указания конкретного значения. Что будет выведено на экран если её распечатать?

```javascript
let name;
console.log(name); // ?
```

На экране появится `undefined`, специальное значение особого типа, которое означает отсутствие значения. Undefined активно используется самим JavaScript в самых разных ситуациях, например, при обращении к несуществующему символу строки:

```javascript
const name = 'Arya';
console.log(name[8]);
```

https://replit.com/@hexlet/js-basics-data-types-undefined

Смысл (семантика) значения `undefined` именно в том, что значения нет. Однако, ничто не мешает написать такой код:

```javascript
let key = undefined;
```

И хотя интерпретатор позволяет такое сделать, это нарушение семантики значения `undefined`, ведь в этом коде выполняется присваивание, а значит — подставляется значение.

JavaScript — один из немногих языков, в которых в явном виде присутствует понятие `undefined`. В остальных языках его роль выполняет значение `null`, которое, кстати, тоже есть в JavaScript.

*Вопрос на самопроверку. Почему нельзя объявить константу без указания значения?*

<details>
<summary>Ответ</summary>

Константу невозможно изменить или переопределить. Ее значение необходимо указывать строго при определении.

</details>