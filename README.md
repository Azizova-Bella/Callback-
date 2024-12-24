# NEWTHEME
![image](https://github.com/user-attachments/assets/875774b2-087b-4469-b35b-a30934250de8)

# Использование методов callback, filter, map и forEach в JavaScript

## Callback-функции
**Callback** — это функция, переданная в другую функцию как аргумент. Она будет вызвана позже, после выполнения основной функции.
![image](https://github.com/user-attachments/assets/cdc809f1-e2b1-4a01-9880-7c9d1703402b)

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


# Методы массивов в JavaScript: `find`, `toSorted`, `reduce`, `some`, `every`

## 1. Метод `find`
Метод `find` используется для поиска первого элемента в массиве, который удовлетворяет заданному условию.

**Синтаксис:**
```javascript
const элемент = массив.find(callback[, thisArg]);
```

**Пример:**
```javascript
const числа = [5, 12, 8, 130, 44];
const больше10 = числа.find((число) => число > 10);

console.log(больше10); // 12
```

## 2. Метод `toSorted`
Метод `toSorted` создает новый отсортированный массив, не изменяя исходный массив.

**Синтаксис:**
```javascript
const новыйМассив = массив.toSorted([compareFunction]);
```

**Пример:**
```javascript
const числа = [5, 2, 8, 1, 4];
const отсортированные = числа.toSorted((a, b) => a - b);

console.log(отсортированные); // [1, 2, 4, 5, 8]
console.log(числа); // [5, 2, 8, 1, 4] (исходный массив не изменился)
```

## 3. Метод `reduce`
Метод `reduce` используется для последовательной обработки каждого элемента массива с целью получения единого итогового значения.

**Синтаксис:**
```javascript
const результат = массив.reduce(callback[, начальноеЗначение]);
```

**Пример:**
```javascript
const числа = [1, 2, 3, 4];
const сумма = числа.reduce((сумма, число) => сумма + число, 0);

console.log(сумма); // 10
```

## 4. Метод `some`
Метод `some` проверяет, удовлетворяет ли хотя бы один элемент массива заданному условию. Возвращает `true` или `false`.

**Синтаксис:**
```javascript
const результат = массив.some(callback[, thisArg]);
```

**Пример:**
```javascript
const числа = [3, 5, 8, 10];
const естьЧетное = числа.some((число) => число % 2 === 0);

console.log(естьЧетное); // true
```

## 5. Метод `every`
Метод `every` проверяет, удовлетворяют ли все элементы массива заданному условию. Возвращает `true` или `false`.

**Синтаксис:**
```javascript
const результат = массив.every(callback[, thisArg]);
```

**Пример:**
```javascript
const числа = [2, 4, 6, 8];
const всеЧетные = числа.every((число) => число % 2 === 0);

console.log(всеЧетные); // true
```

---

Эти методы помогают упростить работу с массивами и сделать код более читаемым и функциональным.


## Заключение
Эти методы облегчают работу с массивами и позволяют писать чистый и понятный код. Используйте `filter` для фильтрации, `map` для преобразования данных, `forEach` для итерации, а callback-функции для гибкого управления логикой в других методах.
