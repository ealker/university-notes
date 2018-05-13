# CS26520 Lecture 23
## Clustering 3 - Hierarchical Clustering
__Thursday, April 19th 2018__  
Lecture: rkj@aber.ac.uk   
Notes: ela12@aber.ac.uk  

These notes are based off of the course notes provided by [Dr. Richard Jensen](https://www.aber.ac.uk/en/cs/staff-list/staff_profiles/?staff_id=rkj).

## Thought Experiment 

6, 8, 13, 18, 24, 26, 32. 

Which two points should be part of the same cluster? 6 and 8. They're the closest data points. 

K means doesn't work out clusters based on how close the data points are to each other, it looks at how close the data points are to a centroid. 

## Hierarchical Clsutering Algorithms 

Agglomerative (Bottom Up) Approach: 

- Start with each dat apoint in a single cluster.
- erge based on distance/closeness
- All data points belong to the same cluster.

Divise (Top Down)

- Start with each dat apoint in a single cluster.
- Split data based on distance.
- Wach node forms a cluster on its own. 

This does not equirew the number of clusters $k$ in advance. 

## HAC - Hierarchical Agglomerative Clustering 

Assumes a similarity measure for determining the similarity of two data points. 

- Use the distance function from previous lectures. 

Starts w/ all points in separate clusters, then repeatedly joins the clusters that are most similar until there is only one cluster. 

The history forms a tree or a hierarchy. 


Clustering obtained by cutting the dendrogram at a desired level: each connected component forms a cluster.

Basic algorithm is straightforward
- Compute the distance matrix (= distance between any 2 data points)
- Let each data point be a cluster
-  Repeat
    - Merge the two (or more) closest clusters  Update the distance matrix
    - Until only a single cluster remains

The key operation odf this approach is the computation of the proximity of any two clusters. 
How do you define the nearness of clusters? 

### Closest Pair of Clusters 

Options: 
- Single Link: Distance of the closest points.
- Complete Link: Distance of the furthest points.
- Centroid: Distance of the centroicds (average over the distance of all points).
- Average Link: Average distance between pairs of elements. 

### Single Link Agglomerative Clustering 

Has a "Chaining" problem - clusters can be created with values that are far apart. 

smallest distance between value (a,b) and (x). so if it's x - a = min, use a, if it's x -b = min, use b. 

### Complete-link agglomerative clustering. 
Use the same equation, but using the max distance. Makes “tighter,” spherical clusters that are typically preferable. 

We **still merge the two nearest clusters based on the distance**.

Clusterings: {1,3},{8,9},{10}, we merge {8,9} and {10}.

