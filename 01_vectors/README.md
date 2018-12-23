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

### inner product
1. one of the properties: 
    (a + b)<sup>T</sup>(c + d) = a<sup>T</sup>c + a <sup>T</sup> d + b <sup>T</sup>c + b <sup>T</sup> d
    
1. 
    * Unit vector: e<sub>i</sub><sup>T</sup>a = a<sub>i</sub>
    * Sum: 1<sup>T</sup>a = a<sub>1</sub> + ... + a<sub>n</sub>
    * Average: (1/n)<sup>T</sup>a = (a<sub>1</sub> + ... + a<sub>n</sub>)/n
    * Sum of squares: a<sup>T</sup> a = a<sub>1</sub>^2 + ... + a<sub>n</sub>^2
    * Selective sum: b is a bit mask, b<sub>T</sub>a is the sum of the elements in a which b<sub>i</sub> = 1

1. inner product of block vectors
    If the vectors a and b are block vectors, and the correspoinding blocks have the same sizes (that they *conform*), then we have 
    a<sup>T</sup>b = a<sub>1</sub><sup>T</sup>b<sub>1</sub> + ... + a<sub>k</sub><sup>T</sup>  (where a<sub>i</sub>, b<sub>i</sub> are vectors themselves)

### Julia language features
1. assignment vs. copy
    * the assignment operator passes the reference of the right-hand right to the left-hand side.  
    * to create a new copy of a vector, use copy()

1. equality test
    * ==

1. blocked (stacked) vector
    * mathematical notation: [x; y] -- stack x y together
    * julia: 
    1. 
        ```
        vcat(x, y)
        ```
        -- create a new vector 
    1. 
        ```
        x = [1, -2]; y = [1, 1, 0]
        z = [x; y]
        ```
    * pitfall: neither of these below creates stack vectors: 
    ```
    z = (x, y)  #creates a tuple of the two vetors
    ```
    ```
    z = [x, y]  #creates an array of the two vectors
    ```
1. Average of the entries
    * 
        ```
        avg(a)
        ```
        computes (1/n)<sup>T</sup>a = (a<sub>1</sub> + ... + a<sub>n</sub>)/n 

1. slicing (subvector)
    * slicing into a vector
        ```
        x = [1, 2, 3, 4, 5]
        y = x[2:4]
        ```
    * partial reassginment 
        ```
        x[4:5] = [-4, -5]
        ```
1. indexing into arrays
    1. **stride** 
        * syntax
        ```
        x[<start>:<stride>:<end>]
        ```
        * examples
        ```
        x =[1,2,3,4,5,6,7,8,9]
        y = x[2:2:8]  # y=[2,4,6,8]
        ```
        ```
        x = [1,0,0,-2,2]
        y = x[2:2:end]  #using keyword end  y = [0, -2]
        ```
    1. backward indexing  **reverse**
        ```
        z[end:-1:1]   # gives the reverse of vetor z
        ```
