# -Fin-Divisibility
Given a positive integer n, find out if there exists an integer k such that the kth Fibonacci number is divisible by n. If such a k exists, return it. Otherwise, print -1. Input Input consists of an integer n (3 ≤ n ≤ 10^4). Output Print an integer: the value of k if it exists, otherwise -1.

def find_k(n):
    a, b = 0, 1
    for k in range(2, n * n): 
        a, b = b, (a + b) % n
        if b == 0:
            return k
    return -1

n = int(input())

print(find_k(n))
