****
### Terms
- KMeans
- WCSS

[code](https://github.com/EricChoii/ai-boot-camp-ablearn/blob/main/ai/unsupervised-learning/clustering/codes/k_means_clustering.ipynb)

# KMeans
![image](https://user-images.githubusercontent.com/39285147/178481551-a473b830-a736-460a-be3d-99b3e63d48d6.png)

## Process
- **STEP 1**: Choose the numbe rK of clusters
- **STEP 2**: Select at random K points, the centroids (not necessarily from your dataset)
- **STEP 3**: Assign each data point to the closest centroid --> That forms K clusters
  - Euclidean distance
- **STEP 4**: Compute and place the new centroid of each cluster
- **STEP 5**: Reassign each data point to the new closest centroid. If any reassignment took place, go to STEP 4, otherwise go to FIN 

### 한계와 해결
![image](https://user-images.githubusercontent.com/39285147/178483148-06b9e317-8101-4467-b919-b64bb84e8a6b.png)![image](https://user-images.githubusercontent.com/39285147/178483167-e02479d0-94ff-4202-bbcd-84c0a04c4732.png)

초기 센터 설정 위치에 따라 결과가 달라진다.
- K-Means++ (**TBD**)

## How to Choose Right # Clusters?
### ① Generally, randomly select # clusters  

### ② [*The Elbow Method*]

![image](https://user-images.githubusercontent.com/39285147/178484283-93d34416-e1cc-4271-a6c7-8977c46f0157.png)

#### *WCSS*이란?

![image](https://user-images.githubusercontent.com/39285147/178485050-9d389d0b-e8c3-4dad-b736-c529f708bf58.png)
