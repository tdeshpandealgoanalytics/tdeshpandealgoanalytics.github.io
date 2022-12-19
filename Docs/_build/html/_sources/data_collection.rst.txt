data\_collection module
=======================
This is the data_collection module. This main() function of the data_collection module is responsible for collecting appropriate frames of data and storing it at a specific location.

Here firstly, frames are captured using OpenCV's VideoCapture() function. If a video is present from the URL then only the process moves forward; else "No Video" is shown.
Now, the ssim_loss of the previous frame and the current frame is calculated using the prefilter() function.
If the ssim_loss of these two frames is greater than the prefilter_threshold then the images are considered almost equal to each other and the frame is not saved as data.

But, if the ssim_loss of these two frames is less than the prefilter_threshold then there is a difference between these two frames and the current frame is then stored in the data folder with the name of the file being the current datetime().


.. automodule:: data_collection
   :members:
   :undoc-members:
   :show-inheritance:
