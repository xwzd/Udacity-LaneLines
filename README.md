# **Finding Lane Lines on the Road** 

## Writeup Template

### You can use this file as a template for your writeup if you want to submit it as a markdown file. But feel free to use some other method and submit a pdf if you prefer.

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[image1]: ./examples/grayscale.jpg "Grayscale"

---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 5 steps. First, I converted the images to grayscale.Secondly, I applied a Gaussian Noise kernel to the images; Thirdly,I use the canny() function to find the edges in the image; Fourthly, I use the region_of_interest() function to only keeps the region which may have the lane line of the image. Finally, use the hough_lines() function to get the coordinates of the start and end points of the lane line in the image. 

In order to draw a single line on the left and right lanes, I modified the draw_lines() function by 2 steps. First, Calculate the slope of the line based on the coordinate difference between the start point and the end point and divided into positive and negative groups. Then, calculate the average of all coordinates in each group as the possible Lane line.


### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when the lane line exceeds preset area of interest;
Another shortcoming could be lane line is not a straight line but a curve


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to use the changing ROI;
 
