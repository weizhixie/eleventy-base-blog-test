---
title: Loops, Arrays and Objects - Practical lesson tasks
description: Loops, Arrays and Objects - Practical
date: 2023-08-27
tags:
  - Loops, Arrays and Objects - Practical
---
```js
//Task 1
const shoppingCart = [
    { name: "loaf of bread", type: "food", quantity: 1, price: 0.85 },
    { name: "multipack beans", type: "food", quantity: 1, price: 1 },
    { name: "mushrooms", type: "food", quantity: 10, price: 0.1 },
    { name: "can of beer", type: "alcohol", quantity: 4, price: 1.1 },
    { name: "prosecco", type: "alcohol", quantity: 1, price: 8.99 },
    { name: "steak", type: "food", quantity: 2, price: 3.99 },
    { name: "blue cheese", type: "food", quantity: 1, price: 2.99 },
    { name: "candles", type: "home", quantity: 3, price: 1.99 },
    { name: "cheesecake", type: "food", quantity: 1, price: 4.99 },
    { name: "onions", type: "food", quantity: 3, price: 0.4 }
];
function cart(shoppingCart) {
    let totalPrice = 0;
    for (const item of shoppingCart) {
        totalPrice += item.price * item.quantity;
    }
    return Math.round(totalPrice * 100) / 100;
}
console.log(`Total price = £${cart(shoppingCart)}`);

//Task 2
const shoppingCart = [
    { name: "loaf of bread", type: "food", quantity: 1, price: 0.85 },
    { name: "multipack beans", type: "food", quantity: 1, price: 1 },
    { name: "mushrooms", type: "food", quantity: 10, price: 0.1 },
    { name: "can of beer", type: "alcohol", quantity: 4, price: 1.1 },
    { name: "prosecco", type: "alcohol", quantity: 1, price: 8.99 },
    { name: "steak", type: "food", quantity: 2, price: 3.99 },
    { name: "blue cheese", type: "food", quantity: 1, price: 2.99 },
    { name: "candles", type: "home", quantity: 3, price: 1.99 },
    { name: "cheesecake", type: "food", quantity: 1, price: 4.99 },
    { name: "onions", type: "food", quantity: 3, price: 0.4 }
];
const foodDiscount = 20;

function getDiscount(shoppingCart) {
    let totalPrice = 0;
    for (const item of shoppingCart) {
        if (item.type === "food") {
            totalPrice += (item.price * item.quantity)
                - (item.price * item.quantity / 100 * foodDiscount);
        } else {
            totalPrice += item.price * item.quantity;
        }
    }
    return Math.round(totalPrice * 100) / 100;
}
console.log(`Total price with 20% food discount = £${getDiscount(shoppingCart)}`);

//Task 3
const shoppingCart = [
    { name: "loaf of bread", type: "food", quantity: 1, price: 0.85 },
    { name: "multipack beans", type: "food", quantity: 1, price: 1 },
    { name: "mushrooms", type: "food", quantity: 10, price: 0.1 },
    { name: "can of beer", type: "alcohol", quantity: 4, price: 1.1 },
    { name: "prosecco", type: "alcohol", quantity: 1, price: 8.99 },
    { name: "steak", type: "food", quantity: 2, price: 3.99 },
    { name: "blue cheese", type: "food", quantity: 1, price: 2.99 },
    { name: "candles", type: "home", quantity: 3, price: 1.99 },
    { name: "cheesecake", type: "food", quantity: 1, price: 4.99 },
    { name: "onions", type: "food", quantity: 3, price: 0.4 }
];

getTotal = (cart, discountAmount, type) => {
    let totalPrice = 0;
    for (const item of cart) {
        let itemTotal = item.price * item.quantity;
        if (type === "any" || item.type === type) {
            itemTotal -= itemTotal / 100 * discountAmount;
        }
        totalPrice += itemTotal;
    }
    return Math.round(totalPrice * 100) / 100;
};
console.log(`Total price = £${getTotal(shoppingCart, 10, "any")}`);

//Task 4
const shoppingCart = [
    { name: "loaf of bread", type: "food", quantity: 1, price: 0.85 },
    { name: "multipack beans", type: "food", quantity: 1, price: 1 },
    { name: "mushrooms", type: "food", quantity: 10, price: 0.1 },
    { name: "can of beer", type: "alcohol", quantity: 4, price: 1.1 },
    { name: "prosecco", type: "alcohol", quantity: 1, price: 8.99 },
    { name: "steak", type: "food", quantity: 2, price: 3.99 },
    { name: "blue cheese", type: "food", quantity: 1, price: 2.99 },
    { name: "candles", type: "home", quantity: 3, price: 1.99 },
    { name: "cheesecake", type: "food", quantity: 1, price: 4.99 },
    { name: "onions", type: "food", quantity: 3, price: 0.4 }
];

function getPriceBetween(cart, lowPrice, highPrice) {
    const arrItems = [];
    for (let i = 0; i < cart.length; i++) {
        if (cart[i].price >= lowPrice && cart[i].price <= highPrice) {
            arrItems.push(cart[i]);
        }
    }
    return arrItems;
}
console.log(getPriceBetween(shoppingCart, 2, 5));

//Task 5
const shoppingCart = [
    { name: "loaf of bread", type: "food", quantity: 1, price: 0.85 },
    { name: "multipack beans", type: "food", quantity: 1, price: 1 },
    { name: "mushrooms", type: "food", quantity: 10, price: 0.1 },
    { name: "can of beer", type: "alcohol", quantity: 4, price: 1.1 },
    { name: "prosecco", type: "alcohol", quantity: 1, price: 8.99 },
    { name: "steak", type: "food", quantity: 2, price: 3.99 },
    { name: "blue cheese", type: "food", quantity: 1, price: 2.99 },
    { name: "candles", type: "home", quantity: 3, price: 1.99 },
    { name: "cheesecake", type: "food", quantity: 1, price: 4.99 },
    { name: "onions", type: "food", quantity: 3, price: 0.4 }
];

function getPriceBetween(cart, lowPrice, highPrice, quantity) {
    const arrItems = [];
    let totalPrice = 0;

    for (let i = 0; i < cart.length; i++) {
        if (cart[i].price >= lowPrice && cart[i].price <= highPrice) {
            arrItems.push(cart[i]);
        }
    }

    if (quantity) {
        for (const item of arrItems) {
            totalPrice += item.price * item.quantity;
        }
    }
    return totalPrice;
}
console.log(getPriceBetween(shoppingCart, 2, 5, true));

//Task 6 - mode, median or mean of the numbers
const grades = [95, 80, 77, 77, 88, 95, 95, 68, 99];

mean = (numbers) => {
    let total = 0;
    for (let i = 0; i < numbers.length; i++) {
        total += numbers[i];
    }
    return total / numbers.length;
};

median = (numbers) => {
    numbers.sort((a, b) => a - b);
    const half = Math.floor(numbers.length / 2);

    if (numbers.length % 2 === 0) {
        return (numbers[half - 1] + numbers[half]) / 2;
    }
    return numbers[half];
};

mode = (numbers) => {
    const modeObj = {};
    for (let i = 0; i < numbers.length; i++) {
        if (!modeObj[numbers[i]]) {
            modeObj[numbers[i]] = 0;
        }
        modeObj[numbers[i]]++;
    }

    let modeNumValue = -1;
    let modeNumKey = -1;

    for (const key in modeObj) {
        if (modeObj[key] > modeNumValue) {
            modeNumValue = modeObj[key];
            modeNumKey = key;
        }
    }
    return modeNumKey;
};

console.log("mean = " + mean(grades));
console.log("median = " + median(grades));
console.log("mode = " + mode(grades));

//Task 7
mmmFunc = (grades, method) => {
    switch (method) {
        case "mean":
            return `${method} = ${mean(grades)}`;
        case "median":
            return `${method} = ${median(grades)}`;
        case "mode":
            return `${method} = ${mode(grades)}`;
    }
};
console.log(mmmFunc(grades, 'mode'));

```
<script>
//Task 1
const shoppingCart = [
    { name: "loaf of bread", type: "food", quantity: 1, price: 0.85 },
    { name: "multipack beans", type: "food", quantity: 1, price: 1 },
    { name: "mushrooms", type: "food", quantity: 10, price: 0.1 },
    { name: "can of beer", type: "alcohol", quantity: 4, price: 1.1 },
    { name: "prosecco", type: "alcohol", quantity: 1, price: 8.99 },
    { name: "steak", type: "food", quantity: 2, price: 3.99 },
    { name: "blue cheese", type: "food", quantity: 1, price: 2.99 },
    { name: "candles", type: "home", quantity: 3, price: 1.99 },
    { name: "cheesecake", type: "food", quantity: 1, price: 4.99 },
    { name: "onions", type: "food", quantity: 3, price: 0.4 }
];
function cart(shoppingCart) {
    let totalPrice = 0;
    for (const item of shoppingCart) {
        totalPrice += item.price * item.quantity;
    }
    return Math.round(totalPrice * 100) / 100;
}
console.log(`Total price = £${cart(shoppingCart)}`);

