---
title: "Why Mean is actually good?"
date: 2023-01-01T18:22:51+03:00
draft: false
---

![average](/images/posts/mean-is-good.png)

This my first post, so why not to pick the most basic topic?

The mean, or the average, is a measure of central tendency that we are all familiar with from a young age.
It is simply *the sum of all values in a dataset divided by the number of values* in the dataset.
For example, if we have a dataset containing the values **1, 2, and 3,** the mean would be **(1+2+3)/3 = 2**.

So why is the mean such a good measure of central tendency?
One reason is that it is *easy to understand and calculate*.
Even those with little mathematical knowledge can grasp the concept of the mean and how to calculate it.

But beyond its simplicity, the mean is also a good measure of central tendency because it is *resistant to errors or mistakes*.
If we have a dataset containing **100 values** and one of those values is accidentally recorded as **1000 instead of 100**, the mean will still be a *relatively accurate representation of the central tendency* of the dataset.
This is because the mistake, or outlier, is only affecting one value and will not greatly impact the mean.

On the other hand, measures of central tendency such as the *median and mode* are more sensitive to mistakes or errors in the data.
If we have a dataset containing the values **1, 2, 3, and 1000**, the *median* would be **2** and the *mode* would be **1**, completely ignoring the outlier value of 1000.
This can lead to a distorted representation of the central tendency of the dataset.

However, the *mean* is not perfect and there are ways to make it a better measure of central tendency.
One way is to use *weighted averages**, which give more weight to certain values in the dataset.
This can be useful in cases where some values are more important or *more representative* of the central tendency than others.

To calculate the *weighted average*, we ***multiply each value by a weight** (which represents its importance or the number of data points it represents) and then sum all the values and weights.
Finally, we divide the sum of the values by the sum of the weights.

For example, let's say we have two observations with the following data points:

{{< notice >}} 
Observation 1: 10 data points, values = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]\
Observation 2: 5 data points, values = [5, 6, 7, 8, 9]
{{< /notice >}}


To calculate the weighted average, we first multiply each value by its weight:

{{< notice >}} 
Observation 1: 10 data points, values = [1x10, 2x10, 3x10, 4x10, 5x10, 6x10, 7x10, 8x10, 9x10, 10x10]\
Observation 2: 5 data points, values = [5x5, 6x5, 7x5, 8x5, 9x5]
{{< /notice >}} 

Then we sum the values and weights:


{{< notice >}} 
Values sum = 1x10 + 2x10 + 3x10 + 4x10 + 5x10 + 6x10 + 7x10 + 8x10 + 9x10 + 10x10 + 5x5 + 6x5 + 7x5 + 8x5 + 9x5 = 330\
Weights sum = 10 + 10 + 10 + 10 + 10 + 10 + 10 + 10 + 10 + 10 + 5 + 5 + 5 + 5 + 5 = 75
{{< /notice >}} 

Finally, we divide the values sum by the weights sum to get the weighted average:

{{< notice >}} 
Weighted average = 330/75 = 4.4
{{< /notice >}} 

In this case, the weighted average takes into account the fact that *Observation 1 has more data points*.
