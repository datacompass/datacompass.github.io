---
layout: post
use_math: true
title: k-means Clustering
---

# H1 What is clustering about?

In a clustering problem, we are given:

- A bunch of points (the data), and </li>
- Some way of measuring "closeness" between pairs of these data points.</li>

Clustering is dividing up the data into non-overlapping groups (which we will call <i>clusters</i> because everyone else does)
so that two data points in the same cluster are "closer" together than two data points in two different clusters. 
Oh, an every data point should end up in a cluster: no "left-overs" allowed.

**Example**: Given daily close-of-business prices for a stock--so each data point is just the price--can we group 
all the prices into three groups, "high", "medium", "low"? (*Quantiles* in statistics are a special case of clustering.)

# H1 *k*-means Clustering

This method of clustering works if:

* The number of clusters is decided from the start.  (This is the number *k*.)
* The data points are coordinate tuples of numbers (for example, $xy$-pairs, or $xyz$-triples, or $x_1 x_2 \ldots x_{N}$-tuples).

