---
title: Function and Control Flow
description: Function and Control Flow
date: 2023-08-13
tags:
  - Function and Control Flow!
---
```js
//Combine first name and last name
function name(firstName, lastName) {
return `Hello ${firstName} ${lastName}`;
}

document.write(`${name("weizhi", "xie")}`);

//Temperature control flow 
const temperature = 0;
if (temperature <= 0) {
    document.write("Stay inside.");
}
else if (temperature <= 30) {
    document.write("Wear a coat and a hat");
}
else if (temperature <= 50) {
    document.write("Put on a coat");
}
else {
    document.write("Just pants and vest is fine");
}
```

<script>
    function name(firstName, lastName) {
        return `Hello ${firstName} ${lastName}`;
    }
    document.write(`${name("Weizhi", "Xie")} `);

    const temperature = 50;
    if (temperature <= 0) {
        document.write("Stay inside.");
    }
    else if (temperature <= 30) {
        document.write("Wear a coat and a hat");
    }
    else if (temperature <= 50) {
        document.write("Put on a coat");
    }
    else {
        document.write("Just pants and vest is fine");
    }
</script>