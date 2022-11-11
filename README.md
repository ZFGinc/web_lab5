<p align = "center">МИНИСТЕРСТВО НАУКИ И ВЫСШЕГО ОБРАЗОВАНИЯ
РОССИЙСКОЙ ФЕДЕРАЦИИ
ФЕДЕРАЛЬНОЕ ГОСУДАРСТВЕННОЕ БЮДЖЕТНОЕ
ОБРАЗОВАТЕЛЬНОЕ УЧРЕЖДЕНИЕ ВЫСШЕГО ОБРАЗОВАНИЯ
«САХАЛИНСКИЙ ГОСУДАРСТВЕННЫЙ УНИВЕРСИТЕТ»</p>
<br><br><br><br><br><br>
<p align = "center">Институт естественных наук и техносферной безопасности<br>Кафедра информатики<br>Хроменков Владимир Александрович</p>
<br><br><br>
<p align = "center">Лабораторная работа №5<br>«Основы языка <strong>JavaScript</strong>»<br>01.03.02 Прикладная математика и информатика</p>
<br><br><br><br><br><br><br><br><br><br><br><br>
<p align = "right">Научный руководитель<br>
Соболев Евгений Игоревич</p>
<br><br><br>
<p align = "center">г. Южно-Сахалинск<br>2022 г.</p>

***
# <p align = "center">Оглавление</p>

