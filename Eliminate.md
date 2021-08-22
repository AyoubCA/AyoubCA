from numpy import *
def enter():
    while True:
        n = int(input('enter n : '))      # n represent the number of cases 
        if 5 <= n <= 30:
            break
    return(n)


def fill(n):
    t = array([''] * n, str)
    for i in range(n):
        t[i] = input('t[ ' + str(i)+ '] = ')
    return(t)


def eliminate(t, n):                          #this fuction elimanates numbers and special lettres 
    for i in range(n):
        ch = ''
        for j in range(len(t[i])):
            if 'A' < t[i][j].upper() <= 'Z':         
                ch += t[i][j]
        t[i] = ch
    return(t)


def display(t, n):
    for i in range(n):
        print(t[i], end = ' ')


n = enter()
t = fill(n)
t = eliminate(t, n)
display(t, n)
