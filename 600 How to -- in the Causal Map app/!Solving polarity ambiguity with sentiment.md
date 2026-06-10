---
date: 2025-04-09
---

# Increasing label coverage and utility: three tweaks

## 



# diversity: Concrete and Memorable labels

We use ordinary clustering of text embeddings to get clusters of labels, but then we use a generative AI to find labels for the clusters. 

The labels generated can be a bit generic, perhaps in the hope that generic labels cover more of the material.

So we tried this prompt:


|     |     |
| --- | --- |
|     |     |


For each cluster, provide four alternative 3-10 word labels which best capture the meaning of each cluster. Usually it is quite easy to provide abstract, generic labels (like a headline in an academic journal) but these can be a bit boring. Concrete, memorable labels on the other hand (like a headline from a local newspaper) can "jump out" at the reader but harder to apply to the whole cluster. That is why I am asking you for four alternative labels for each cluster.

Your four alternatives should vary as follows:

- very concrete, very memorable
- moderately concrete, very memorable
- very concrete, moderately memorable
- moderately concrete, moderately memorable



Perhaps surprisingly, 

- all the labels produced like this were more concrete and memorable, 
- the more concrete and memorable labels performed better as magnets than labels produced by a prompt without this addition.

## Attempt with iterative label refinement, one step

### initial, no number parameter to magnets

![image-20250317211238749](../img/image-20250317211238749.png)

![image-20250317202038611](../img/image-20250317202038611.png)

### second iteration

getting labels for the new clusters, discarding the cluster labels, and magnetising again. I think I prefer the original!

- ![image-20250317201905666](../img/image-20250317201905666.png)

## First iteration, More variants

The interesting news is that by asking for eight variants, at temperature = 0.5, explicitly differentiated by memorability and concreteness, we can get up to a 30% increase of coverage. 



![image-20250317210721912](../img/image-20250317210721912.png)