- [Цели и задачи](#цели-и-задачи)
- [Решение задач](#решение-задач)
    - [JavaScript](#javascript)
    - [Codewars](#codewars)
- [Вывод](#вывод)

***

# <p align = "center">Цели и задачи</p>


1.  Напишите код, выполнив задание из каждого пункта отдельной строкой:
    -	Создайте пустой объект user.
    -	Добавьте свойство name со значением John.
    -	Добавьте свойство surname со значением Smith.
    -	Измените значение свойства name на Pete.
    -	Удалите свойство name из объекта.
    
2. Напишите функцию `isEmpty(obj)`, которая возвращает `true`, если у объекта нет свойств, иначе `false`. Должно работать так:
    ```js
    let schedule = {};
    alert( isEmpty(schedule) ); // true
    schedule["8:30"] = "get up";
    alert( isEmpty(schedule) ); // false
    ```

3. Можно ли изменить объект, объявленный с помощью `const`? Как вы думаете?
    ```js
    const user = {
    name: "John"
    };
    // это будет работать?
    user.name = "Pete";
    ```
4. У нас есть объект, в котором хранятся зарплаты нашей команды:
    ```js
    let salaries = {
    John: 100,
    Ann: 160,
    Pete: 130
    }
    ```
    Напишите код для суммирования всех зарплат и сохраните результат в переменной `sum`. Должно получиться `390`. Если объект `salaries` пуст, то результат должен быть `0`.

5. Создайте функцию `multiplyNumeric(obj)`, которая умножает все числовые свойства объекта `obj` на `2`.

    Например:

    ```js
    // до вызова функции
    let menu = {
    width: 200,
    height: 300,
    title: "My menu"
    };

    multiplyNumeric(menu);
    // после вызова функции
    menu = {
    width: 400,
    height: 600,
    title: "My menu"
    };
    ```

    Обратите внимание, что `multiplyNumeric` не нужно ничего возвращать. Следует напрямую изменять объект.

6. Что выведет следующий код?
    ```js
    let fruits = ["Яблоки", "Груша", "Апельсин"];

    // добавляем новое значение в "копию"
    let shoppingCart = fruits;
    shoppingCart.push("Банан");

    // что в fruits?
    alert( fruits.length ); // ?
    ```
7. Давайте произведём 5 операций с массивом.

    -	Создайте массив styles с элементами «Джаз» и «Блюз».  
    -	Добавьте «Рок-н-ролл» в конец.  
    -	Замените значение в середине на «Классика».      
        Ваш код для поиска значения в середине должен работать для массивов с любой длиной.
    -	Удалите первый элемент массива и покажите его.  
    -	Вставьте «Рэп» и «Регги» в начало массива.      
    - Массив по ходу выполнения операций:  
        `Джаз, Блюз`  
        `Джаз, Блюз, Рок-н-ролл`  
        `Джаз, Классика, Рок-н-ролл`  
        `Классика, Рок-н-ролл`  
        `Рэп, Регги, Классика, Рок-н-ролл`

8. Каков результат? Почему?
    ```js
    let arr = ["a", "b"];
    arr.push(function() {
    alert( this );
    })
    arr[2](); // ?
    ```
9. Напишите функцию `sumInput()`, которая:
    - Просит пользователя ввести значения, используя `prompt` и сохраняет их в массив.
    - Заканчивает запрашивать значения, когда пользователь введёт не числовое значение, пустую строку или нажмёт `«Отмена»`.
    - Подсчитывает и возвращает сумму элементов массива.

10. На входе массив чисел, например: `arr = [1, -2, 3, 4, -9, 6]`.

    Задача: найти непрерывный подмассив в `arr`, сумма элементов в котором максимальна.

    Функция `getMaxSubSum(arr)` должна возвращать эту сумму.

    Например:

    ```
    getMaxSubSum([-1, 2, 3, -9]) = 5 (сумма выделенных)  
    getMaxSubSum([2, -1, 2, 3, -9]) = 6  
    getMaxSubSum([-1, 2, 3, -9, 11]) = 11  
    getMaxSubSum([-2, -1, 1, 2]) = 3  
    getMaxSubSum([100, -9, 2, -3, 5]) = 100  
    getMaxSubSum([1, 2, 3]) = 6 (берём все)
    ```

    Если все элементы отрицательные – ничего не берём(подмассив пустой) и сумма равна «0»:
    ```
    getMaxSubSum([-1, -2, -3]) = 0
    ```

    Попробуйте придумать быстрое решение: `O(n2)`, а лучше за `О(n)` операций.

11. Удалить в массиве все числа, которые повторяются более двух раз. 

12. Введите одномерный целочисленный массив. Найдите наибольший нечетный элемент. Далее трижды осуществите циклический сдвиг влево элементов, стоящих справа от найденного максимума, и один раз сдвиг элементов вправо, стоящих слева от найденного максимума.

13. Найдите сумму отрицательных элементов массива.

14. Найдите произведение элементов массива с нечетными номерами.

15. Найдите сумму элементов массива между двумя первыми нулями. Если двух нулей нет в массиве, то выведите ноль.

16. Найдите наибольший элемент массива.

17. Найдите наименьший четный элемент массива. Если такого нет, то выведите первый элемент. 

18. Преобразовать массив так, чтобы сначала шли нулевые элементы, а затем все остальные.

19. Найдите сумму номеров минимального и максимального элементов. 

20. Найдите минимальный по модулю элемент массива.

21. Заполнить массив из 10 элементов случайными числами в интервале [-10..10] и сделать реверс отдельно для 1-ой и 2-ой половин массива.

22. Заполнить массив из 12 элементов случайными числами в интервале [-12..12] и выполнить циклический сдвиг ВПРАВО на 4 элемента.


## [Codewars](https://www.codewars.com)

23.	[Javascript Mathematician](https://www.codewars.com/kata/javascript-mathematician)

24.	[Javascript from the Inside #1 : Map](https://www.codewars.com/kata/javascript-from-the-inside-number-1-map)

25.	[Javascript from the Inside #2: Filter](https://www.codewars.com/kata/javascript-from-the-inside-number-2-filter)

26.	[Power .bind()](https://www.codewars.com/kata/power-bind)

27.	[Closures and Scopes](https://www.codewars.com/kata/closures-and-scopes)

28.	[Can you keep a secret?](https://www.codewars.com/kata/can-you-keep-a-secret)

***

# <p align = "center">Решение задач</p>

## JavaScript

```js
//1.
//  Создайте пустой объект user.
var user1 = {};
//  Добавьте свойство name со значением John.
user1.name = "John";
//  Добавьте свойство surname со значением Smith.
user1.surname = "Smith";
//  Измените значение свойства name на Pete.
user1["name"] = "Pit";
//  Удалите свойство name из объекта.
delete user1.name;

//2.
function isEmpty(obj) {
    if (Object.keys(obj).length)
        return true;

    return false;
}

let schedule = {};
console.log(isEmpty(schedule)); // true
schedule["8:30"] = "get up";
console.log(isEmpty(schedule)); // false

//3.
const user3 = {
    name: "John"
};

// это будет работать?
user3.name = "Pete"; // Да

//4.
const salaries = {
    John: 100,
    Ann: 160,
    Pete: 130
}

var sum = 0;
for (const i in salaries) {
    sum += +salaries[i];
}

//5.
let menu = {
    width: 200,
    height: 300,
    title: "My menu"
};

function multiplyNumeric(menu) {
    for (const x in menu) {
        if (!isNaN(menu[x]))
            menu[x] *= 2;
    }
}

//6.
let fruits = ["Яблоки", "Груша", "Апельсин"];

// добавляем новое значение в "копию"
let shoppingCart = fruits;
shoppingCart.push("Банан");

// что в fruits?
console.log(fruits.length); //! 4 (ссылки одинаковые)

//7.
//  Создайте массив styles с элементами «Джаз» и «Блюз».
let styles = ['Джаз', 'Блюз'];
//  Добавьте «Рок-н-ролл» в конец.
styles.push('Рок-н-ролл');
//  Замените значение в середине на «Классика». Ваш код для поиска значения в середине должен работать для массивов с любой длиной.
styles[Math.floor(styles.length / 2)] = 'Классика';
//  Удалите первый элемент массива и покажите его.
console.log(styles.shift());
//  Вставьте «Рэп» и «Регги» в начало массива.
styles.unshift('Рэп', 'Регги');

//8. Каков результат? Почему?
var arr = ["a", "b"];
arr.push(function () {
    //alert(this);
})
console.log(arr[2]()); // undefined

// 9. Просит пользователя ввести значения, используя prompt и сохраняет их в массив.
let mas = [];
do {
    let data = prompt();
    //  Заканчивает запрашивать значения, когда пользователь введёт не числовое значение, пустую строку или нажмёт «Отмена».
    if (!isNaN(data) || data === null)
        break;
    mas.push(data);
} while (true);
//  Подсчитывает и возвращает сумму элементов массива.
console.log(mas.length);

//10. найти непрерывный подмассив в arr, сумма элементов в котором максимальна.
var arr10 = [1, -2, 3, 4, -9, 6];

function getMaxSubSum(arr) {
    let newSum = 0, maxSum = 0;
    for (let i = 0; i < arr.length; i++) {
        newSum += arr[i];
        if (arr[i] > newSum) newSum = arr[i];
        if (newSum > maxSum) maxSum = newSum;
    }

    return maxSum;
}
console.log("10.", maxSum(arr10));

//11. Удалить в массиве все числа, которые повторяются более двух раз. 
function onlyDoubles(arr) {
    let temp = [];
    let map = new Map();

    for (const elem of arr) {
        let inMap = map.get(elem);

        console.log(inMap);

        if (!inMap || inMap < 2) {
            map.set(elem, (inMap ?? 0) + 1)
            temp.push(elem);
        }

    }

    return arr = temp;
}

let doubles = [1, 1, 1, 1, 1, 2, 3, 4, 4, 5, 6, 7, 7, 7];
console.log(onlyDoubles(doubles));

// 12.
function Left3Right1FromMax(arr) {
    let max = arr[0], idx = 0;
    for (let i = 1; i < arr.length; i++) {
        if (arr[i] > max) {
            max = arr[i];
            idx = i;
        }
    }

    // Сдвиг 3 влево
    for (let i = 0; i < 3; i++) {
        if (idx === arr.length - 1) break;
        let temp = arr[idx + 1];
        arr.splice(idx + 1, 1);
        arr.splice(idx, 0, temp);
        idx++;
    }

    let temp = arr[idx - 1];
    arr.splice(idx - 1, 1);
    arr.splice(idx, 0, temp);
}

var arr12 = [1, 2, 3, 4, 5, 4, 3, 2, 1];
Left3Right1FromMax(arr12);
console.log("12. " + arr12);

// 13. Найдите сумму отрицательных элементов массива.
function NegativeSum(arr) {
    return arr.reduce((acc, elem) => elem < 0 ? acc += elem : acc);
}
var arr13 = [-5, -4, -3, -2, -1, 0, 1, 2, 3, 4, 5];
console.log("13.", NegativeSum(arr13));

// 14. Найдите произведение элементов массива с нечетными номерами.
function ProdOddIdx(arr) {
    return arr.reduce((acc, elem, idx) => idx % 2 != 0 ? acc *= elem : acc);
}
var arr14 = [1, 2, 3, 4, 5];
console.log("14.", ProdOddIdx(arr14));

// 15. Найдите сумму элементов массива между двумя первыми нулями. Если двух нулей нет в массиве, то выведите ноль.
function betweenZeros(arr) {
    let pos1, pos2;

    for (let i = 0; i < arr.length; i++) {
        arr[i] === 0 && !pos1 ? pos1 = i : pos2 = i
    }

    if (!pos1 || !pos2)
        return 0;

    let sum = 0;
    for (let i = pos1 + 1; i < pos2; i++) {
        sum += arr[i];
    }

    return sum;
}

var arr15 = [0, 2, 3, 3, 4, 0, 3, 3, 4, 5];
console.log("между нулями:", betweenZeros(arr15));

//16. Найдите наибольший элемент массива
var arr = [5, 6, 7, 1, 2, 9, 11];
console.log("16.", Math.max.apply(null, arr));

// 17. Найдите наименьший четный элемент массива. Если такого нет, то выведите первый элемент.
function minOdd(arr) {
    let min = arr[0];

    for (const elem of arr) {
        if (elem < min && elem % 2 == 0)
            min = elem;
    }

    return min;
}

// 18. Преобразовать массив так, чтобы сначала шли нулевые элементы, а затем все остальные.
function StartsWithZeros(arr) {
    for (let i = 1; i < arr.length; i++) {
        if (arr[i] === 0)
            arr.unshift(arr.splice(i--, 1)[0]);
    }
}
var arr18 = [0, 1, 2, 3, 0, 4, 5, 0, 6, 7, 0, 8, 0, 0, 0, 9];
StartsWithZeros(arr18);
console.log("18.", arr18);

//19. Найдите сумму номеров минимального и максимального элементов.
function MinMaxIdxSum(arr) {
    let min = arr[0], max = arr[0], idx1 = 0, idx2 = 0;
    for (let i = 1; i < arr.length; i++) {
        if (arr[i] < min) {
            min = arr[i];
            idx1 = i;
        }

        if (arr[i] > max) {
            max = arr[i];
            idx2 = i;
        }
    }

    return idx1 + idx2;
}

var arr19 = [7, -5, 2, -1, 9, 1, 2, 0];
console.log("19.", MinMaxIdxSum(arr19));

//20. Найдите минимальный по модулю элемент массива.
function MinAbs(arr) {
    return arr.reduce((a, b) => Math.min(Math.abs(a), Math.abs(b)));
}
let arr20 = [-3, -2, -1, 1, 2, 3];
console.log("20.", MinAbs(arr20));

//21. Заполнить массив из 10 элементов случайными числами в интервале [-10..10] и сделать реверс отдельно для 1-ой и 2-ой половин массива.
function RandRevers() {
    let arr = [];
    for (let i = 0; i < 10; i++) {
        arr[i] = Math.floor(Math.random() * (10 - -10 + 1)) - 10;
    }

    return arr = [...arr.slice(0, 5).reverse(), ...arr.slice(5, 10).reverse()]
}
console.log(RandRevers());

//22. Заполнить массив из 12 элементов случайными числами в интервале [-12..12]
//    и выполнить циклический сдвиг ВПРАВО на 4 элемента.
function RandMoveLeft4() {
    let arr = [];
    for (let i = 0; i < 10; i++) {
        arr[i] = Math.floor(Math.random() * (12 - -12 + 1)) - 12;
    }

    console.log("arr:", arr);

    for (let i = 0; i < 4; i++) {
        arr.unshift(arr.pop());
    }

    return arr;
}
console.log(RandMoveLeft4());
```

## [Codewars](https://www.codewars.com) ([Profile Link](https://www.codewars.com/users/ZFGinc))

### [Javascript Mathematician](https://www.codewars.com/kata/javascript-mathematician)

```js
function calculate(...args1) {
    return function (...args2) {
        return [].concat([...args1], [...args2]).reduce((a, b) => a + b, 0);
    }
}
```

<p align = "center">
<img src = "img/1.PNG">
</p>

### [Javascript from the Inside #1 : Map](https://www.codewars.com/kata/javascript-from-the-inside-number-1-map)

```js
Array.prototype.map = function (callback, context) {
    const newArr = new Array(this.length)
    
    for (let i = 0; i < this.length; i++) {
        if (i in this) newArr[i] = callback.call(context,this[i], i, this)
    }

    return newArr
}
```

<p align = "center">
<img src = "img/2.PNG">
</p>

### [Javascript from the Inside #2: Filter](https://www.codewars.com/kata/javascript-from-the-inside-number-2-filter)

```js
Array.prototype.filter = function (callback, context) {
    const newArr = [];
    const len = this.length;
  
    for (let i = 0; i < len; i++) {
        if (i in this && callback.call(context,this[i], i, this))
          newArr.push(this[i]);
    }
  
    return newArr;
}
```

<p align = "center">
<img src = "img/3.PNG">
</p>

### [Power .bind()](https://www.codewars.com/kata/power-bind)
 
```js
Function.prototype.bind = function (root) {
  return (child = root) => this.call(child, child);
};
```

<p align = "center">
<img src = "img/4.PNG">
</p>

### [Closures and Scopes](https://www.codewars.com/kata/closures-and-scopes)

```js
function createFunctions(n) {
  var callbacks = [];

  for (let i=0; i<n; i++) {
    callbacks.push(function() {
      return i;
    });
  }
  
  return callbacks;
}
```

<p align = "center">
<img src = "img/5.PNG">
</p>

### [Can you keep a secret?](https://www.codewars.com/kata/can-you-keep-a-secret)

```js
function createSecretHolder(secret) {
  return {
    getSecret: function() { return secret; },
    setSecret: function(scr) { secret = scr; }
  };
}
```

<p align = "center">
<img src = "img/6.PNG">
</p>

***

# <p align = "center">Вывод</p>

Выполнил *лабораторную работу №5*, совершенствую навыки работы с языком `JavaScript`, решая все более и более сложные задачи.
