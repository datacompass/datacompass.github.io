---
layout: post
use_math: true
title: k-means Clustering
---

Before giving the steps of the method, we give a small overview of clustering in general.

# What is clustering about?

In a clustering problem, we are given:

- A bunch of points (the data), and </li>
- Some way of measuring "closeness" between pairs of these data points.</li>

Clustering is dividing up the data into non-overlapping groups (which we will call <i>clusters</i> because everyone else does)
so that two data points in the same cluster are "closer" together than two data points in two different clusters. 
Oh, an every data point should end up in a cluster: no "left-overs" allowed.

**Example**: Given daily close-of-business prices for a stock--so each data point is just the price--can we group 
all the prices into three groups, "high", "medium", "low"? (*Quantiles* in statistics are a special case of clustering.)

# *k*-means Clustering

##  When this method is usable

This method of clustering can be used if:

* The number of clusters is decided from the start.  (This is the number *k*.)
* The data points are coordinate tuples of numbers (for example, $xy$-pairs, or $xyz$-triples, or $x_1 x_2 \ldots x_{N}$-tuples).
* One can make a good guess at the means of the clusters.  These means are coordinate tuples of the same dimension as the data points.

##  The steps of *k*-means clustering

Let $\mu_{1}, \mu_{2}, \ldots, \mu_{k}$ be the initially guessed means of the *k* clusters we are looking to determine.

**Step 1.**  For each data point, find the closest mean $\mu_{i}$ and label that point as belonging to the $i$-th cluster.

**Step 2.**  Recompute the means by letting each
$$
\mu_{i} = \mbox{the average of all the data points in the $i$-th cluster, where $i$ goes from 1 to $k$.}
$$
If all the newly computed means are the same as the previous ones, stop.  Otherwise, go back to Step 1.

