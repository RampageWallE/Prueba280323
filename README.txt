//PROBLEMA 1 

from timeit import default_timer as timer

def factorial(n):
    if n == 0:
        return 1
    else:
        return n*factorial(n-1)
start = timer()
print(factorial(998))
end = timer()
delay = end - start
print("EL TIEMPO TRANSCURRIDO ES DE: {}".format(delay))


//PROBLEMA 2 
