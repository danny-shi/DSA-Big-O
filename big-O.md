## 1. What is Big O for this?

1. Determine the Big O for the following algorithm:
   You are sitting in a room with 15 people. You want to find a playmate for your dog, preferably of the same breed.
   So you want to know if anyone out of the 15 people have the same breed as your dog.
   You stand up and yell out, who here has a golden retriever and would like to be a playdate for my golden.
   Someone yells - "I do, be happy to bring him over"

- _Big O_: O(1), You are only selecting one person from the entire group.

2. Determine the Big O for the following algorithm:
   You are sitting in a room with 15 people. You want to find a playmate for your dog who is of the same breed.
   So you want to know if anyone out of the 15 people have the same breed as your dog.
   You start with the first person and ask him if he has a golden retriever.
   He says no, then you ask the next person, and the next, and the next until you find someone who has a golden or there is no one else to ask.

- **Big O**: O(n), You are iterating over each person in the group.

## 2. Even or odd?

What is the Big O of the following algorithm? Explain your answer

```
function isEven(value) {
  if (value % 2 === 0) {
    return true;
  } else {
    return false;
  }
}
```

**Big O**: O(1), You are checking the value exactly one time.

## 3. Are you here?

What is the Big O of the following algorithm? Explain your answer

```
function areYouHere(arr1, arr2) {
    for (let i = 0; i < arr1.length; i++) {
        const el1 = arr1[i];
        for (let j = 0; j < arr2.length; j++) {
            const el2 = arr2[j];
            if (el1 === el2) return true;
        }
    }
    return false;
}
```

**Big O**: O(n^2), Nested for loop.

## 4. Doubler

What is the Big O of the following algorithm? Explain your answer

```
function doubleArrayValues(array) {
    for (let i = 0; i < array.length; i++) {
        array[i] *= 2;
    }
    return array;
}
```

**Big O**: O(n), One iterative loop. Grows linearly with size of the array.

## 5. Naive Search

What is the Big O of the following algorithm? Explain your answer

```
function naiveSearch(array, item) {
    for (let i = 0; i < array.length; i++) {
        if (array[i] === item) {
            return i;
        }
    }
}
```

**Big O**: O(n), Linear search through array.

## 6. Creating pairs

What is the Big O of the following algorithm? Explain your answer

```
function createPairs(arr) {
    for (let i = 0; i < arr.length; i++) {
        for(let j = i + 1; j < arr.length; j++) {
            console.log(arr[i] + ", " +  arr[j] );
        }
    }
}
```

**Big O**: O(n^2), Nested for loop.

## 7. Compute the sequence

What does the following algorithm do? What is its runtime complexity? Explain your answer

```
function compute(num) {
    let result = [];
    for (let i = 1; i <= num; i++) {

        if (i === 1) {
            result.push(0);
        }
        else if (i === 2) {
            result.push(1);
        }
        else {
            result.push(result[i - 2] + result[i - 3]);
        }
    }
    return result;
}
```

_Algorithm_: Loop linearly through the result array. On the first iteration, push 0 to the array. Push 1 to the array on the second iteration. Afterwards, it pushes the next value in the fibonacci sequence.

_Runtime complexity_: O(n)