//Task 2
const foodDiscount = 20;

function getDiscount(shoppingCart) {
    let totalPrice = 0;
    for (const item of shoppingCart) {
        if (item.type === "food") {
            totalPrice += (item.price * item.quantity)
                - (item.price * item.quantity / 100 * foodDiscount);
        } else {
            totalPrice += item.price * item.quantity;
        }
    }
    return Math.round(totalPrice * 100) / 100;
}
console.log(`Total price with 20% food discount = £${getDiscount(shoppingCart)}`);


//Task 3
getTotal = (cart, discountAmount, type) => {
    let totalPrice = 0;
    for (const item of cart) {
        let itemTotal = item.price * item.quantity;
        if (type === "any" || item.type === type) {
            itemTotal -= itemTotal / 100 * discountAmount;
        }
        totalPrice += itemTotal;
    }
    return Math.round(totalPrice * 100) / 100;
};
console.log(`Total price = £${getTotal(shoppingCart, 10, "any")}`);

//Task 4
function getPriceBetween(cart, lowPrice, highPrice) {
    const arrItems = [];
    for (let i = 0; i < cart.length; i++) {
        if (cart[i].price >= lowPrice && cart[i].price <= highPrice) {
            arrItems.push(cart[i]);
        }
    }
    return arrItems;
}
console.log(getPriceBetween(shoppingCart, 2, 5));

