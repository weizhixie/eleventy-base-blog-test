---
title: Intro to JS Practicals
description: Intro to JS Practicals
date: 2023-08-19
tags:
  - Intro to JS Practicals
---
```js
/**
 * Percentage Calculator
 * Create a function that is able to return a specific percentage of any number.
*/
function percentageCalculator(inputNumber, inputPercentage) {
    if ((!Number.isInteger(inputNumber) && Number.isInteger(inputPercentage))) {
        return "Please enter a valid number.";
    }
    return inputNumber / 100 * inputPercentage;
}

console.log(percentageCalculator(135, 30));

/**
 * Switch Statement
 * Customers can order 3 different types of drink and also select 3 sizes.
 * Cola, Lemonade and  Orangeade
 * Small, Medium and Large
*/
function drinkOrder(inputSize, inputDrink) {
    const lowerCaseDrink = inputDrink.toLowerCase();
    let drinkLabel;

    switch (lowerCaseDrink) {
        case "lemon":
            drinkLabel = "Lemonade";
            break;
        case "orange":
            drinkLabel = "Orangeade";
            break;
        case "cola":
            drinkLabel = "Cola";
            break;
        }
        return `You have ordered a ${inputSize} of ${drinkLabel}`;
    }

console.log(drinkOrder("large", "Orange"));

/**
 * Calculator
 * a function capable of using the addition, subtraction, multiply, 
 * divider or modulus operator on 2 numbers provided.
*/
function calculator(inputNumber1, inputOperator, inputNumber2) {
    let result;
    switch (inputOperator) {
        case "%":
            result = inputNumber1 % inputNumber2;
            break;
        case "*":
            result = inputNumber1 * inputNumber2;
            break;
        case "/":
            result = inputNumber1 / inputNumber2;
            break;
        case "+":
            result = inputNumber1 + inputNumber2;
            break;
        case "-":
            result = inputNumber1 - inputNumber2;
            break;
    }
    return `${inputNumber1} ${inputOperator} ${inputNumber2} = ${result}`;
}

console.log(calculator(135, "/", 5));
```

<script>
    /**
    * Percentage Calculator
    * Create a function that is able to return a specific percentage of any number.
    */
    function percentageCalculator(inputNumber, inputPercentage) {
        if ((!Number.isInteger(inputNumber) && Number.isInteger(inputPercentage))) {
            return "Please enter a valid number.";
        }
        return inputNumber / 100 * inputPercentage;
    }

    console.log(percentageCalculator(135, 30));

    function drinkOrder(inputSize, inputDrink) {
        const lowerCaseDrink = inputDrink.toLowerCase();
        let drinkLabel;

        switch (lowerCaseDrink) {
            case "lemon":
                drinkLabel = "Lemonade";
                break;
            case "orange":
                drinkLabel = "Orangeade";
                break;
            case "cola":
                drinkLabel = "Cola";
                break;
            }
            return `You have ordered a ${inputSize} of ${drinkLabel}`;
        }

    console.log(drinkOrder("large", "Orange"));

        function calculator(inputNumber1, inputOperator, inputNumber2) {
            let result;
            switch (inputOperator) {
                case "%":
                    result = inputNumber1 % inputNumber2;
                    break;
                case "*":
                    result = inputNumber1 * inputNumber2;
                    break;
                case "/":
                    result = inputNumber1 / inputNumber2;
                    break;
                case "+":
                    result = inputNumber1 + inputNumber2;
                    break;
                case "-":
                    result = inputNumber1 - inputNumber2;
                    break;
            }
            return `${inputNumber1} ${inputOperator} ${inputNumber2} = ${result}`;
        }

    console.log(calculator(135, "/", 5));
</script>
