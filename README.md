# Assignment-02-may-17-2022
t=int(input())
while t:
    t=t-1
    n=int(input())
    arr=[]
    arr.extend(list(map(int,input().split())))
    l=len(arr)
    pf=[0]*l
    pf[0]=arr[0]
    for i in range(1,n):
        pf[i]=pf[i-1]+arr[i]
    for i in range(n):
        if i==0:
            lsum=0
        else:
            lsum=pf[i-1]
        rsum=pf[l-1]-pf[i]
        if lsum==rsum:
            print(i)
    
