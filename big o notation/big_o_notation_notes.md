# Big O Notation

Big O is known in full as big o asymptotic analysis
any coder given enough time can solve a problem what matters is how well the problem is solved


## What is good code?
- Readable
- Scalable

## Big O and Scalability

This deals with how long an algorithm takes to run regardless of ccomputer differences.
So we look how elements/inputs increases how many operations we will need to run.
Different functions have different big o complexities.

## O(n) --> Linear Time

This occurs when the number of operations is directly proportional to the number of inputs,
where n stands for the number of inputs, a single forloop works with linear time.

## O(1) --> Constant Time

No matter the number of operations the time will remain the same, like when you have to pull out a constant set of items from an array no matter how large the array is. It is the most Scalable, very excellent and predictable.

## What is the big o of the function below?

```
function funChallenge(input) {
  let a = 10; // O(1)
  a = 50 + 3; // O(1)

  for (let i = 0; i < input.length; i++) { // O(n)
    anotherFunction(); // O(n)
    let stranger = true; // O(n)
    a++; // O(n)
  }
  return a; // O(1)
}
```
> Answer: 
``` 
O(1) + O(1) + O(1) + O(n) + O(n) + O(n) + O(n)
BIG O(3 + 4n)
```

```
function anotherFunChallenge(input) {
  let a = 5; // O(1)
  let b = 10; // O(1)
  let c = 50; // O(1)
  for (let i = 0; i < input; i++) { // O(n)
    let x = i + 1; // O(n)
    let y = i + 2; // O(n)
    let z = i + 3; // O(n)

  }
  for (let j = 0; j < input; j++) { // O(n)
    let p = j * 2; // O(n)
    let q = j * 2;// O(n)
  }
  let whoAmI = "I don't know"; // O(1)
}

```

> Answer: 
```
 BIG O(4 + 7n)
```

## O(n^2) --> Quadratic Time

When you see nested loops we see multiplication, which results in exponentials, the number of loops will determine the number of exponents. Quadratic time is horrible espectially for large inputs in wich the time rises quickly.

## O(n!) --> Factorial Time

You may not encountered it and if you do then youare doing something wrong, it means you are adding a loop for every element you are iterating over.

## Simplifying Big O

### Rules of Big O Notation

* **Worst Case**

When calculating Big O we always thing of the worst case scenario, how things will be when it scale up.

* **Remove Constants**

Here we also ignore variable assignments and small calculations
so things like O(2n), O(n + 1) becomes O(n)

* **Different terms for input**

When there are different inputs i.e parameters in a function, the big O an addition based on the number of inputs. So if we have three parameters in a function the big O will be O(a + b + c), since each of the parameters may contain different number of values and ifthere are loops, the loops are not nested. 
If the loops are nested the big O will be big O(a * b)

* **Drop Non Dorminants**

Look at the one that is larger, take it and drop the lower one so O(n + n^2) will become O(n^2)


## 3 Layers of  Programming
When we sy scalable we consider two things
- Readable: clean, maintainable code that others can read.
- Scalable
..- Speed: Has an efficient big O time complexity
..- Memory: What is the space complexity(memory usage of code)

Note that their is usaully a tradeoff between time complexity and space complexity.

## Space Complexity

When a programme execute their are two ways to remember things the heap and the stack, the heap is where we store variable that we assign and the stack is where we keep function calls

What causes space complexity? 
- Variables
- Function calls
- Data Structures
- Allocations

