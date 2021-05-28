# Network Graph Approach to Image Imputation

Abstract — Image imputation has many applications in image processing from photo restoration and editing, to medical image correction, to applications in computer vision and object permanence. In this paper, we develop two methodologies to impute pixel values in images with the first serving as a baseline and the second serving as an improved final approach. The first approach uses linear regression to imputing selected unknown pixels in an image. We then discuss the drawbacks of this methodology and propose an original and novel alternative. This alternative is a graph networks approach that allows for higher flexibility and performance, but at a cost of high computation constraints. We demonstrate the differences of my two methodologies and their unique advantages and drawbacks.

### See report in repo for more detail 

## The Problem

The overall problem is centered around imputing unknown or damaged pixels using the surrounding pixels.

<img width="600" alt="Screen Shot 2021-05-28 at 9 21 14 AM" src="https://user-images.githubusercontent.com/54241448/119998261-27e12c00-bf96-11eb-8230-9dcff2590dbe.png">

The two test cases we tested our two imputation approaches on.
 (1) how well can we replace certain specific areas of an image
 (2) how well can we impute the blacked out pixels if 50% of the pixels are set to randomly blacked out.

<img width="600" alt="Screen Shot 2021-05-28 at 9 24 08 AM" src="https://user-images.githubusercontent.com/54241448/119998600-78f12000-bf96-11eb-83ca-d1de82fdc3af.png">

## Solutions with Naive Linear Regression Approach

Problem 1 : 

<img width="207" alt="Screen Shot 2021-05-28 at 9 26 10 AM" src="https://user-images.githubusercontent.com/54241448/119998872-c1a8d900-bf96-11eb-9416-4a1b266a834c.png"><img width="207" alt="Screen Shot 2021-05-28 at 9 26 34 AM" src="https://user-images.githubusercontent.com/54241448/119998927-cff6f500-bf96-11eb-94f3-b7fbc03d9356.png">

Problem 2 :
First image is full image with imputed pixes, second image is the imputed pixels only
<img width="514" alt="Screen Shot 2021-05-28 at 9 27 11 AM" src="https://user-images.githubusercontent.com/54241448/119999019-e69d4c00-bf96-11eb-900c-cb604e8b7007.png">

## Novel Network Graph Approach Parameters

 * see report for detailed description of parameters and their calculation

<img width="514" alt="Screen Shot 2021-05-28 at 9 28 52 AM" src="https://user-images.githubusercontent.com/54241448/119999241-22d0ac80-bf97-11eb-94e5-457ce4e0ece8.png">

<img width="514" alt="Screen Shot 2021-05-28 at 9 29 55 AM" src="https://user-images.githubusercontent.com/54241448/119999363-485db600-bf97-11eb-8e7d-11ce1e25c756.png">

## Solutions with Novel Network Graph Approach

Problem 1 : 

<img width="207" alt="Screen Shot 2021-05-28 at 9 30 49 AM" src="https://user-images.githubusercontent.com/54241448/119999476-69260b80-bf97-11eb-8358-ef90b798b64c.png"><img width="207" alt="Screen Shot 2021-05-28 at 9 31 10 AM" src="https://user-images.githubusercontent.com/54241448/119999522-74793700-bf97-11eb-9d4d-806380fa4c8c.png">

Problem 2 :
First image is full image with imputed pixes, second image is the imputed pixels only
<img width="514" alt="Screen Shot 2021-05-28 at 9 31 40 AM" src="https://user-images.githubusercontent.com/54241448/119999602-89ee6100-bf97-11eb-9cdf-aabb036bb3f3.png">

## Conclusion

We are overall happy with the graph networks approach in its ability to successfully predict missing pixel values. In both evaluations of predicting specific missing areas of an image and in understanding all image features as whole, the graph network approach performed significantly better than our baseline linear regression approach. We are further encouraged by the fact that we didn’t reference any previous methodologies for image imputation and instead relied on our own processes of trial and error to develop a novel graph network-based methodology. One of our next steps will now be research how others attempted to solve this problem. We look forward to learning about how other people solved the problems we couldn’t, mainly in being able to scale their methodology to a higher pixel image. Once we have a more efficient running pipeline we think immediate uses could be in photo restoration and editing. Our methodology is much further away from contributing to any feature recognition/computer vision tasks, but nonetheless it is still an interesting application to think about.
