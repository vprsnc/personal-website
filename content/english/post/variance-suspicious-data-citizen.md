---
title: "Variance: How to detect Suspicious Data Citizen"
date: 2023-01-06T20:28:50+03:00
draft: false
Tags: basics
---
![suspicious-data-citizen](/images/posts/suspicious-citizen.png)
Previously, we've covered why the mean is a great measure of *central trend*.
In short: it allows just one number to describe a whole *set* of values.
But the middle one also has a downside.
It is unstable to strong outliers in the data.
For example, if in one dataset we described the salaries of ordinary citizens and one (but what) salary of a conditional deputy.
In this case, the average result for the group can be highly distorted.

Let's say we have a dataset like this:


```
a = [1, 4, 7, 9, 4, 5, 5, 2, 3, 3, 3]

mean(а) = 4.2
```

We know the average value of **a**.
How can we understand how accurately it describes our set?
How do you know if there are outliers in your data and if you should use some other measure of central tendency?
This is exactly what spread measures are for.

Let's think about what we can do with what we *already* have.
We know each individual value of a, as well as their average.
Why don't we just compare *all values* with the average? Then we can easily understand how far each value is from the "middle".

```
[1 - 4.2, 4 - 4.2, 7 - 4.2 ... 3 - 4.2]

[-3.2, -0.2, 2.8, 4.8, -0.2, 0.8, 0.8, -2.2, -1.2, -1.2, -1.2]
```

Okay, said and done.
We have a new list of values.
But can we somehow describe it with a single number, just as we do with the average?
After all, if the list turns out to be long, it will be difficult to evaluate it “by eye”.

We could have just summed all the values and divided by the number, but in the [very first post](/post/why-mean-is-good) we said that the average itself compensates for errors.

So if we just add up all the values, we get **0**!

In general, there are a couple of options for how we can get everything not just **0**, but something more or less sane.
One is to take *absolute values*, that is, simply remove all minuses in front of negative values.

```
3.2+0.2+2.8+4.8+0.2+0.8+0.8+2.2+1.2+1.2+1.2 = 18.6

18.6 / 11 = 1.69
```

Now this is something!
Another option is to raise all values to *square*.
In practice, squaring is much more common and is known as **variance**.
And variance is more common because it has one important *advantage*:
Squaring gives an *exponential* increase in deviation.
The farther the value is from the average, the more it will affect the variance, thereby making it more visible.


```
[-3.2, -0.2, 2.8, 4.8, -0.2, 0.8, 0.8, -2.2, -1.2, -1.2, -1.2]^2

10.24+0.04+7.84+23.04+0.04+0.64+0.64+4.84+1.44+1.44+1.44 = 51.64

51.64/11 = 4.69
```

4.69 per value...
Looks suspicious.
Do we really need to do something?
But more on that next time...
