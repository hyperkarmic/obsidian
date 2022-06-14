# callback
***This explains req/res err/data......argument structure.***

# Parameters Of A Callback Function

Since callback functions are called asynchronously and can neither supply a direct return value nor throw errors, appropriate parameters should be provided for at least these two cases:

1.  one parameter that contains information about the error that occurred in the event of an error,
2.  one parameter that normally contains the result of the asynchronous calculation.

Even if the order of these two parameters does not matter in principle, it has become a convention — especially when developing Node.js modules — to list the error as the first parameter and the result as the second parameter (if there is no error, the first parameters corresponding to zero).

#callback
#js #javascript 