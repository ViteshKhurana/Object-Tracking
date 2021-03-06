# Object-Tracking
Optical Flow: https://opencv-python-tutroals.readthedocs.io/en/latest/py_tutorials/py_video/py_lucas_kanade/py_lucas_kanade.html

ShiTomasi: https://opencv-python-tutroals.readthedocs.io/en/latest/py_tutorials/py_feature2d/py_shi_tomasi/py_shi_tomasi.html

Lucas kanade: https://en.wikipedia.org/wiki/Lucas%E2%80%93Kanade_method

Gunnar Farneback's algorithm.
calcOpticalFlowFarneback(prev, next, flow, pyr_scale, levels, winsize, iterations, poly_n, poly_sigma, flags) -> flow

1. prev first 8-bit single-channel input image.
2. next second input image of the same size and the same type as prev.
3. flow computed flow image that has the same size as prev and type CV_32FC2.
4. pyr_scale parameter, specifying the image scale (<1) to build pyramids for each image
   4a.   pyr_scale=0.5 means a classical pyramid, where each next layer is twice smaller than the previous one.
5. levels number of pyramid layers including the initial image; levels=1 means that no extra layers are created and only the original images are used.
6. winsize averaging window size
   6a.  larger values increase the algorithm robustness to image
7. noise and give more chances for fast motion detection, but yield more blurred motion field.
8. iterations number of iterations the algorithm does at each pyramid level.
9. poly_n size of the pixel neighborhood used to find polynomial expansion in each pixel
   9a.   larger values mean that the image will be approximated with smoother surfaces, 
10. yielding more robust algorithm and more blurred motion field, typically poly_n =5 or 7.
11. poly_sigma standard deviation of the Gaussian that is used to smooth derivatives used as a basis for the polynomial expansion; for poly_n=5, you can set poly_sigma=1.1, for poly_n=7, a good value would be poly_sigma=1.5.

Meanshift and Camshift: https://docs.opencv.org/master/d7/d00/tutorial_meanshift.html
