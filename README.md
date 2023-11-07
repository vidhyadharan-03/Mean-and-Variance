#  Mean and variance of a discrete  distribution
## DATE : 25.08.23
# Aim : 

To find mean and variance of arrival of objects from the feeder using probability distribution


# Software required :  

Python and Visual components tool

# Theory:

The expectation or the mean of a discrete random variable is a weighted average of all possible
values of the random variable. The weights are the probabilities associated with the corresponding values. 
It is calculated as,

![image](https://user-images.githubusercontent.com/103921593/192938463-e34177f4-f188-48a0-bda2-8f6d1d660ed2.png)

The variance of a random variable shows the variability or the scatterings of the random variables.
It shows the distance of a random variable from its mean. It is calcualted as

![image](https://user-images.githubusercontent.com/103921593/192938695-99fedc01-34d5-4d36-84df-5880e766ed0c.png)


# Procedure :

1. Construct frequency distribution for the data

2. Find the  probability distribution from frequency distribution.

3. Calculate mean using 
   
   ![image](https://user-images.githubusercontent.com/103921593/192940431-03b81777-c54d-4286-b4f4-82dfe7666b4c.png)

4. Find  
   
      ![image](https://user-images.githubusercontent.com/103921593/192940255-2d9dd746-6875-4a6d-877b-6da6cdb96ab1.png)

5.  Calculate variance using 
  
      ![image](https://user-images.githubusercontent.com/103921593/192942852-913550a9-fabe-4a55-b956-0487b18bbd97.png)


# Experiment :

![image](https://user-images.githubusercontent.com/103921593/229993174-5b67e57e-3e01-4ac4-9f83-410a932b22bf.png)

# Program :
Developed by : VIDHYADHARAN R

Reg no : 212222110053
```
L=[int(i) for i in input().split()]
N=len(L); M=max(L) 
x=list(); f=list()
for i in range (M+1):
    c = 0
    for j in range(N):
        if L[j]==i:
            c=c+1 #finding frequency f
    f.append(c)
    x.append(i) #adding random variable X
sf=np.sum(f)
p=list()
for i in range(M+1):
    p.append(f[i]/sf) #finding p(x) 
mean=np.inner(x,p) #inner will product the X and p(X). Then add the results
EX2=np.inner(np.square(x),p) #product the x² and p(X). Then add the results
var=EX2-mean**2 #finding the variance
SD=np.sqrt(var) #finding the standard deviation
print("The Mean arrival rate is %.3f "%mean)
print("The Variance of arrival from feeder is %.3f "%var) 
print("The Standard deviation of arrival from feeder is %.3F "%SD)
```

# Output : 

![Screenshot (95)](https://user-images.githubusercontent.com/118042624/231043623-69106b1c-5075-4030-a5fb-e814aa909c7c.png)




# Results :
The mean and variance of arrivals of objects from feeder using probability distribution are calculated.
