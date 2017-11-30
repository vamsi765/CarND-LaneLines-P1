# **Finding Lane Lines on the Road** 

## Writeup Template

### You can use this file as a template for your writeup if you want to submit it as a markdown file. But feel free to use some other method and submit a pdf if you prefer.

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[image1]: test_images/solidWhiteRight.jpg "Original Image"
[image2]: test_images_output/solidWhiteRight.jpg "Marked Image"

---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 5 steps.

1) Convert the images to grayscale
2) Apply Guassian filter for blurring the image to have smother transition
3) Apply Canny filter to create black and white image given the threshold
4) Apply Mask to get the region of interest
5) Apply Hough transform to get the lines for joining the pixels

If you'd like to include images to show how the pipeline works, here is how to include an image: 

![alt text][image1]
![alt text][image2]


### 2. Identify potential shortcomings with your current pipeline


Couple of potential shortcomings are:
1) Curvature of road is not being taken into consideration
2) The basic assumption is that the road and lines are distictively different
3) There might be an issue when there is a white car close to the camera 


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to ...

1) The lines should be traced only until certain angle[horizontal lines can be ignored]

