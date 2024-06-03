## Mean squared Error

Remember This Proof that $E[(\hat{\Theta}-\theta)^2]$

$$E[(\hat{\Theta}-\theta)^2]=E(\hat{\Theta}^2-2\hat{\Theta}\theta+\theta^2)$$
$$=E(\hat{\Theta}^2)-2\theta E(\hat{\Theta})+\theta^2$$
$$=E(\hat{\Theta}^2)-(E(\hat{\Theta}))^2+(E(\hat{\Theta}))^2-2\theta E(\Theta)+\theta^2$$
$$V(\hat{\Theta})+[E(\hat{\Theta})-\theta]^2$$
$$V(\hat{\Theta})+[\text{Bias}(\hat{\Theta})]^2$$


## Show that S is unbiased estimator of $\sigma$ 

![[Pasted image 20231207112440.png]]



Remember how to find power of the test, part c

![[Pasted image 20231128144924.png]]
Answer to part c is : .967

c.

True: $\mu_{1}-\mu_{2}=-3$

Lower bound of rejection zone t value = qt(0.025,df=28,lower.tail=FALSE) = -1.701131

Actual value of lower bound = -1.4096481571
$$-1.701131=\frac{val-0}{.8286535}\to val=-1.4096481571$$


```r
pt((-1.4096481571+3)/.8286535,df=28,lower.tail=FALSE)
#0.03260185
```
$\beta=P(T\geq\frac{-1.4096481571+3}{.8286535})=0.03260185$

$\text{Power}=1-\beta=1-0.03260185=0.96739815$


