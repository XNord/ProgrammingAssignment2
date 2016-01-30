### Programming Assignment 2: Caching the Inverse of a Matrix

File 'cachematrix.R' contains following functions:

1.  `makeCacheMatrix`: Creates a special "matrix" object
    that can cache its inverse.
2.  `cacheSolve`: Computes the inverse of the special
    "matrix" returned by `makeCacheMatrix` above. If the inverse has
    already been calculated (and the matrix has not changed), then
    `cacheSolve` should retrieve the inverse from the cache.

Note: It is assumed that the matrix supplied is always invertible.

### Example code: Caching an inverse of a large matrix

n <- 1000
mtx <- matrix(rnorm(n*n),n,n)
cache <- makeCacheMatrix(mtx)

## Run twice to see difference in time used
t1 <- Sys.time()
mtx.inverse <- cacheSolve(cache)
t2 <- Sys.time()
t2-t1