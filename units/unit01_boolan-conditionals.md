# StuyCS Annual Intro Term 0

## Unit II: Boolean Values and Conditional Statements

### Concepts
1. What are Boolean values?
2. How do comparison operators work?
3. What are Boolean operators?
4. Using functions that return Boolean values.
5. Using `if`.
6. Using `cond`.

### Language Features
1. Boolean values
  - `true false` also `#t #f`
2. Comparison operators
  - `= > < >= <=`
  - note that not equals is not a basic comparison operator
  - `(COMP ARG0 ARG1 ARG2 ...)`
  - `(= 4 5)`
  - `(> 8 4 1)`
  - Is using more than one argument, you can think of it as using the provided operator between each argument.
    - Example above would mean 8 > 4 > 2
3. Boolean operators
  - `and or not`
  - `(and BOOL0 BOOL1 BOOL2 ...)`
  - `not` can only take 1 argument.
4. Using `if`
  - Keep in mind `if` is a function, that takes 3 arguments and returns a value.
  - ```racket
    (if BOOLEAN
        RETURN IF TRUE
        RETURN IF FALSE)
    ```
  - ```racket
    (if (< a 10)
        0
        10)
    ```
  - You can leave out the second result (if the boolean is `false`), but then the function will not always return a value.
4. Using `cond`
  - Each argument to `cond` is a boolean value (usually a function returning a boolean value) with an attached return value.
  - The return value connected to the first boolean value that is `true` will be returned, and the rest of the `cond` function will be ignored.
  - If NO boolean value is `true`, the function will not return anything.
  - You can connect as many boolean/return pairs as you need.
  - You _can_ use `else` in place of the _last boolean value only_. If `else` is present, then the return value attached to the `else` will be returned in the event that all the previous boolean values are `false`.
  - `else` is not required, but if used, it must be in the last boolean/return pair.
  - ```racket
    (cond
      ( BOOL0 RESULT0 )
      ( BOOL1 RESULT1 )
      ( BOOL2 RESULT2 )
      ...
      ( else DEFAULT RESULT)
    )
    ```
  - ```racket
    (cond
      ( (> a 200) 200 )
      ( (> a 100) 100 )
      ( (> a 0) 0 )
      ( else -1)
    )
