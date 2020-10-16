def addsort(arr,n,k):
    result=+214783647
    re=result
    arr.sort()
    #print(arr)
    a=10
    for i in range(n-k+1):
        result=(min(result,arr[i+k-1]-arr[i]))
#        print("the difference between the chosen goodie with highest price and the lowest price is" ,result)
        if(result<=re):
            #print("hi")
            a=arr[i:(i+k-1)+1]
    
    n=("Number of the employees: " ,k )
    z=("\n")
    p=("the goodies price selected for distribution are",a )
    y=("\n")
    q=("the difference between the chosen goodie with highest price and the lowest price is" ,result)

    file1 = open("output.txt", "w")  
    file1.write(str(n)) 
    file1.write(str(z))
    file1.write(str(p))
    file1.write(str(y))
    file1.write(str(q)) 
 

        

    #sys.stdout.close()

with open('MyFile.txt','r') as file:
    c = file.read()
#print(c)
import re

string = c

arr = re.findall(r"[-+]?\d*\.\d+|\d+", string)

for i in range(0, len(arr)): 
    arr[i] = int(arr[i])
#print(arr)
k=4
#arr=[7980,22349,999,2799,229900,11101,9999,2195,9800,4999]

addsort(arr,len(arr),k)
