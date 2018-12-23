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
1. If a1 , ... , am are n-vectors, and β1 , . . . , βm are scalars, the n-vector
    ```
    β1a1 +···+βmam
    ```
    is called a linear combination of the vectors a1,..., an. The scalars β1,..., βm are
    called the coefficients of the linear combination.

1. any n-vector b can be written as a linear combination of unit vectors, as 
    ```
    b = b1e1 + b2e2 + ... + bnen
    ```
    in which bi is the ith entry of b, ei is the ith unit vector.
1. **special** linear combinations
    * **sum** the linear combination with β1 = · · · = βm = 1, given by a1 + · · · + am , is the sum of the vectors
    * **average** the linear combination with β1 = ··· = βm = 1/m, given by (1/m)(a1 +···+am), is the average of the vectors
    * **affine combination** When the coefficients sum to one, i.e., β1 + · · · + βm = 1, the linear combination is called an affine combination
    * **convex combination/weighted average/mixture** When the coefficients in an affine combination are nonnegative

### convex combination
* https://en.wikipedia.org/wiki/Convex_combination
* When a and b are different n-vectors, the affine combination c = (1 − θ)a + θb, where θ is a scalar, describes a point on the line passing through a and b. When 0 ≤ θ ≤ 1, c is a convex combination of a and b,and is said to lie on the segment between a and b.