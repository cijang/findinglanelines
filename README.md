# **Finding Lane Lines on the Road** 
[![Udacity - Self-Driving Car NanoDegree](https://s3.amazonaws.com/udacity-sdc/github/shield-carnd.svg)](http://www.udacity.com/drive)

<img src="examples/laneLines_thirdPass.jpg" width="480" alt="Combined Image" />

Overview
---

This project aims to implement the logics to find the left and right lane lines in the given images and annotate throughout almost all of the videos.

Helper Function
- grayscale function is used to convert an image to gray color image.
- canny function is used to detect all the edges from a given image.
- gaussian_blur is used to apply Gaussian Noise kernel to the graycolor image.
- region_of_interest is used to define the interest region in a given image and mask all other area.
- draw_lines function is used to calculate the average line and center from the identified lines and create one big line. This help performance by reducing the number of lines drawing.
- hough_lines function is used to detect the meaningful lines and draw the left and right lane lines.
- weighted_img function is used to draw the weighted lines on top of the output image from hough_lines.

Reflection
---

My solution is not identifying the interested region automatically. When an image has curves and shadows in a different region of the image, it could miscalculate the lane lines. It may have to improve the logic to identify the region of interest, range of white color channel, etc.


Project
---
## If you have already installed the [CarND Term1 Starter Kit](https://github.com/udacity/CarND-Term1-Starter-Kit/blob/master/README.md) you should be good to go!   If not, you should install the starter kit to get started on this project. ##

**Step 1:** Set up the [CarND Term1 Starter Kit](https://github.com/udacity/CarND-Term1-Starter-Kit/blob/master/README.md) if you haven't already.

**Step 2:** Open the code in a Jupyter Notebook

You will complete the project code in a Jupyter notebook.  If you are unfamiliar with Jupyter Notebooks, check out [Udacity's free course on Anaconda and Jupyter Notebooks](https://classroom.udacity.com/courses/ud1111) to get started.

Jupyter is an Ipython notebook where you can run blocks of code and see results interactively.  All the code for this project is contained in a Jupyter notebook. To start Jupyter in your browser, use terminal to navigate to your project directory and then run the following command at the terminal prompt (be sure you've activated your Python 3 carnd-term1 environment as described in the [CarND Term1 Starter Kit](https://github.com/udacity/CarND-Term1-Starter-Kit/blob/master/README.md) installation instructions!):

`> jupyter notebook`

A browser window will appear showing the contents of the current directory.  Click on the file called "P1.ipynb".  Another browser window will appear displaying the notebook.  Follow the instructions in the notebook to complete the project.  

**Step 3:** Complete the project and submit both the Ipython notebook and the project writeup

## How to write a README
A well written README file can enhance your project and portfolio.  Develop your abilities to create professional README files by completing [this free course](https://www.udacity.com/course/writing-readmes--ud777).

