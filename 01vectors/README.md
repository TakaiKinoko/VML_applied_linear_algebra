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

### linear combination
1. any n-vector b can be written as a linear combination of unit vectors, as 
    ```
    b = b1e1 + b2e2 + ... + bnen
    ```
    in which bi is the ith entry of b, ei is the ith unit vector.