# Masterthesis Properties

# Locality
* clustering function is local if its behavior on a union of a subset of the clusters (in a clustering it outputs) depends only on distances between elements of that union, and is independent of the rest of the domain set
* "clustering a subset outputs this subset"
* can be reformulated for general clustering functions

# Consistency
* output of clustering function is invariant to shrinking within-cluster distances, and stretching between-cluster distances
* aims to formalize the preference for clusters that are dense and well-separated
* consistency implies:

## outer-consistency
* represents preference for well separated clusters, by requiring that the output of a clustering function does not change if clusters are moved away from each other
 
## inner-consistency
* represents the preference for placing points that are close together within the same cluster, by requiring that the output of a clustering function does not change if elements of the same cluster are moved closer to each other

# Richness
* clustering function is rich if by modifying the distances any output can be obtained

## k-Richness
* based on richness
* requires that we can obtain any partition of the domain by modifying the distances between elements 

## Outer / Extended Richness: 
* natural variation on k-richness
* clustering function satisfies extended richness if for every finite collection of disjoint domain sets (each with its own distance function), by setting the distances between the data sets, we can get F to output each of these data sets as a cluster.
* This corresponds to the intuition that if groups of points are moved sufficiently far apart, then they will be placed in separate clusters.

## Inner richness
* complementary to outer richness
* requires that there is a way of setting distances within sets, without modifying distances between the sets, so that F outputs each set as a cluster
* between-cluster distances cannot eliminate any partition of X

# Isomorphism invariance / Representation independence
* output of clustering function is independent of the labels of the data points

# Scale invariance
* the output of clustering is invariant to uniform scaling of the data

# Order invariance
* describes clustering functions that are based on the ordering of pairwise distances

# Γ-forcing property
* For a partition Γ, we say that a distance function d (a, b)-conforms to Γ if, for all pairs of points i, j that belong to the same cluster of Γ, we have d(i, j) ≤ a, while for all pairs of points i, j that belong to different clusters, we have d(i, j) ≥ b. With respect to a given clustering function f, we say that a pair of positive real numbers (a, b) is Γ-forcing if, for all distance functions d that (a, b)-conform to Γ, we have f(d) = Γ

## Threshold-richness
* based on Γ-forcing property
* A k-clustering function F is threshold-rich if for every clustering C of X, there exist real numbers a < b so that for every distance function d overX where d(x, y) ≤ a for all x ∼C y, and d(x, y) ≥ b for all x ?∼C y, we have that F(X, d, |C|) = C.


# Refinement-confined
* A clustering C of X is a refinement of clustering C? of X if every cluster in C is a subset of some cluster in C?, or, equivalently, if every cluster of C? is a union of clusters of C.

# Categories of weight responsiveness
## Weight responsive
* A partitional clustering algorithm A is weight-responsive on a clustering C of (X, d) if
1. there exists a weight function w so that A(w[X], d) = C, and
2. there exists a weight function w' so that A(w'[X], d) ≠ C.

## Weight sensitive
* weight-sensitive algorithms are weight-responsive on all clusterings in their range

### weight separable
* By modifying weights, we can make these algorithms separate any set of points.

## Weight robust
* weight robust algorithms do not respond to weights on any data set

## Weight considering
* algorithms that respond to weights on some clusterings but not on others

# Clustering conditions
## perfect clustering
* clustering C of (w[X], s) is perfect if for all x1,x2,x3,x4 ∈ X where x1 ∼C x2 and x3 (not)∼C x4, s(x1, x2) > s(x3,x4)

### nice clustering
* A clustering C of (w[X], d) is nice if for all x1,x2,x3 ∈ X where x1 ∼C x2 and x1 (not)∼C x3, d(x1,x2) < d(x1,x3)

## separation-uniform clustering
*C is separation-uniform if there exists λ so that for all x, y ∈ X where x (not)∼C y, s(x, y) = λ.