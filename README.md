## EX.NO : 05
## Date : 27.04.2022
# <p align="center"> Implementation-of-Filters</p>
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1
Import the necessary modules.

### Step2
For performing smoothing operation on a image.

* Average filter
```
avg_kernel=np.ones((13,13),np.float32)/169
average_filter_image=cv2.filter2D(image,-1,avg_kernel)
```
* Weighted average filter
```
wt_avg_kernel=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
wt_average_filter_image=cv2.filter2D(image,-1,wt_avg_kernel)
```
* Gaussian Blur
```
gaussian_blur=cv2.GaussianBlur(image,(31,31),0,0)
Median filter
median_blur=cv2.medianBlur(image,11)
```

</br>
</br> 

### Step3
For performing sharpening on a image.

* Laplacian Kernel
```
lap_kernel=np.array([[-1,-1,-1],[-1,8,-1],[-1,-1,-1]])
lap_image=cv2.filter2D(image,-1,lap_kernel)
```
* Laplacian Operator
```
Lap_sharp=cv2.Laplacian(image,cv2.CV_64F)
```
</br>
</br> 

### Step4
Display all the images with their respective filters.

</br>
</br> 
 

## Program:
### Developed By   :DurgaDevi.P
### Register Number:212220230015
</br>

### 1. Smoothing Filters

i) Using Averaging Filter
```Python
average_kernel=np.ones((13,13),np.float32)/169
average_filter_image=cv2.filter2D(image,-1,avg_kernel)
plt.figure(figsize=(10,10))
plt.subplot(1,2,1)
plt.axis("off")
plt.title('Original image')
plt.imshow(image)
plt.subplot(1,2,2)
plt.axis("off")
plt.title('Average Filter image')
plt.imshow(average_filter_image)
plt.show()



```
ii) Using Weighted Averaging Filter
```Python
weight_average_kernel=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
weight_average_filter_image=cv2.filter2D(image,-1,weight_average_kernel)
plt.figure(figsize=(10,10))
plt.subplot(1,2,1)
plt.axis("off")
plt.title('Original image')
plt.imshow(image[30:200,50:200])
plt.subplot(1,2,2)
plt.axis("off")
plt.title('Weighted average Filter image')
plt.imshow(weight_average_filter_image[30:200,50:200])
plt.show()




```
iii) Using Gaussian Filter
```Python
gaussian_blur=cv2.GaussianBlur(image,(31,31),0,0)
plt.figure(figsize=(10,10))
plt.subplot(1,2,1)
plt.axis("off")
plt.title('Original image')
plt.imshow(image)
plt.subplot(1,2,2)
plt.axis("off")
plt.title('Gaussian Filter image')
plt.imshow(gaussian_blur)
plt.show()




```

iv) Using Median Filter
```Python
median_blur=cv2.medianBlur(image,11)
plt.figure(figsize=(10,10))
plt.subplot(1,2,1)
plt.axis("off")
plt.title('Original image')
plt.imshow(image)
plt.subplot(1,2,2)
plt.axis("off")
plt.title('Median Filter image')
plt.imshow(median_blur)
plt.show()




```

### 2. Sharpening Filters
i) Using Laplacian Kernal
```Python
laplacian_kernel=np.array([[-1,-1,-1],[-1,8,-1],[-1,-1,-1]])
laplacian_image=cv2.filter2D(image,-1,laplacian_kernel)
plt.figure(figsize=(10,10))
plt.subplot(1,2,1)
plt.axis("off")
plt.title('Original image')
plt.imshow(image)
plt.subplot(1,2,2)
plt.axis("off")
plt.title('Laplacian Kernel Filter image')
plt.imshow(laplacian_image)
plt.show()




```
ii) Using Laplacian Operator
```Python
Laplacian_sharp=cv2.Laplacian(image,cv2.CV_64F)
plt.figure(figsize=(10,10))
plt.subplot(1,2,1)
plt.axis("off")
plt.title('Original image')
plt.imshow(image)
plt.subplot(1,2,2)
plt.axis("off")
plt.title('Laplacian Operator Filter image')
plt.imshow(Laplacian_sharp)
plt.show()




```

## OUTPUT:
### 1. Smoothing Filters
</br>

i) Using Averaging Filter

![p1](https://user-images.githubusercontent.com/75235704/167774965-1bd8f37d-896e-4b16-87b2-f230935b3969.jpeg)

</br>
</br>
</br>
</br>
</br>

ii) Using Weighted Averaging Filter

![p2](https://user-images.githubusercontent.com/75235704/167775015-265f1515-9547-4131-bcf8-f15c48ba1a0a.jpeg)

</br>
</br>
</br>
</br>
</br>

iii) Using Gaussian Filter

![p3](https://user-images.githubusercontent.com/75235704/167775070-334c7552-0610-407b-b599-978ddce2743c.jpeg)

</br>
</br>
</br>
</br>
</br>

iv) Using Median Filter
![p4](https://user-images.githubusercontent.com/75235704/167775135-0986ce8f-9790-4e7e-bb4a-0ec63776d6a2.jpeg)


</br>
</br>
</br>
</br>
</br>

### 2. Sharpening Filters
</br>

i) Using Laplacian Kernal
![p5](https://user-images.githubusercontent.com/75235704/167775166-3e369933-ceeb-4974-81f7-680238f06b74.jpeg)


</br>
</br>
</br>
</br>
</br>

ii) Using Laplacian Operator

![p6](https://user-images.githubusercontent.com/75235704/167775221-32b45507-ffaf-4162-88d3-fc52081ccd90.jpeg)

</br>
</br>
</br>
</br>
</br>

## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
