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