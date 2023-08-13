---
title: Tip Calculator
description: Tip Calculator
date: 2023-08-12
tags:
  - Tip Calculator!
---
```js
const total = 100;
const tipPercentage = 30;
const totalWithTip = total + (total / 100 * tipPercentage)

document.write(`Your total bill, with tip, is £${totalWithTip.toFixed(2)}`);

//tipCalculator function
function tipCalculator(total, tipPercentage)
{
    const totalWithTip = total + (total / 100 * tipPercentage)
    return totalWithTip.toFixed(2);
}

document.write(`Your total bill, with tip, is £${tipCalculator(100, 30)}`);
```

<script>
    function tipCalculator(total, tipPercentage)
    {
        const totalWithTip = total + (total / 100 * tipPercentage)
        return totalWithTip.toFixed(2);
    }

    document.write(`Your total bill, with tip, is £${tipCalculator(100, 30)}`);
</script>