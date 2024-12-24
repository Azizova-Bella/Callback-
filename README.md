# NEWTHEME

# Использование методов callback, filter, map и forEach в JavaScript

## Callback-функции
**Callback** — это функция, переданная в другую функцию как аргумент. Она будет вызвана позже, после выполнения основной функции.

Пример: 
```javascript
function processArray(arr, callback) {
    const result = [];
    for (let i = 0; i < arr.length; i++) {
        result.push(callback(arr[i]));
    }
    return result;
}

const numbers = [1, 2, 3, 4];
const doubled = processArray(numbers, (num) => num * 2);

console.log(doubled); // [2, 4, 6, 8]
```

---

## Метод filter
Метод `filter` используется для фильтрации массива на основе заданного условия. Он возвращает новый массив с элементами, которые соответствуют этому условию.

Пример:
```javascript
const numbers = [1, 2, 3, 4, 5, 6];

// Фильтруем только чётные числа
const evenNumbers = numbers.filter((num) => num % 2 === 0);

console.log(evenNumbers); // [2, 4, 6]
```

---

## Метод map
Метод `map` создаёт новый массив, применяя функцию преобразования к каждому элементу исходного массива.

Пример:
```javascript
const numbers = [1, 2, 3, 4];

// Умножаем каждое число на 10
const multipliedNumbers = numbers.map((num) => num * 10);

console.log(multipliedNumbers); // [10, 20, 30, 40]
```

---

## Метод forEach
Метод `forEach` выполняет указанную функцию один раз для каждого элемента массива. В отличие от `map`, он ничего не возвращает.

Пример:
```javascript
const numbers = [1, 2, 3, 4];

// Выводим каждый элемент в консоль
numbers.forEach((num) => {
    console.log(num);
});

// Вывод:
// 1
// 2
// 3
// 4
```

---

## Заключение
Эти методы облегчают работу с массивами и позволяют писать чистый и понятный код. Используйте `filter` для фильтрации, `map` для преобразования данных, `forEach` для итерации, а callback-функции для гибкого управления логикой в других методах.
