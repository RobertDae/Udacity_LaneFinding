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

My pipeline consisted of 7 steps. Those are:
1.  Convert color image to grayscale,
2.  Apply Gaussian smoothing: to the graycaled image,
3.  Apply Canny edge detection filter: in order to get the shapes of the objects (as points),
4.  Create Mask in the picture: in order shrink the area of interest to a minimum,
5.  Apply Hough transform: in order to get the points transformed into lines,
6.  Manipulate Hough lines: here the lines will be manipulated in order to get weighted and to handle dotted lines,
7.  Draw extrapolated lines: this is finally drawing the lines as expected in the pictures and in the images

In order to draw a single line on the left and right lanes, I modified the draw_lines() function by ...

If you'd like to include images to show how the pipeline works, here is how to include an image: 

![alt text][image1]


### 2. Identify potential shortcomings with your current pipeline


Currently only the algo is not designed for shadow and sun at a time this can be improved.
Also the also gets problesm if the curves changes from left curve to right.


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to ...

- Distinguish between right and left curves.
- introduce a HSV space for the images for better analysis
- introduce a smoothing function in order to get a better transition of the lines

