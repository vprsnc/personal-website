---
title: "Why the Mean is not Always the Best Measure: The Case of Bill Gates and the Average Persons Income"
date: 2023-01-01T18:22:51+03:00
draft: false
---

![mean-is-bad](/images/posts/mean-is-bad.png)

When it comes to understanding income distribution and comparing the financial wellbeing of different groups, it is common to use measures like the *mean* (or average) income.
However, the mean can be a problematic measure in certain situations, especially when there are *extreme values* (also known as *outliers*) in the data.

Consider the case of Bill Gates, one of the wealthiest people in the world, and the income of the average person.
If we were to take the mean income of both groups and compare them, the *mean income* for the group including Bill Gates would be *significantly* higher than the mean income for the group of the average person.
However, this comparison might not accurately reflect the reality of the income distribution for these two groups.

Average income for the group of the average person is **\$50,000** per year.
We can represent this group of people as follows:

```
Group 1: [$50,000, $50,000, $50,000, ...]
```
Now, lets add Bill Gates income to this group and calculate the mean income for the resulting group:

```
Group 2: [$50,000, $50,000, $50,000, ..., $10,000,000,000]

Mean income for Group 2: $2,000,000,000
```

As we can see, the mean income for Group 2 is *significantly higher* than the mean income for Group 1, due to the influence of Bill Gates extremely high income on the mean.
This example illustrates how the mean can be a problematic measure when there are extreme values (like Bill Gates income) in the data.

But what about *weigthed average* we were speaking in the previous post? We were stating that the *weighted average* is more resistant to this kind of outliers...

Well, even the *weighted average* might not be a suitable measure in this case, despite being more resistant to the influence of extreme values:
Say that we have a group of **10** people, including Bill Gates, with the following incomes:

```
Group 3: [$50,000, $50,000, $50,000, $50,000, $50,000, $50,000, $50,000, $50,000, $50,000, $10,000,000,000]
```

To calculate the weighted average for this group, we need to assign weights to each income.
One approach could be to assign a weight of 1 to each income of **\$50,000** and a weight of **10** to Bill Gates' income of **\$10,000,000,000**.
The weighted average would then be calculated as follows:

```
Weighted average = (1 * $50,000 + 1 * $50,000 + ... + 1 * $50,000 + 10 * $10,000,000,000) / (1 + 1 + ... + 1 + 10)

Weighted average = $1,000,000,000
```

As we can see, even though the weighted average is less influenced by Bill Gates' extremely high income compared to the unweighted mean, it is still significantly higher than the income of the average person in this group (**\$50,000**).
In this case, the weighted average might not provide a meaningful or accurate comparison between the income of Bill Gates and the income of the average person.

On the other hand, if we calculate the *median income* for these two groups, we would get a more representative measure of the "typical" income for each group.
The median income for Group 1 would be **\$50,000**, and the median income for Group 2 would also be **\$50,000**, since Bill Gates income would be the highest value in the group and therefore would not influence the median.

It is important to note that the choice of weights is subjective and can significantly influence the resulting weighted average.
In this example, we used a weight of 10 for Bill Gates' income, but we could have used a higher or lower weight depending on our goals. However, it is unlikely that any weighting scheme would be able to fully compensate for the influence of Bill Gates' extremely high income on the mean or weighted average.

In summary, the mean and weighted average can be useful measures in some cases, but they can be problematic when there are extreme values in the data.
In the case of comparing the income of Bill Gates to the income of the average person, these measures might not provide a complete or accurate picture of the income distribution for these two groups.
Other measures, such as the median, might be more informative in this case.
