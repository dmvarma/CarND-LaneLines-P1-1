# **Finding Lane Lines on the Road** 

## Introduction


### The goal of this project is to identify and mark the lanes on the road for a given input video and output a video with lane markings.  

---

**Finding Lane Lines on the Road**

The project consists of following steps: 
* Read input file 
* pass the input through pipeline 
* save the output file 

### 1. Pileline Design
*I have converted the input image to grayscale image. Then I have used gaussian function to reduce the noise.  
*To identify edges I have used canny edge detection function with kernel_size = 5, low_threshold = 110 and high_treshold = 170 
*To specify of the region to detect the lanes, I have created a mask , with dimensions 450, 320 , 500, 300.
*To identify the lines in the image I have used Hough transform  with rho =2 , theta = np.pi/180, threshold = 50,  min_line = 2 and max_line_gap= 130. 
*Finally, I have used addWeighted function from cv2 to create a final image with lane marking on the input image. 


### 2. Observation  
The pipeline is able to 

### 3. Scope of Improvements 
Although Hough transformation is able to identify lines for lanes. It did not appear to be continous for a given video. Lines can be joined seperately for visibility purpose. 
Or Hough transform can be further modified. 


