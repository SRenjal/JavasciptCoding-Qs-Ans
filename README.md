# Javascipt-Qs-Ans


###### 1. Write a JavaScript function that takes an array of objects as input, where each object contains key-value pairs. The function should return an object representing the cumulative sum of values for each unique key across all objects in the array.

###### Example Input:

javascript
Copy code
const inputArray = [
  { A: 4, B: 3 },
  { B: 6, C: 1 },
  { A: 5, C: 3 },
];

console.log(calculateCumulativeSum(inputArray));
Expected Output:

javascript
Copy code
// { A: 9, B: 9, C: 4 }
Constraints:

The input array may be empty or contain a variable number of objects.
Keys and values are non-negative integers.
The function should handle cases where a key is present in some objects but not in others.

<details><summary><b>Answer</b></summary>

  
```javascript

function calculateCumulativeSum(inputArray) {
  const result = {};

  inputArray.forEach((element) => {
    Object.keys(element).forEach((key) => {
      result[key] = (result[key] || 0) + element[key];
    });
  });

  return result;
}

// Example usage:
const inputArray = [
  { A: 4, B: 3 },
  { B: 6, C: 1 },
  { A: 5, C: 3 },
];

console.log(calculateCumulativeSum(inputArray));

```

</details>




###### 2. Finding Common Letters in Array Items in JavaScript

<details><summary><b>Answer</b></summary>

```javascript
const items = ["apple", "banana", "orange"];

// Function to find common letters among array items
function findCommonLetters(arr) {
    // Initialize an array to hold common letters
    let commonLetters = [];

    // Iterate through each character of the first item
    for (let letter of arr[0]) {
        // Check if this character exists in all other items
        if (arr.every(item => item.includes(letter))) {
            // If it does, and it's not already in the commonLetters array, add it
            if (!commonLetters.includes(letter)) {
                commonLetters.push(letter);
            }
        }
    }

    return commonLetters;
}

const commonLetters = findCommonLetters(items);

```

</detail>
console.log("Common letters:", commonLetters);

```
