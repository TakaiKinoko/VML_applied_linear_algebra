### Julia language features
1. assignment vs. copy
    * the assignment operator passes the reference of the right-hand right to the left-hand side.  
    * to create a new copy of a vector, use copy()

1. equality test
    * ==

1. blocked (stacked) vector
    * mathematical notation: [x; y] -- stack x y together
    * julia: 
    ```
    vcat(x, y)
    ```
     -- create a new vector 
    * pitfall: neither of these below creates stack vectors: 
    ```
    z = (x, y)  #creates a tuple of the two vetors
    ```
    ```
    z = [x, y]  #creates an array of the two vectors
    ```