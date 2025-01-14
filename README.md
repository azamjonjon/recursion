# Рекурсия в JavaScript

Рекурсия — это когда функция вызывает саму себя, чтобы решить задачу. Это как зеркало, которое смотрит в другое зеркало: процесс повторяется, пока не достигнет конца.

---

## Что нужно знать о рекурсии?

1. **Базовый случай**: Условие, при котором функция перестанет вызывать саму себя.
2. **Рекурсивный случай**: Часть, где функция вызывает себя с новым значением.

Простой пример:
```javascript
function countdown(n) {
    if (n <= 0) { // Базовый случай
        console.log("Всё!");
        return;
    }
    console.log(n);
    countdown(n - 1); // Рекурсивный случай
}

countdown(5); // 5, 4, 3, 2, 1, "Всё!"
```

---

## Примеры задач

### 1. Факториал числа
Факториал числа — это произведение всех чисел от 1 до этого числа.
```javascript
function factorial(n) {
    if (n === 0) { // Базовый случай
        return 1;
    }
    return n * factorial(n - 1); // Рекурсивный случай
}

console.log(factorial(5)); // 120
```
(https://www.bing.com/images/search?view=detailV2&ccid=GEp2gd%2FH&id=3DA2D815DFE40932945E1B28C611A6F5B3C30718&thid=OIP.GEp2gd_Hrgk0HtqvyXnajwHaHa&mediaurl=https%3A%2F%2Ficon-library.com%2Fimages%2Fjavascript-icon-png%2Fjavascript-icon-png-24.jpg&cdnurl=https%3A%2F%2Fth.bing.com%2Fth%2Fid%2FR.184a7681dfc7ae09341edaafc979da8f%3Frik%3DGAfDs%252fWmEcYoGw%26pid%3DImgRaw%26r%3D0&exph=512&expw=512&q=%D1%84%D0%B0%D0%BA%D1%82%D0%BE%D1%80%D0%B8%D0%B0%D0%BB+%D0%B2+js+%D0%BA%D0%B0%D1%80%D1%82%D0%B8%D0%BD%D0%BA%D0%B8&simid=607994501959086065&FORM=IRPRST&ck=787CC4F1D5B4EF5EE037588E38D5C086&selectedIndex=98&itb=1&cw=1375&ch=664&ajaxhist=0&ajaxserp=0)


### 2. Числа Фибоначчи
Каждое число Фибоначчи — это сумма двух предыдущих чисел.
```javascript
function fibonacci(n) {
    if (n <= 1) { // Базовый случай
        return n;
    }
    return fibonacci(n - 1) + fibonacci(n - 2); // Рекурсивный случай
}

console.log(fibonacci(6)); // 8
```

### 3. Сумма чисел до N
Считаем сумму всех чисел от 1 до заданного числа.
```javascript
function sumTo(n) {
    if (n === 1) { // Базовый случай
        return 1;
    }
    return n + sumTo(n - 1); // Рекурсивный случай
}

console.log(sumTo(5)); // 15
```

---

## Как это работает?
Каждый раз, когда функция вызывает саму себя, создаётся новый уровень или "слой". Когда достигается базовый случай, слои начинают исчезать, возвращая результаты.

---

## Запомните
- **Рекурсия** — это просто повторение. 
- Всегда нужен базовый случай, чтобы избежать бесконечного цикла.
- Иногда рекурсию можно заменить обычным циклом.

---

