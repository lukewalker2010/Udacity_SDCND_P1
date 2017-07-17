**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report

Below I have showed an example of the various processed images as they go through my pipeline.

[//]: # (Image References)

[image1]: ./processed_images/gray.png "Grayscale"
[image2]: ./processed_images/blur.png "Gaussian Blur"
[image3]: ./processed_images/canny.png "Canny Image Transformation"
[image4]: ./processed_images/roi.png "Region of Interest"
[image5]: ./processed_images/hough.png "Hough Image Transformation"
[image6]: ./processed_images/overlay.png "Overlayed Result"

---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 5 steps. First, I converted the images to grayscale, then I applied a Gaussian blur. After that I applied the Canny image transformation. Then I defined a region of interest. Finally I applied the hough lines which called my modified draw_lines() function to extend the lines.

In order to draw a single line on the left and right lanes, I modified the draw_lines() function by first checking to see if the slope was positive or negative. If it was negative that meant that I had a right line, and if it was positive, it meant that I had a left line. From there I calculated the average slopes and intercepts. Using those along with the maximum and minimum values for x and y I was able to plot the lines.


### 2. Identify potential shortcomings with your current pipeline

One potential shortcoming would be that this model only can track straight lines and would not track curved lines correctly.

Another shortcoming could be that the way I have set it up the lines jump around a fair amount.


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to average multiple frames of the video to smooth out the transition from frame to frame.

If you would like to see the entire project open up the P1.ipynb notebook.

Luke Walker
