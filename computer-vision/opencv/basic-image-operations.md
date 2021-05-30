# Basic Image Operations

## Read image - `imread()`

[Link](https://learnopencv.com/read-display-and-write-an-image-using-opencv/)

`imread(filename, flags)`

It takes two arguments:

1. The first argument is the image name, which requires a fully qualified **pathname** to the file.
2. The second argument is an optional flag that lets you specify how the image should be represented. OpenCV offers several options for this flag, but those that are most common include:
   * `cv2.IMREAD_UNCHANGED`  or `-1`
   * `cv2.IMREAD_GRAYSCALE`  or `0`
   * `cv2.IMREAD_COLOR`  or `1`- _default_
   * To check out the different flag options, click [here](https://docs.opencv.org/master/d8/d6a/group__imgcodecs__flags.html#ga61d9b0126a3e57d9277ac48327799c80)

{% hint style="warning" %}
OpenCV reads color images in BGR ****format, whereas most other computer vision libraries use the RGB channel format order
{% endhint %}

{% tabs %}
{% tab title="Python" %}
```python
# import the cv2 library
import cv2

# The function cv2.imread() is used to read an image.
img_grayscale = cv2.imread('dog.jpg',0)

#or
# Read an image
img_color = cv2.imread('test.jpg',cv2.IMREAD_COLOR)
img_grayscale = cv2.imread('test.jpg',cv2.IMREAD_GRAYSCALE)
img_unchanged = cv2.imread('test.jpg',cv2.IMREAD_UNCHANGED)

# The function cv2.imshow() is used to display an image in a window.
cv2.imshow('color image',img_color)  
cv2.imshow('grayscale image',img_grayscale)
cv2.imshow('unchanged image',img_unchanged)

# waitKey() waits for a key press to close the window and 0 specifies indefinite loop
cv2.waitKey(0)

# cv2.destroyAllWindows() simply destroys all the windows we created.
cv2.destroyAllWindows()
```
{% endtab %}

{% tab title="C++" %}
```cpp
//Include Libraries
#include<opencv2/opencv.hpp>
#include<iostream>

// Namespace nullifies the use of cv::function(); 
using namespace std;
using namespace cv;

// Read an image 
Mat img_grayscale = imread("test.jpg", 0);

//or
// Read an image 
Mat img_color = imread("test.jpg", IMREAD_COLOR);
Mat img_grayscale = imread("test.jpg", IMREAD_GRAYSCALE);
Mat img_unchanged = imread("test.jpg", IMREAD_UNCHANGED);

// Create a window.
namedWindow( "color image", WINDOW_AUTOSIZE );
namedWindow( "grayscale image", WINDOW_AUTOSIZE );
namedWindow( "unchanged image", WINDOW_AUTOSIZE );

// Show the image inside it.
imshow( "color image", img_color ); 
imshow( "grayscale image", img_grayscale );
imshow( "unchanged image", img_unchanged ); 

// Wait for a keystroke.   
waitKey(0);  

// Destroys all the windows created                         
destroyAllWindows();
```
{% endtab %}
{% endtabs %}



## Display image - `imshow()`

`imshow(window_name, image)`

1. The first argument is the window name that will be displayed on the window.
2.  The second argument is the image that you want to display. 

To display multiple images at once, specify a new window name for every image you want to display.

The `imshow()` function is designed to be used along  with the `waitKey()` and `destroyAllWindows()` / `destroyWindow()` functions. 

The `waitKey()` function is a keyboard-binding function. 

* It takes a single argument, which is the **time \(in milliseconds\)**, for which the window will be displayed.
* If the user presses any key within this time period, the program continues.
* If **0** is passed, the program waits indefinitely for a keystroke.
* You can also set the function to detect specific keystrokes like the **Q** key or the **ESC** key on the keyboard, thereby telling more explicitly which key shall trigger which behavior. 

The function `destroyAllWindows()` destroys all the windows we created. If a specific window needs to be destroyed, give that exact window name as the argument. Using `destroyAllWindows()` also clears the window or image from the main memory of the system.

## Write image - `imwrite()`

`imwrite(filename, image)`

1. The first argument is the filename, which must include the filename extension \(for example .png, .jpg etc\). OpenCV uses this filename extension to specify the format of the file. 
2. The second argument is the image you want to save. The function returns `True` if the image is saved successfully.

{% tabs %}
{% tab title="Python" %}
```python
cv2.imwrite('grayscale.jpg',img_grayscale)
```
{% endtab %}

{% tab title="C++" %}
```cpp
imwrite("grayscale.jpg", img_grayscale);
```
{% endtab %}
{% endtabs %}

