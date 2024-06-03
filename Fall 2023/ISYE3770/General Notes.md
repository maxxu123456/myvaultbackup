
The standard deviation of the estimate is also called the standard error

Write confidence interval $5\leq \mu \leq 10$ instead of $5\leq \bar{x}\leq 10$

T test works when sample is normal

Get $t_{0.025,10}=2.228$
```r
qt(0.975,df=10)
```


Use T test in R
```r
t.test(x)
```
where x is list of values


![[Pasted image 20231109140810.png]]

$$E(\chi^2)=n-1$$
Find values for $\chi^2_{.95,10}$
```r
qchisq(0.05,10)
qchisq(.95,10,lower.tail=FALSE)
#3.940299
```

VarCI

To find upper or lower bound
```r
VarCI(x,sides="right")
```

Example of Proportion Confidence Interval

In a random sample of n=1000 families owning TV sets in Atlanta, it is found that 600 subscribed to ESPN. Find a 95% confidence interval for the actual proportion of families in Atlanta that subscribe to ESPN.

$$\hat{p}=\frac{x}{n}=\frac{600}{1000}=.6$$
$$\hat{p}\pm z_{0.025}\times \sqrt{ \frac{0.6\times 0.4 }{1000}}=0.6\pm 1.96 \times \sqrt{  \frac{0.6\times0.4}{1000} }$$

VarCi

Find CI for proportions
```r
BinomCI(600,1000,method="wald")
```

To gain $\pm 3\%$ interval with 95% confidence, what the size n should be?

$$n=\left( \frac{1.96}{0.03} \right)^2\times 0.25=1067$$



Example of Hypothesis Testing

$\alpha$ is the probability of getting a type 1 error which is rejecting the null hypothesis when it's true. 

$X_{1},X_{2},\dots,X_{10}\sim N(\mu,2.5^2),n=10\to \bar{X}\sim N\left( \mu, \frac{2.5^2}{10} \right)$

$H_{0}:\mu=50$
$H_{1}:\mu \neq 50$

Assume the Acceptance Region is $48.5\leq \bar{x}\leq 51.5$

Find $\alpha$
Find $\beta$ when the true mu is 52

$$\alpha = P(\bar{X}>51.5|\mu=50)+P(\bar{X}<48.5|\mu=50)=0.05777952$$

$\beta=P(\text{Type II Error})=P(\text{Fail to reject }H_{0}|H_{0} \text{ is false})=P(48.5\leq \bar{X} \leq 51.5|\mu=52)$

Power = $1-\beta$


A textile fiber manufactuer is investigating a new drapery yarn which teh compnay claims has a mean thread elongation of 12 kilograms with a population sd of 0.5 kg. The company wishes to test the hypothesis $H_{0}:\mu=12$ against $H_{1}:\mu<12$ using a random sample of four speciemsn

(a). What is the type I error probability if the rejection region is defined as $\bar{x}<11.5 \text{kg}$
(b). Find $\beta$ for teh case where the ture mean elongation is 11.25 kg.
(c). Find $\beta$ for the case where the ture mean is 11.5 kilograms

$$\bar{X}\sim N\left( \mu, \frac{0.5^2}{4} \right)=N(\mu,0.25^2)$$
(a).

$$\alpha=P(\bar{X}<11.5|\mu=12)=0.02275013$$
(b)
$$\beta=P(\text{Fail to reject }H_{0}|H_{0}\text{ is false})=P(\bar{X}\geq 11.5|\mu=11.25)=P(Z\geq 1)=0.1586553$$

(c).
$$\beta=P(\text{Fail to reject }H_{0}|H_{0}\text{ is false})=P(\bar{X}\geq 11.5|\mu=11.5)=0.5$$


Find the boundary of the critical region is the type I error probaiblity is 
(a). $\alpha=0.01$ and $n=4$ 
(b). $\alpha=0.05$ and $n=4$ 
(c). $a=0.01,n=16$
(d). $\alpha=0.05,n=16$

(a).
$\alpha= P(\bar{X}<U_{\alpha}|\mu=12)=0.01$

$$P\left( \frac{\bar{X}-12}{0.25}< \frac{U_{\alpha}-12}{0.25} \right)=0.01\to P(\frac{\bar{X}-12}{0.25}<-z_{0.01})=0.01$$

```r
qnorm(.99)
#-2.32
```
$$\frac{U_{\alpha}-12}{0.25}=-z_{0.01}=-2.326348$$
$U_{\alpha}=11.41841$

or 
```r
qnorm(0.01,mean=12,sd=0.25)
```

For 
$Z_{\boxed{0.05}}$
the subscript denotes upper tail probability always!!!!!!!!!!!!!


z vs t for means

pop normal or not
variance of pop known
n size



![[Pasted image 20231116141216.png]]

but use 40 as threshold


Test on Mean for Normal, pOpulation Vairance Known

$H_{0}:\mu=\mu_{0}$
$H_{1}:\mu \neq \mu_{0}$

Test Statistics
$Z_{0}=\frac{\bar{X}-\mu_{0}}{\frac{\sigma}{\sqrt{ n }}}\sim N(0,1)$

![[Pasted image 20231116144720.png]]
a is wrong since you need absolut value
c is worng since it should just be $z_{0}$

For large sample, you can use Z as well, even if unknown variance , no need for t

if small sample, data is normal use t test

R code for one sided t test
where $H_{1}$ is $\mu>0.82$
```r
t.test(x,mu=0.82,alternative="greater")
```

Two sample

Two types of plastic are sutiable for use by an electrocis component manufacturer, The breaking strength of this plastic is important. It is known that $\sigma_{1}=\sigma_{2}=1$ psi. From a random sample of size $n_{1}=10,n_{2}=12$, we obtain $\bar{x}_{1}=162.5,\bar{x}_{2}=155.0$ . The company will not adopt plastic 1 unless its mean breaking strength exceeds that of plastic 2 by at least 10 psi.

$$H_{0}:\mu_{1}-\mu_{2}=10$$
$$H_{1}:\mu_{1}-\mu_{2}>10$$
$$z_{0}=\frac{162.5-155-10}{\sqrt{ \frac{1}{10}+\frac{1}{12} }}=-5.838742$$

$z_{0.05}=1.645$

Fail to Reject $H_{0}$

p-value $\approx 1$
```r
1-pnorm(-5.838)
```

# Difference in Means

Variances Known
![[Pasted image 20231205133107.png]]

Variances Unknown and Equal
![[Pasted image 20231205133124.png]]
![[Pasted image 20231205133135.png]]

Variances Unknown and Unequal

![[Pasted image 20231205133200.png]]
