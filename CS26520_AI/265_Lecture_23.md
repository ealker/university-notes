# CS26520 Lecture 23
## Data Mining - Clustering
__Friday, March 23rd 2018__  
Lecture: rkj@aber.ac.uk   
Notes: ela12@aber.ac.uk  

These notes are based off of the course notes provided by [Dr. Richard Jensen](https://www.aber.ac.uk/en/cs/staff-list/staff_profiles/?staff_id=rkj).

## Clustering Algorithms 

- Partitional Algorithms
- Hierarchical Algorithms

## Clustering Considerations 

Clustering is the process of grouping a set of objects into classes of similar objects.

Grouping and similar are both quite ambiguous terms. 

## $k$ - means algorithm

A partitional algorithm that uses a centroid.

Centroid: A point that is considered to be the center of a cluster - can be an instance in a data set or it can be artificially generatred. 

Process: 

- Start by picking $k$, the number of clusters (centroids)
- Initialise clusters by picking one point per cluster (seeds)
    - Pick data points at random.

### Populating Clusters 

Iterate until converged:

- Compute distance (using euclidean distance function) from all data points to all $k$ centroids.
- For each data point (that's not a centroid), assign it to the cluster whose current centroid it is nearest to. 
- For each centroid, compute the (mean) of all points assigned to it. 
- Replace the $k$ centroids with the new averages. 

With each iteration the new centroid beomes more accurate - converged when further iteration produces the same centroid. 

There can be other termination conditions: 

- Fixed number of iterations..
- Centroid positions don't change. 
- Clusters look "reasonable". 

