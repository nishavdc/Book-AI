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

## Resize image - `resize()`

[Link](https://learnopencv.com/image-resizing-with-opencv/)

* It is important to keep in mind the original aspect ratio of the image \(i.e. width by height\), if you want to maintain the same in the resized image too.
* Reducing the size of an image will require resampling of the pixels. 
* Increasing the size of an image requires reconstruction of the image. This means you need to interpolate new pixels.

{% tabs %}
{% tab title="Python" %}
```python
# let's start with the Imports 
import cv2
import numpy as np

# Read the image using imread function
image = cv2.imread('image.jpg')
cv2.imshow('Original Image', image)

# let's downscale the image using new  width and height
down_width = 300
down_height = 200
down_points = (down_width, down_height)
resized_down = cv2.resize(image, down_points, interpolation= cv2.INTER_LINEAR)

# let's upscale the image using new  width and height
up_width = 600
up_height = 400
up_points = (up_width, up_height)
resized_up = cv2.resize(image, up_points, interpolation= cv2.INTER_LINEAR)

# Display images
cv2.imshow('Resized Down by defining height and width', resized_down)
cv2.waitKey()
cv2.imshow('Resized Up image by defining height and width', resized_up)
cv2.waitKey()

#press any key to close the windows
cv2.destroyAllWindows()
```
{% endtab %}

{% tab title="C++" %}
```cpp
// let's start with including libraries 
#include<opencv2/opencv.hpp>
#include<iostream>

// Namespace to nullify use of cv::function(); syntax
using namespace std;
using namespace cv;

int main()
{
	// Read the image using imread function
	Mat image = imread("image.jpg");
	imshow("Original Image", image);


	// let's downscale the image using new  width and height
	int down_width = 300;
	int down_height = 200;
	Mat resized_down;
	//resize down
	resize(image, resized_down, Size(down_width, down_height), INTER_LINEAR);
	// let's upscale the image using new  width and height
	int up_width = 600;
	int up_height = 400;
	Mat resized_up;
	//resize up
	resize(image, resized_up, Size(up_width, up_height), INTER_LINEAR);
	// Display Images and press any key to continue
	imshow("Resized Down by defining height and width", resized_down);
	waitKey();
	imshow("Resized Up image by defining height and width", resized_up);
	waitKey();


	destroyAllWindows();
	return 0;
}
```
{% endtab %}
{% endtabs %}

To obtain the size of an image:

* use the **shape** method in **Python**
  * `image.shape` in  returns three values: **\(H, W, C\)**
* **rows** and **cols** in **C++** 
  * `image.rows` gives you the height
  * `image.columns` gives you the width of the image 
  * using the `size()` function
    * `image.size().width` returns the width
    * `image.size().height` returns the height

{% tabs %}
{% tab title="Python" %}
```python
# Get original height and width
h,w,c = image.shape
print("Original Height and Width:", h,"x", w)
```
{% endtab %}

{% tab title="C++" %}
```cpp
// Get height and width
cout << "Original Height and Width :" << image.rows << "x" << image.cols << endl;
```
{% endtab %}
{% endtabs %}

{% hint style="info" %}
OpenCV outputs the shape of an image in ![height \* width \* channels ](https://learnopencv.com/wp-content/ql-cache/quicklatex.com-29d033d57c7330f89d8885fbc83a9834_l3.png) format, whereas some other image-processing libraries give in the form of _**width, height, channels.**_ There’s a logical take to this.
{% endhint %}

> When images are read using OpenCV, they are represented as NumPy arrays. And in general, you always refer to the shape of an array, in terms of ![rows \* columns](https://learnopencv.com/wp-content/ql-cache/quicklatex.com-9e8744fadcaf9eeeb4be4a5ac2edf8c3_l3.png) \(rows representing its height and the columns its width\). So, even when reading images with OpenCV to get their shape,  the same NumPy array rule comes into play. And  you get the shape in the form of ![height \* width \* channels](https://learnopencv.com/wp-content/ql-cache/quicklatex.com-34e0ab84b7d34817c20bb347dfbf59e7_l3.png).

