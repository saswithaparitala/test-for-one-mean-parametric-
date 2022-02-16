# test-for-one-mean-parametric-
data<-c(63,63,66,67,68,69,70,70,71,71)
#data<-c(45,47,50,52,48,47,49,53,51)
#data<-c(12.1,11.9,12.4,12.3,11.9,15.4,13.9,12.8)
print("Ënter the mu value to be tested:")
mu<-scan()
n<-length(data)
print("enter the level of significance")
alpha<-scan()
std<-sd(data)
print("Standard deviation is:")
print(std)
t<-t.test(data,mu=mu)
print(t)
#t<-t.test(data,mu=mu,alternative="less")
#print(t)
#t<-t.test(data,mu=mu,alternative="greater")
#print(t)
#t<-t.test(data,mu=mu,alternative="two.sided")
#print(t)
print("Table value for two-tailed test:")
tablevalue<-qt(1-alpha/2, df=n-1)
print(round(tablevalue,digits=4))
print("Table value for one-tailed test:")
tablevalue<-qt(1-alpha, df=n-1)
print(round(tablevalue,digits=4))


OUTPUT:
One Sample t-test

data:  data
t = 1.8904, df = 9, p-value = 0.09128
alternative hypothesis: true mean is not equal to 66
95 percent confidence interval:
 65.646 69.954
sample estimates:
mean of x 
     67.8 

> print("Table value for two-tailed test:")
[1] "Table value for two-tailed test:"
> tablevalue<-qt(1-alpha/2, df=n-1)
> print(round(tablevalue,digits=4))
[1] 2.2622
> print("Table value for one-tailed test:")
[1] "Table value for one-tailed test:"
> tablevalue<-qt(1-alpha, df=n-1)
> print(round(tablevalue,digits=4))
[1] 1.8331
