# VehicleDetection_and_Counting_OpenCV
 ### The code demonstrates a simple yet effective method for detecting and counting vehicles in a video stream, using background subtraction, image processing techniques, and contour analysis.
 ##  Methodology:
1. Initialization: The code initializes necessary variables, such as the video capture object (cap), minimum width and height for detected rectangles     (min_width_react and min_height_react), and a list to store detected object centers (detect).
2. Background Subtraction: The code creates a background subtractor object (algo) using the MOG2 algorithm and applies it to the frames to extract foreground objects.
3. Image Processing: The code further processes the foreground image by applying Gaussian blur (blur), dilation (dilat), and morphological closing (dilatada) to smooth and refine the objects.
4. Contour Detection: The code finds contours in the processed image (dilatada) and iterates over each contour.
5. Bounding Rectangles: For each contour, the code calculates the bounding rectangle and checks if it meets the minimum size requirements.
6. Vehicle Counting: If a contour meets the size requirements and its center is within a certain range of the counting line, the code increments the vehicle counter (counter) and updates the list of detected object centers.   
7. Visualization: The code draws the counting line, bounding rectangles, and vehicle count on the frame (frame1) for visualization.
8. Display and Control: The code displays the processed frame, pauses for a short time to control the frame rate, and exits the loop if the 'Enter' key is pressed.
9. Cleanup: Finally, the code closes all OpenCV windows and releases the video capture resource.
