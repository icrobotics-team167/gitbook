# Loops and Recursion

*In this lesson we will go over **loops** and **recursion**, two fundamental ways to repeat instructions in Java.*

---

## For Loop
**What it is**: A counter‑controlled loop. You set a start value, a stop condition, and how the counter changes each time.

**Pattern**:
```java
for (initialization; condition; update) {
    // repeated code
}
```

**Example: Count 1 to 5**
```java
for (int i = 1; i <= 5; i++) {
    System.out.println(i);
}
```

**Example: Sum the first N numbers**
```java
int n = 10;
int sum = 0;
for (int i = 1; i <= n; i++) {
    sum += i;
}
System.out.println("Sum = " + sum); // 55
```

**Mini‑exercise**
- Print all multiples of 3 from 3 to 30.

>[!WARNING]  **Common mistakes**
> - Off‑by‑one errors (`i < n` vs `i <= n`).
> - Forgetting the update step and creating an infinite loop.

---

## While Loop
**What it is**: A condition‑controlled loop. It keeps running **while** a condition is true.

**Pattern**:
```java
while (condition) {
    // repeated code
}
```

**Example: Guessing game skeleton**
```java
int secret = 7;
int guess = -1;
java.util.Scanner sc = new java.util.Scanner(System.in);
while (guess != secret) {
    System.out.print("Guess: ");
    guess = sc.nextInt();
}
System.out.println("Correct!");
```

**Mini‑exercise**
- Starting from 50, keep subtracting 7 and print the value **while** it remains non‑negative.

>[!WARNING]  **Common mistakes**
> - Forgetting to change the variables used in the condition → infinite loop.
> - Checking the wrong condition (e.g., `==` vs `.equals` for strings).

---

## Enhanced For‑Each Loop
**What it is**: A simple way to loop over **arrays** and **collections** without using an index.

**Pattern**:
```java
for (ElementType item : collectionOrArray) {
    // use item
}
```

**Example: Array**
```java
String[] fruits = {"Apple", "Banana", "Cherry"};
for (String fruit : fruits) {
    System.out.println(fruit);
}
```

**Example: ArrayList**
```java
java.util.List<Integer> nums = java.util.Arrays.asList(2, 4, 6, 8);
for (int n : nums) {
    System.out.println(n);
}
```

**When to use**
- You want to visit every item in order and you **don’t** need the index.

**Mini‑exercise**
- Given `int[] a = {5, 1, 5, 2};` print each element on one line using a for‑each loop.

>[!WARNING]  **Common mistakes**
> - Trying to modify the collection’s structure (add/remove) while iterating.
> - Needing the index but using for‑each; in that case, prefer a classic `for`.

---

### Recursion

**Definition**: Recursion is when a method calls itself to solve a smaller version of the same problem until a base condition is reached.

**Key Concepts**:
- **Base Case**: The stopping condition that ends the recursion.
- **Recursive Case**: The part where the method calls itself with a simpler/smaller input.

**Example Recursive Factorial Function**
```java
int factorial(int n) {
	if (n == 0) { // base case
		return 1;
	} else {
		return n * factorial(n - 1); // recursive case
	}
}
```  

**How it works** for `factorial(3)`:
1. `factorial(3)`
2. → 3 * `factorial(2)`
3. → 3 * (2 * `factorial(1)`)
4. → 3 * (2 * (1 * `factorial(0)`))
5. → 3 * (2 * (1 * (1)))
6. → **6**

**When to use recursion**:
- Problems that can be broken down into smaller, similar subproblems.
- Examples: factorial, Fibonacci numbers, traversing trees, depth-first search.

**Mini-exercise**:
- Write a recursive function to calculate the sum of numbers from 1 to `n`.

---