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
    with a = (f(e<sub>1</sub>), f(e<sub>2</sub>), ... ,f(e<sub>n</sub>) 

* The representation of a linear function f as f (x) = a<sup>T</sup>x is **unique**, which means that there is only one vector a for which f (x) = a<sup>T</sup>x holds for all x

#### examples 
* mean value of an n-vector: 
    f(x) = (x1 + x2 + ... + xn)/n
         = a<sup>T</sup>x with a = (1/n, ..., 1/n) = **1**/n
* maximum: 
    The maximum element of an n-vector x, f (x) = max{x1 , . . . , xn }, is not a linear function (except when n = 1).

#### affine functions 
* A linear function plus a constant is called an affine function.
* f: R<sup>n</sup> -> R is affine iff it can be expressed as **f(x) = a<sup>T</sup>x + b**
* e.g. f(x) = 2.3 - 2x1 + 1.3x2 - x3 is affine, with b = 2.3, a = (-2, 1.3, -1)
* superposition holds for affine functions when the coefficients sum to one (i.e., when the argument is an affine combination)


## Taylor approximation
#### when to use
In many applications, scalar-valued functions of n variables, or relations between n variables and a scalar one, can be **approximated** as linear or affine functions, which are called a **model**

![Taylor approximation](/taylor.png)