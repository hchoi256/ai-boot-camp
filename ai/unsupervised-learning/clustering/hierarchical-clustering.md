****
### Terms
- Hierarchical Clustering

[code](https://github.com/EricChoii/ai-boot-camp/blob/main/ai/unsupervised-learning/clustering/codes/hierarchical_clustering.ipynb)

# Hierarchical Clustering
![image](https://user-images.githubusercontent.com/39285147/178683601-7888f796-67e2-4b36-87dc-94152059b69e.png)

## Distance Between Clusters
![image](https://user-images.githubusercontent.com/39285147/178683249-e795538b-4c26-43fb-99d7-17f72e8a5c12.png)
![image](https://user-images.githubusercontent.com/39285147/178691023-037c228e-2253-46df-a359-17a70d51ef61.png)

### Agglomerative HC
- STEP 1: Make each data point a single-point cluster --> that forms N clusters
- STEP 2: Take the two closest data points and make them one cluster --> that forms N-1 clusters
- STEP 3: Take the two closest and make them one cluster --> that forms N-2 clusters
- STEP 4: Repeat STEP 3 untill there is only one cluster

## How to Find Optimal # Clusters
### Dendrogram
![image](https://user-images.githubusercontent.com/39285147/178686508-07b5caac-8888-42f4-8546-2e66fa4ea5d4.png)
![image](https://user-images.githubusercontent.com/39285147/178688136-a9be3518-e380-4613-aa38-cd2fbd668942.png)

Dendrogram에서 가지 길이가 급격하게 짧아지는 지점까지의 cluster 개수
