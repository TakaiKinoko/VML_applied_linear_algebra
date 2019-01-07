## Linear functions

#### function notation
* **f: R<sup>n</sup> -> R** means:  f is a function that maps R<sup>n</sup> to R, 

* f can also be interpretted as a function of n scalar arguments: 
    f(x) = f(x<sub>1</sub>,x<sub>2</sub>, ..., x<sub>n</sub>)

* e.g. 
    f(x) = x<sub>1</sub> + x<sub>2</sub> - x<sub>4</sub><sup>2</sup> 
    is a function f: R<sup>4</sup>-> R

#### inner product function
* suppose a is an n-vector, f(x) = a<sup>T</sup>x = a<sub>1</sub>x<sub>1</sub>, a<sub>2</sub>x<sub>2</sub>, ..., a<sub>n</sub>x<sub>n</sub> 

* f can be thought of as forming a weighted sum of the elements of x 

#### superposition and linearity
* **superposition equality**: f(αx + βy) = αf(x) + βf(y)
* the inner product function satisfy the **superposition** property, thus it is **linear**. 
* superposition equality: on the left-hand side, the term αx + βy involves scalar-vector multiplication and vector addition. On the right-hand side, αf(x) + βf(y) involves ordinary scalar multiplication and scalar addition.
* if a function is linear, superposition extends to linear combinations of any number of vectors, not just two. 
* **another presentation of superposition**
    1. Homogeneity. For any n-vector x and any scalar α, f(αx) = αf(x)
    1. Additivity. For any n-vectors x and y, f(x + y) = f(x) + f(y)
* Homogeneity states that scaling the (vector) argument is the same as scaling the function value; additivity says that adding (vector) arguments is the same as adding the function values.

#### represent a linear function as inner product 
* If a function is linear, then it can be expressed as the inner product of its argument with some fixed vector.
* Suppose f is a scalar-valued function of n-vectors, and is linear, then *there is an n-vector a such that f(x) = a<sup>T</sup>x for all x*, where a<sup>T</sup>x is the **inner product representation of f**
* e.g. f(x) = f(x<sub>1</sub>e<sub>1</sub>, x<sub>2</sub>e<sub>2</sub>, ..., x<sub>n</sub>e<sub>n</sub>) 
    = x<sub>1</sub>f(e<sub>1</sub>) + x<sub>2</sub>f(e<sub>2</sub>) + ... + x<sub>n</sub>f(e<sub>n</sub>) 
    = a<sup>T</sup>x