//Task 5
function getPriceBetween1(cart, lowPrice, highPrice, quantity) {
    const arrItems = [];
    let totalPrice = 0;

    for (let i = 0; i < cart.length; i++) {
        if (cart[i].price >= lowPrice && cart[i].price <= highPrice) {
            arrItems.push(cart[i]);
        }
    }

    if (quantity) {
        for (const item of arrItems) {
            totalPrice += item.price * item.quantity;
        }
    }
    return totalPrice;
}
console.log(getPriceBetween1(shoppingCart, 2, 5, true));

//Task 6 - mode, median or mean of the numbers
const grades = [95, 80, 77, 77, 88, 95, 95, 68, 99];

mean = (numbers) => {
    let total = 0;
    for (let i = 0; i < numbers.length; i++) {
        total += numbers[i];
    }
    return total / numbers.length;
};

median = (numbers) => {
    numbers.sort((a, b) => a - b);
    const half = Math.floor(numbers.length / 2);

    if (numbers.length % 2 === 0) {
        return (numbers[half - 1] + numbers[half]) / 2;
    }
    return numbers[half];
};

mode = (numbers) => {
    const modeObj = {};
    for (let i = 0; i < numbers.length; i++) {
        if (!modeObj[numbers[i]]) {
            modeObj[numbers[i]] = 0;
        }
        modeObj[numbers[i]]++;
    }

    let modeNumValue = -1;
    let modeNumKey = -1;

    for (const key in modeObj) {
        if (modeObj[key] > modeNumValue) {
            modeNumValue = modeObj[key];
            modeNumKey = key;
        }
    }
    return modeNumKey;
};

console.log("mean = " + mean(grades));
console.log("median = " + median(grades));
console.log("mode = " + mode(grades));

//Task 7
mmmFunc = (grades, method) => {
    switch (method) {
        case "mean":
            return `${method} = ${mean(grades)}`;
        case "median":
            return `${method} = ${median(grades)}`;
        case "mode":
            return `${method} = ${mode(grades)}`;
    }
};
console.log(mmmFunc(grades, 'mode'));
</script>

