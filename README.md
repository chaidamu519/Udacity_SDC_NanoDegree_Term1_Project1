# Udacity_SDC_NanoDegree_Term1_Project1
Lane Finding
# ## **Finding Lane Lines on the Road**

The output images are in (.\test_images_output\\)
The output 2 videos are in (.\test_videos_output\\)



# Pipelines

**the pipeline is written in the function **` lane_lines `

  1. Convert the image to grayscale.
  2. Gaussian smoothing.
  3. Applying the Canny transform to find edges.
  4. Define region of interest.
  5. Use Hough transform to find lines.
  6. Draw the lines on the initial image. 
      > In `draw_lines`, lines obtained from Hough transform are separated into  left and  right parts  by calculating the slop. Short lines are removed. Then  `cv2.fitLine` is used to obtain the average slopes and and intercepts for the drawing of the final lines.
  

## Shortcomings 

The code doesn't work for the challenge task in which the lane lines are strongly distorted by the shadows of the tree branches. Other objects that can distort the distribution of light intensity may reduce the performances as well.

## Possible improvements

By taking into account the precedent few frames taken by the camera, we could increase the stability of the lane line detector to remove some noises such as the shadows of the tree branches. However, this may not be the solution for a real self-driving car in certain special circumstances. The information used from the image is not sufficient. We can improve the performance by taking into account other factors from the image, but we need to use other image processing methods.


