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



from timeit import default_timer as timer
def hanoi(n):
    if n == 1:
        count = 1
    else:
        count = (2 * hanoi(n - 1) + 1)
    return count


def ToH(n, A, B, C):
    if n == 1:
        print("Mover Disco 1 desde ", A, "a", B)
        return
    ToH(n - 1, A, C, B)
    print("Mover Disco ", n, " desde ", A, "a", B)
    ToH(n - 1, C, B, A)


def main():
    n = eval(input("Introduzca el número total de discos de la Torre de Hanói:"))
    print("{} os discos deben moverse: {} veces".format(n, hanoi(n)))
    ToH(n, 'A', 'B', 'C')


start = timer()
if __name__ == "__main__":
    main()
end = timer()
delay = end - start
print("EL tiempo transcurrido es {} ".format(delay))