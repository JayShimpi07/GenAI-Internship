# Understanding Stacks in Python with Real-World Examples

A practical guide to implementing stacks in Python with real-world applications and time complexity analysis.

---

## What is a Stack?

A **Stack** is a linear data structure that follows the principle of:

**LIFO (Last In, First Out)**

This means the last element inserted into the stack is the first one to be removed.

### Example Visualization

```
Top
|  30
|  20
|  10
```

If we remove an element, 30 will be removed first.

---

## Core Stack Operations

- **Push** – Add an element to the top  
- **Pop** – Remove the top element  
- **Peek** – View the top element  
- **isEmpty** – Check if the stack is empty  

---

## Implementing Stack in Python

### Method 1: Using List

```python
stack = []

# Push elements
stack.append(10)
stack.append(20)
stack.append(30)

print("Stack after push:", stack)

# Pop element
stack.pop()
print("Stack after pop:", stack)

# Peek element
print("Top element:", stack[-1])
```

---

### Method 2: Using collections.deque

```python
from collections import deque

stack = deque()

stack.append(10)
stack.append(20)
stack.append(30)

print("Stack:", stack)

stack.pop()
print("After pop:", stack)
```

---

## Real-World Applications

### 1. Undo/Redo Functionality

```python
actions = []

actions.append("Typed Hello")
actions.append("Added !")
actions.append("Deleted word")

print("Last action:", actions[-1])

actions.pop()
print("After undo:", actions)
```

---

### 2. Browser Back Button

```python
browser_stack = []

browser_stack.append("google.com")
browser_stack.append("youtube.com")
browser_stack.append("linkedin.com")

print("Current Page:", browser_stack[-1])

browser_stack.pop()
print("After Back:", browser_stack[-1])
```

---

### 3. Balanced Parentheses Checking

```python
def is_balanced(expression):
    stack = []
    
    for char in expression:
        if char == '(':
            stack.append(char)
        elif char == ')':
            if not stack:
                return False
            stack.pop()
    
    return len(stack) == 0

print(is_balanced("(())"))
print(is_balanced("(()"))
```

---

## Time Complexity

| Operation | Time Complexity |
|-----------|-----------------|
| Push      | O(1)            |
| Pop       | O(1)            |
| Peek      | O(1)            |
| Search    | O(n)            |

---

## Conclusion

Stacks are foundational to many real-world systems such as undo mechanisms, browser navigation, and expression evaluation.

Understanding stacks strengthens your core data structure knowledge and builds a strong base for advanced algorithms.
