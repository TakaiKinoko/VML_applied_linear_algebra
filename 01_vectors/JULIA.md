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
