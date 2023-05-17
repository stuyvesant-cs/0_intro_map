# StuyCS Annual Intro Term 0

## Unit III Lists and Recursion

### Concepts
1. What is a data structure?
2. What is a linked list?
3. Using cons-cell diagrams.
4. Using recursion to work with lists.
5. Working with `map` `filter` and `reduce`

### Language Features
1. Literals
  - A data item that evaluates to itself
  - Examples: numbers, booleans, functions, strings
2. List
  - A sequential collection of data items that begins with '(' and ends with a ')'
  - A list is either empty or contains items
  - The length of a list is the number of items contained in the list
  - Examples:
    - `'()` <- the empty list
    - `'(1 2 3)`
3. Creating Lists
  - `(list)` -> '()
  - `(list 1 2 3)` -> '(1 2 3)
  - `(> 8 4 1)`
4. Built-in Predicate Functions Regarding Lists
    - `(list? x)` -> boolean where x is data. Evaluates to true if arg is a list
    - `(empty? x)` -> boolean where x is data. Evaluates to true if x is the empty list
    - `(atom? x)` -> boolean where x is data. Evaluates to true if x is not a list
5. car and cdr
  - `(car L)` -> data where L is a list. Evaluates to the first item in a list
    - Example: `(car ‘(a b c))` → a
  - `(cdr L)` -> list where L is a non-empty list. Evaluates to a list with the first data expression of L removed
    - Example: `(cdr ‘(a b c))` → '(b c)
6. cons
  - `(cons x L)` -> list where x is data and L is a list. Constructs a list by inserting x into the front of the list
  - Examples: 
    - `(cons 1 '(2 3))` → '(1 2 3)
    - `(cons 3 '())` → '(3)
    - `(cons (cons 1 '(2)) '(3) )` → '((1 2) 3)
7. Processing List Using Recursion
  - The general format to process a list:
    - If the list is empty: return an expression based on (car L)
    - Call the function again with (cdr L) to process to remaining list
  - Important to teach students how to trace their work.
  - For example, if (my-length L) -> Number where the result is the length of the list.
    - (my-length '(a b c))
      = (+ 1 (my-length '(b c)))
      = (+ 1 (+ 1 (my-length '(c))))
      = (+ 1 (+ 1 (+ 1 (my-length '()))))
      = (+ 1 (+ 1 (+ 1 0)))
      = (+ 1 (+ 1 1))
      = (+ 1 2)
      = 3
  - Lists can be processed in Racket using recursion.
  - Using list processing we can compute statistical information about our lists
  - Predicate list functions can tell us about the items contained in the list
  - Combining list processing with the cons function, we can create new lists that serve as map, filter, and reduce functions
