# Python-
[C++核心编程.md](https://github.com/SosDay123/Python-/files/9765905/C%2B%2B.md)
import time
from math import sqrt
from random import random

def MC(n):
    k = 0
    for i in range(n):
        x = random( )
        y = random( ) 
        if sqrt(x*x + y*y) <= 1:
            k += 1
    return 4*k/n

def pi_time( ):
    global n, pi
    n = int(input("请输入模拟次数，n = "))
    begin = time.time( )
    pi = MC(n)
    print("蒙特卡罗算法模拟的Pi值为：", pi)
    end = time.time( )
    print("程序处理时间为：%.2fs"%(end-begin))
    return n, pi

def write_file( ):
    with open("C://Users//1128//Desktop//i值的计算.txt", "a") as f:
        f.write('计算次数：' + str(n))
        f.write('\n模拟Pi值：' + str(pi))
        print('写入成功。')

if __name__ == "__main__":
    pi_time( )
    write_file( )
    
