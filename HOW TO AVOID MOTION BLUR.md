# HOW TO AVOID MOTION BLUR
Motion blur can cause the industrial camera to capture unsharp / blurry images. Unsharp images result in inaccurate measurements, bad fault detection or wrong classifications. Motion blur is caused by movement or vibration during the exposure time of the industrial camera. When the object moves for more than 0.5 pixel during the exposure time, the image will have motion blur.

To avoid motion blur, the shutter speed must freeze the scene, so the object does not move more than 0.5 pixel during exposure time. This can be done by reducing the exposure time of the camera. However, reducing the exposure time will also make the image darker (as there is less time to capture light).
 ![Illustration of the effect of motion blur](https://www.get-cameras.com/Files/8/122000/122647/FileBrowser/knowledge-center/motion-blur-2.png)

# HOW TO MAKE YOUR SETUP MORE LIGHT SENSITIVE

If your image is too dark you can check one of the following points to make the imaging setup more light sensitive:
- Use a lens with a bigger aperture, when switching from F2.0 to a F1.4 lens, you will capture twice as much light (please note that the depth of field will be reduced when using a bigger aperture)
- Use a camera with big pixel size. When looking at image sensors from the same product line, the larger the pixel, the more photons can be captured. Using an image sensor with a 6.9µ pixel instead of 3.45µ pixel will result in four times more light (3.45*3.45=10.90µm² , 6.9*6.9=47.61µm²). When comparing sensors from different product lines, a bigger pixel will not always result in a more light sensitive pixel, because the newer the image sensor, the more light sensitive the pixel is for the same pixel size.
- Use camera in binning mode. The camera takes the sum of four pixels as the new pixel value. (Resolution of the camera will be reduced by a factor four). This will result in four times more light sensitivity
- Use a Monochrome camera. A monochrome camera can capture up to three times more light than a colour camera.
- Add digital gain, however digital gain also introduces noise.
- Add extra external lights.
- If you use machine vision lights, you could try to over strobe the lights using a strobe controller
- Slowing down the movement of your object will decrease motion blur.

# HOW TO CALCULATE THE EXPOSURE TIME TO PREVENT MOTION BLUR

In this example we want to detect an object of 1mm. Our field of view is 320x240mm and we use a camera with a resolution of 1280x960mm. Our system resolution = FOV / camera resolution = 320/1280=0,25mm/pixel.

The speed of the object is 0.6 meter / minute = 0.6*1000/60= 10mm/second
The object should not move more than 0.5 pixel and we already calculated that 1 pixel is 0.25mm. So the object should not move more than 0.5*0.25=0.125mm. The time the object needs for moving 0.125mm is movement distance / speed of object = 0.125/10= 0.0125second = 12.5 milliseconds.
The max exposure time to prevent motion blur is 12.5 milliseconds.

Important note, for capturing moving objects a global shutter camera is required. A rolling shutter camera will give distorted images (see global shutter vs rolling shutter).

