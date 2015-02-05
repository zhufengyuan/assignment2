# assignment2
code for Caching the Inverse of a Matrix

makeCacheMatrix <- function(x = matrix()) {
elc <- NULL
set <- function(y) {
x <<- y
elc <<- NULL
}
get <- function() x
setinverse <- function(inverse) elc <<-inverse
getinverse <- function() elc
list(set = set, get = get,
setinverse = setinverse,
getinverse = getinverse)

}

cacheSolve <- function(x, ...) {
elc <- x$getinverse()
if(!is.null(elc)) {
message("getting cached data")
return(el)
}
data <- x$get()
elc <- Solve(data, ...)
x$setinverse(elc)
elc
}

