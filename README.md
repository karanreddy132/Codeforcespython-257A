# Codeforcespython-257A
import sys

n,m,k = map(int,input().split())
lst = list(map(int,input().split())) 
lst.sort(reverse=True)
if(m<=k):
    print(0)
    sys.exit()

tmp = k
i = 0
while(m>tmp and i<n):
    tmp+=lst[i]-1
    i+=1

print(i if tmp>=m else -1)
