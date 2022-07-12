****
### Terms
- KNN
- Eclidean distance

[code](https://github.com/EricChoii/ai-boot-camp-ablearn/blob/main/ai/supervised-learning/classification/codes/k_nearest_neighbors.ipynb)

# KNN Intuition
![image](https://user-images.githubusercontent.com/39285147/178264975-cbcd6ecf-396a-4aae-af13-b10957c9eae1.png)

## How did it work?
![image](https://user-images.githubusercontent.com/39285147/178265534-fe4dedc0-7c7a-403b-a1f1-0f8a48dc82d7.png)![image](https://user-images.githubusercontent.com/39285147/178282037-d5a93c2d-e01f-4a64-9d47-5c6ba34ea51f.png)

- STEP 1: Choose the number K of neighbors
- STEP 2: Take the Knearest neighbors of the new data point, according to the Eclidean distance
- STEP 3: Among these K neighbors, count the number of data points in each category
- STEP 4: Assign the new data point to the category where you counted the most neighbors

## Eclidean distance
![image](https://user-images.githubusercontent.com/39285147/178265398-d2498983-0efd-4d6c-82c6-b6d2b0cf5749.png)
