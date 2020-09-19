# Reverse Image Search

## Summary

Image search engines that quantify the contents of an image are called Content-Based Image Retrieval(CBIR) systems. 

### 4 Steps of Any CBIR System

1. **Define image descriptor:** An image descriptor is alogrithm which are used for describing the image. Three different type of image descriptor (Color Histogram, Region Adjacency Graphs and Structural Similarity Index) are used.
2. **Index dataset:** Apply image descriptor to each image in dataset, extract features from these images, and write the features to storage (ex. CSV file, RDBMS, Redis, etc.) so that they can be later compared for similarity.
3. **Define similarity metric:** Chi-squared distance for Histogram method and Hausdorff’s distance for RAG features are used.
4. **Searching:** Extract features from image and then apply similarity function to compare the image features to the features already indexed. 

### Result

Method | Precision | Recall | F1-score | SSIM 
--- | --- | --- | --- | ---
Global Color Histogram | 0.714 | 0.5 | 0.588 | 0.53 
--- | --- | --- | --- | ---
Regional Color Histogram | 0.67 | 0.8 | 0.729 | 0.57 
--- | --- | --- | --- | ---
RAG based description | 0.375 | 0.3 | 0.33 | 0.63 
