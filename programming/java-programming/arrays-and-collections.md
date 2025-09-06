# Arrays and Collections

*In this lesson we will go over arrays and important collections including ArrayLists, Stacks, and Queues.*

---

### Elements
**Definition**: An element is the value stored at a particular position within an _array_.  
> **Example**: Suppose an array of integers: [5,3,2,6], The 2nd element (index 1) in the array is 3.

---

### Arrays
**Definition**: An array is a fixed-size, ordered collection of _elements_ of the same type stored in contiguous memory locations.

> **Example**
> ```java
> int[] scores = {95, 87, 74, 100};
> System.out.println(scores[2]); // prints 74
> scores[2] = 80; // update the third element
> System.out.println(scores[2]); // prints 80
> System.out.println(scores.length); // prints 4
> ```

**Key Characteristics**:
- **Fixed Size**: Once created, the length of an array cannot be changed.
- **Indexed Access**: Elements are accessed using a zero-based index (Indices start at 0).
- **Homogeneous Data**: All elements must be of the same data type.
- **Direct Lookup**: Java can access any element immediately using its index.

> [!WARNING]  
> Accessing an index outside the valid range (`0` to `array.length - 1`) will cause a  
> `ArrayIndexOutOfBoundsException`.  
>
> **Example**:
> ```java
> int[] numbers = {1, 2, 3};
> System.out.println(numbers[3]); // ERROR: valid indices are 0,1,2
> ```

---

### Collections
> [!NOTE]  
> Collections in Java are dynamic data structures that can grow or shrink in size, unlike arrays which have a fixed length. They are part of the **Java Collections Framework (JCF)**, which provides a set of interfaces and classes for storing and manipulating groups of objects. However, even though most of these are beyond the scope of this lesson, learning them is encouraged.

**Main Interfaces in JCF**:
- **List**: Ordered, allows duplicates (e.g., `ArrayList`, `LinkedList`).
- **Set**: Unordered, unique elements only (e.g., `HashSet`, `TreeSet`).
- **Queue**: Ordered for processing, typically FIFO (e.g., `LinkedList`, `PriorityQueue`, `ArrayDeque`).
- **Map**: Key-value pairs (e.g., `HashMap`, `TreeMap`, `LinkedHashMap`).

**Diagram Placeholder:** *(Java Collections Framework hierarchy diagram)*

---

### ArrayList
```java
import java.util.ArrayList;

ArrayList<String> names = new ArrayList<>();
names.add("Alice");
names.add("Bob");
names.add("Charlie");

System.out.println(names.get(1)); // prints Bob
names.remove("Alice"); // removes Alice
System.out.println(names); // prints [Bob, Charlie]
```

**What it is**
- A list that behaves like a flexible array. You can add or remove items and the list adjusts its size for you.
- Keeps items in the order you insert them.

**Core operations you’ll use a lot**
- `add(item)`, `add(index, item)`: put items in the list.
- `get(index)`: read an item by its position.
- `set(index, item)`: replace an item at a position.
- `remove(index)` / `remove(object)`: delete by position or by value.
- `size()`: how many items are in the list.

**When to use it**
- You want a list of things that you’ll read by their position (first, second, third…).
- You don’t know the final amount of items up front.
- You care about keeping the original insertion order.

**Mini‑exercise**
- Make a list of three favorite movies. Replace the second one, then remove the last one.

---

### Stack
> [!TIP]  
> A `Stack` follows the **LIFO (Last In, First Out)** rule. Think of a stack of plates; the last plate placed is the first one taken off.

```java
import java.util.Stack;

Stack<Integer> stack = new Stack<>();
stack.push(10);
stack.push(20);
stack.push(30);

System.out.println(stack.pop()); // prints 30
System.out.println(stack.peek()); // prints 20
```

**What it is**
- A container that lets you work with the top item only.
- Great for “undo” features, backtracking, and processing nested structures (like matching parentheses).

**Core operations**
- `push(item)`: put an item on top.
- `pop()`: take the top item off and return it.
- `peek()`: look at the top item without removing it.
- `isEmpty()`: check if there are any items.

**When to use it**
- You need to reverse a recent action or remember a path of steps.
- You’re parsing expressions or checking for balanced brackets.

**Mini‑exercise**
- Push three integers. Pop once. What’s left on top?

---

### Queue
> [!TIP]  
> A `Queue` follows the **FIFO (First In, First Out)** rule. Think of a line at the grocery store; the first person in line is the first one served.

```java
import java.util.LinkedList;
import java.util.Queue;

Queue<String> queue = new LinkedList<>();
queue.add("first");
queue.add("second");
queue.add("third");

System.out.println(queue.poll()); // prints "first"
System.out.println(queue.peek()); // prints "second"
```

**What it is**
- A line of items where you add to the back and take from the front.
- Helpful whenever tasks must be handled in the order they arrive.

**Core operations**
- `add(item)` / `offer(item)`: put an item at the back.
- `remove()` / `poll()`: take the front item (use `poll()` to avoid exceptions when empty).
- `peek()`: look at the front item.
- `isEmpty()`: check if there are any items.

**When to use it**
- Processing tasks or jobs in arrival order (printing, requests, customer service tickets).
- Breadth‑first search in graphs and trees.

**Mini‑exercise**
- Enqueue three strings, dequeue one, then check which string is at the front.

---

## Summary

- Use **ArrayList** for lists that need to resize automatically.  
- Use **Stack** when you need LIFO behavior.  
- Use **Queue** when you need FIFO behavior.  
- Arrays are still useful when working with a fixed number of elements.

---