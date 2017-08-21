---
layout: post
use_math: true
title: k-means clustering
---

<h1> *k*-means Clustering </h1>

In a clustering problem, we are given:

<ul>
<li> A bunch of points (the data), and </li>
<li> Some way of measuring "closeness" between pairs of these data points.</li>
</ul>

Clustering is dividing up the data into non-overlapping groups (which we will call <i>clusters</i> because everyone else does)
so that two data points in the same cluster are "closer" together than two data points in two different clusters. 
Oh, an every data point should end up in a cluster: no "left-overs" allowed.

**Example**: Given daily close-of-business prices for a stock--so each data point is just the price--can we group 
all the prices into three groups, "high", "medium", "low"? (*Quantiles* in statistics are a special case of clustering.)
