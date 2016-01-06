# week4_Ridge_Regression
Ridge regression, is the most commonly used method of regularization of ill-posed problems. In statistics, the method is known as Tikhonov regularization, named for Andrey Tikhonov.
When the following problem is not well posed (either because of non-existence or non-uniqueness of x)

    A\mathbf {x} =\mathbf {b} , 
    
then the standard approach (known as ordinary least squares) leads to an overdetermined (Over-fitted), or more often an underdetermined (under-fitted) system of equations. Most real-world phenomena operate as low-pass filters in the forward direction where A maps \mathbf {x} to \mathbf {b} . Therefore in solving the inverse-problem, the inverse mapping operates as a high-pass filter that has the undesirable tendency of amplifying noise (eigenvalues / singular values are largest in the reverse mapping where they were smallest in the forward mapping). In addition, ordinary least squares implicitly nullifies every element of the reconstructed version of \mathbf {x} that is in the null-space of A, rather than allowing for a model to be used as a prior for \mathbf {x} . Ordinary least squares seeks to minimize the sum of squared residuals, which can be compactly written as

    \|A\mathbf {x} -\mathbf {b} \|^{2}

where \left\|\cdot \right\| is the Euclidean norm. In order to give preference to a particular solution with desirable properties, a regularization term can be included in this minimization:

    \|A\mathbf {x} -\mathbf {b} \|^{2}+\|\Gamma \mathbf {x} \|^{2}

for some suitably chosen Tikhonov matrix, \Gamma . In many cases, this matrix is chosen as a multiple of the identity matrix (\Gamma =\alpha I), giving preference to solutions with smaller norms; this is known as L2 regularization.[1] In other cases, lowpass operators (e.g., a difference operator or a weighted Fourier operator) may be used to enforce smoothness if the underlying vector is believed to be mostly continuous. This regularization improves the conditioning of the problem, thus enabling a direct numerical solution. An explicit solution, denoted by {\hat {x}}, is given by:

    {\hat {x}}=(A^{T}A+\Gamma ^{T}\Gamma )^{-1}A^{T}\mathbf {b} 

The effect of regularization may be varied via the scale of matrix \Gamma . For \Gamma =0 this reduces to the unregularized least squares solution provided that (ATA)−1 exists.
