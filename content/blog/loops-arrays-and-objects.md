---
title: Loops, Arrays and Objects - Lesson 1 Tasks
description: Loops, Arrays and Objects
date: 2023-08-26
tags:
  - Loops, Arrays and Objects
---
```js
//Task 1 - Write a loop that outputs the 7 times table,
for (let i = 1; i <= 12; i++) {
    console.log(`7 x ${i} = ${7*i}`);
}

/**
 * Task 2
 * 1. Create an array of your favourite foods.
 * 2. Print some of them to the screen
*/
const favoriteFood = ["burger", "pizza", "noodle"];
console.log(favoriteFood[0]);
console.log(favoriteFood[1]);

//Task 3 - Use a for loop to print a list of all your favourite foods
const favoriteFood = ["burger", "pizza", "noodle"];
for (let i = 0; i < favoriteFood.length; i++) {
    console.log(favoriteFood[i]);
}

/**
 * Task 4
 * Create an object to hold information on your favourite recipe. Then display the properties on screen.
*/
const recipe = {
    title: "Chickpea & coriander burgers",
    servings: 4,
    ingredients: ["400g can chickpeas, drained", "zest 1 lemon, plus juice ½", "1 tsp ground cumin"],
    direction: ["STEP 1", "More in github"]
};
for (const key in recipe) {
    if (key === "ingredients" || key === "direction") {
        for (const item of recipe[key]) {
            console.log(`${key}: ${item}`);
        }
    } else {
        console.log(`${key}: ${recipe[key]}`);
    }
}

//Task 5 - Add a function called letsCook
const recipe = {
    title: "Chickpea & coriander burgers",
    servings: 4,
    ingredients: ["400g can chickpeas, drained", "zest 1 lemon, plus juice ½", "1 tsp ground cumin"],
    direction: ["STEP 1", "More in github"],
    letsCook() {
        console.log(`I'm hungry! Let's cook ${this.title}`);
    },

};
recipe.letsCook();
```
<script>
//Task 1
for (let i = 1; i <= 12; i++) {
    console.log(`7 x ${i} = ${7*i}`);
}

//Task 2
const favoriteFood = ["burger", "pizza", "noodle"];
console.log(favoriteFood[0]);
console.log(favoriteFood[1]);

//Task 3
const favoriteFood2 = ["burger", "pizza", "noodle"];
for (let i = 0; i < favoriteFood.length; i++) {
    console.log(favoriteFood[i]);
}

//Task 4
const recipe = {
    title: "Chickpea & coriander burgers",
    servings: 4,
    ingredients: ["400g can chickpeas, drained", "zest 1 lemon, plus juice ½", "1 tsp ground cumin",
        "small bunch coriander, chopped", "1 egg", "100g fresh breadcrumbs",
        "1 medium red onion, ½ diced, ½ sliced", "1 tbsp olive oil", "small wholemeal buns",
        "1 large tomato, sliced, ½ cucumber, sliced and chilli sauce, to serve"],
    direction: ["STEP 1", "In a food processor, whizz the chickpeas, lemon zest, lemon juice, cumin, half the coriander, the egg and some seasoning. Scrape into a bowl and mix with 80g of the breadcrumbs and the diced onions. Form 4 burgers, press remaining breadcrumbs onto both sides and chill for at least 10 mins.",
        "STEP 2", "Heat the oil in a frying pan until hot. Fry the burgers for 4 mins each side, keeping the heat on medium so they don’t burn. To serve, slice each bun and fill with a slice of tomato, a burger, a few red onion slices, some cucumber slices, a dollop of chilli sauce and the remaining coriander."]
};
for (const key in recipe) {
    if (key === "ingredients" || key === "direction") {
        for (const item of recipe[key]) {
            console.log(`${key}: ${item}`);
        }
    } else {
        console.log(`${key}: ${recipe[key]}`);
    }
}

//Task 5
const recipe2 = {
    title: "Chickpea & coriander burgers",
    servings: 4,
    ingredients: ["400g can chickpeas, drained", "zest 1 lemon, plus juice ½", "1 tsp ground cumin",
        "small bunch coriander, chopped", "1 egg", "100g fresh breadcrumbs",
        "1 medium red onion, ½ diced, ½ sliced", "1 tbsp olive oil", "small wholemeal buns",
        "1 large tomato, sliced, ½ cucumber, sliced and chilli sauce, to serve"],
    direction: ["STEP 1", "In a food processor, whizz the chickpeas, lemon zest, lemon juice, cumin, half the coriander, the egg and some seasoning. Scrape into a bowl and mix with 80g of the breadcrumbs and the diced onions. Form 4 burgers, press remaining breadcrumbs onto both sides and chill for at least 10 mins.",
        "STEP 2", "Heat the oil in a frying pan until hot. Fry the burgers for 4 mins each side, keeping the heat on medium so they don’t burn. To serve, slice each bun and fill with a slice of tomato, a burger, a few red onion slices, some cucumber slices, a dollop of chilli sauce and the remaining coriander."],
    letsCook() {
        console.log(`I'm hungry! Let's cook ${this.title}`);
    },

};
recipe2.letsCook();
</script>

