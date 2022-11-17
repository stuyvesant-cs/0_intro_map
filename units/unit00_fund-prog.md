# StuyCS Annual Intro Term 0

## Unit I: Fundamentals of Programming

### Concepts
1. The purpose of programming languages
2. Syntax vs Semantics
3. Calling functions
4. Algorithms
5. Creating functions
   - Parameters vs Arguments
6. Anonymous functions
7. Identifiers

### Language Features
1. Basic prefix notation
    - `( OPERATOR OPERANDS )`
    - `(+ 3 7)`
2. Using provided functions
   - `(sqrt 16)`
   - `(max 7 238 3)`
3. Chaining functions.
   - `(+ (sqrt 16) (max 7 238 3))`
4. Creating anonymous functions
    - ```racket
      ( (lambda
           (PAREMETER LIST)
           (FUNCTON BODY)
        )
        ARGUMENTS
      )
      ```
     - ```racket
       ( (lambda
            (a b)
            (+ a b)
         )
         3 7
       )
       ```
5. Using `define`
    - `(define IDENTIFIER VALUE)`
    - For single values
      - `(define PI 3.14)`
    - For anonymous functions
      - ```racket
        (define myFunc
          (lambda (a b)
            (+ a b)
          )
        )
        ```
      - Usage: `(myfunc 3 5)`
