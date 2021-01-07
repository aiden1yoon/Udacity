# **Finding Lane Lines on the Road** 

## Writeup Template

### You can use this file as a template for your writeup if you want to submit it as a markdown file. But feel free to use some other method and submit a pdf if you prefer.

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[image1]: ./test_images_output/solidWhiteCurve.jpg 

---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 5 steps. First, I converted the images to grayscale, then I found blurred the images. This make it easier to get the canny image. I would need to choose a region of interest so that I can calculate the hough transformation of the lanes.

In order to draw a single line on the left and right lanes, I modified the draw_lines() function by first finding the first degree polynomial for both left and right lanes. I could then pick out points to draw the most accurate lines.

![alt text][image1]


### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when the lane is curved. I can't accurately draw lines that are curved as its in 1st degree polynomial but if I increase the degree then I think I can.

Another shortcoming could be if the camera setting is changed then I would not be able to detect the lanes correctly due to a fixed region of interest.


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to increase the degree of polynomial.

Another potential improvement could be to implement a flexible region of interest.