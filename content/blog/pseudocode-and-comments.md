---
title: Pseudocode & Comments
description: Pseudocode & Comments
date: 2023-08-20
tags:
  - Pseudocode & Comments
---
```js
// *** FixStart ***
// --- Problem ---
// Create a FUNCTION modify input string argument
// Return  occurrences of its first character with * expect first character


// --- Solution ---
// Create a Function named fixStart with single parameter
// Create a variable to store the first character if the input string
// Create a variable to store input string replaced with *
// FOR loop through the input string 
// Check IF any character is same as the the first character, but ignore the first character 
// Append ever single character from the input string into a newly created variable
// RETURN the newly created variable

// --- Code ---
function FixStart(word) {
    const firstChar = word[0];
    let newWord = "";

    for (let i = 0; i < word.length; i++) {
        if (word[i] === firstChar && i !== 0) {
            newWord += "*";
        }
        else {
            newWord += word[i];
        }
    }
    return newWord;
}

console.log(FixStart("turtle"));
```
<script>
// *** FixStart ***
// --- Problem ---
// Create a FUNCTION modify input string argument
// Return  occurrences of its first character with * expect first character


// --- Solution ---
// Create a Function named fixStart with single parameter
// Create a variable to store the first character if the input string
// Create a variable to store input string replaced with *
// FOR loop through the input string 
// Check IF any character is same as the the first character, but ignore the first character 
// Append ever single character from the input string into a newly created variable
// RETURN the newly created variable

// --- Code ---
function FixStart(word) {
    const firstChar = word[0];
    let newWord = "";

    for (let i = 0; i < word.length; i++) {
        if (word[i] === firstChar && i !== 0) {
            newWord += "*";
        }
        else {
            newWord += word[i];
        }
    }
    return newWord;
}

console.log(FixStart("turtle"));
</script>

