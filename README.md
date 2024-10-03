# COLOR_CONVERSIONS_OF-IMAGE
## AIM
To write a python program using OpenCV to do the following image manipulations.

i) Read, display, and write an image.

ii) Access the rows and columns in an image.

iii) Cut and paste a small portion of the image.

iv)To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.


## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Choose an image and save it as a filename.jpg ,
### Step2:
Use imread(filename, flags) to read the file.
### Step3:
Use imshow(window_name, image) to display the image.
### Step4:
Use imwrite(filename, image) to write the image.
### Step5:
End the program and close the output image windows.
### Step6:
Convert BGR and RGB to HSV and GRAY
### Step7:
Convert HSV to RGB and BGR
### Step8:
Convert RGB and BGR to YCrCb
### Step9:
Split and Merge RGB Image
### Step10:
Split and merge HSV Image

##### Program:
### Developed By: Naveen Kumar B
### Register Number: 212222230091


## Output:

### i) Read and display the image

```Python
import cv2
from google.colab.patches import cv2_imshow
image=cv2.imread("/content/uiop.jpg")
cv2_imshow(image)
cv2.waitKey(0)
cv2.destroyAllWindows()
    
```
<img width="440" alt="Screenshot 2024-10-03 at 10 25 35 AM" src="https://github.com/user-attachments/assets/5a88215b-a488-490c-8fd7-489b0df031c0">





### ii)Draw shapes and add text
#### Line
```Python

import cv2
from google.colab.patches import cv2_imshow
image=cv2.imread("/content/uiop.jpg")
height,width,_=image.shape
diagonal = cv2.line(image, (0, 0), (int(width * 2), int(height * 2)), (255,
0, 0), 5)
cv2_imshow(diagonal)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
<img width="334" alt="Screenshot 2024-10-03 at 10 25 12 AM" src="https://github.com/user-attachments/assets/2d61a8db-efb5-4a12-923d-7278a4cc1873">


#### Circle
```Python
import cv2
from google.colab.patches import cv2_imshow
image=cv2.imread("/content/uiop.jpg")
circle=cv2.circle(image, (700, 500), 350, (0, 255, 0), 5)
cv2_imshow( circle)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

<img width="440" alt="Screenshot 2024-10-03 at 10 24 31 AM" src="https://github.com/user-attachments/assets/6b507f28-6a91-431f-9079-c3ddab766ee4">



#### Rectangle
```Python
import cv2
from google.colab.patches import cv2_imshow
image=cv2.imread("/content/uiop.jpg")
rectangle=cv2.rectangle(image, (10,10), (1450,950),(0, 0, 255), 5)
cv2_imshow(rectangle)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
<img width="452" alt="Screenshot 2024-10-03 at 10 23 14 AM" src="https://github.com/user-attachments/assets/295e2503-4c6d-4760-a9a9-cbfcb4b658bc">



#### Add the text "OpenCV Drawing" at the top-left corner of the image.
```Python
import cv2
image = cv2.imread("/content/uiop.jpg")
text = "OpenCV Drawing"
position = (10, 50)
font = cv2.FONT_HERSHEY_SIMPLEX
font_scale = 1
color = (204, 51, 255)
thickness = 2
res = cv2.putText(image, text, position, font, font_scale, color,
thickness, cv2.LINE_AA)
cv2_imshow(image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
<img width="448" alt="Screenshot 2024-10-03 at 10 22 54 AM" src="https://github.com/user-attachments/assets/dec0821e-9070-495d-b641-260cc82d1b09">



### iii) Image color conversion

#### BGR and RGB to HSV and GRAY
```Python
import cv2
image = cv2.imread('/content/uiop.jpg',1)
cv2_imshow(image)
hsv = cv2.cvtColor(image,cv2.COLOR_RGB2HSV)
cv2_imshow(hsv)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
<img width="439" alt="Screenshot 2024-10-03 at 10 22 16 AM" src="https://github.com/user-attachments/assets/5091b348-4351-4577-80fe-5680e549d19d">
<img width="440" alt="Screenshot 2024-10-03 at 10 22 29 AM" src="https://github.com/user-attachments/assets/bcc7a68c-2246-4722-95de-e07c405b14af">




```Python
import cv2
image = cv2.imread('/content/uiop.jpg',1)
cv2_imshow(image)
gray = cv2.cvtColor(image,cv2.COLOR_RGB2GRAY)
cv2_imshow(gray)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
<img width="447" alt="Screenshot 2024-10-03 at 10 21 24 AM" src="https://github.com/user-attachments/assets/d26813ab-06b6-4d86-b941-1f2e775336eb">
<img width="446" alt="Screenshot 2024-10-03 at 10 21 52 AM" src="https://github.com/user-attachments/assets/dc3c4e5d-4536-40bc-8ce2-59dcbe065c22">







#### RGB and BGR to YCrCb
```Python
import cv2
image = cv2.imread('/content/uiop.jpg',1)
cv2_imshow(image)
YCrCb = cv2.cvtColor(image, cv2.COLOR_BGR2YCrCb)
cv2_imshow(YCrCb)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

<img width="446" alt="Screenshot 2024-10-03 at 10 20 40 AM" src="https://github.com/user-attachments/assets/2d255725-5566-4164-95a2-d7ed7bc482a0">
<img width="438" alt="Screenshot 2024-10-03 at 10 20 53 AM" src="https://github.com/user-attachments/assets/99c8350b-9b8b-4eca-ab3d-4eec1baf4626">





#### (4) Convert the HSV image back to RGB and display it.
```Python
import cv2
image = cv2.imread('/content/uiop.jpg',1)
cv2_imshow(image)
RGB = cv2.cvtColor(image,cv2.COLOR_HSV2BGR)
cv2_imshow(RGB)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
<img width="455" alt="Screenshot 2024-10-03 at 10 20 07 AM" src="https://github.com/user-attachments/assets/3a5d34df-46e9-4108-a820-2126de724325">
<img width="442" alt="Screenshot 2024-10-03 at 10 20 19 AM" src="https://github.com/user-attachments/assets/7a643123-596e-406b-939a-ea8b00efe616">







### iv) Access and Manipulate Image Pixels
#### (1) Access and print the value of the pixel at coordinates (100, 100)
```Python
import cv2
image = cv2.imread('/content/uiop.jpg',1)
pixel_value = image[100, 100]
print(f"Pixel value at (100, 100): {pixel_value}")
```
<img width="257" alt="Screenshot 2024-09-28 at 11 02 29 AM" src="https://github.com/user-attachments/assets/0a19d8a9-f2b2-45e3-95bb-3a14f8d474db">


#### (2) Modify the color of the pixel at (200, 200) to white
```Python
import cv2
image = cv2.imread('/content/uiop.jpg',1)
image = cv2.resize(image,(400,300))
cv2_imshow(image)
image[200, 200] = [255, 255, 255]
cv2_imshow( image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

<img width="447" alt="Screenshot 2024-10-03 at 10 16 03 AM" src="https://github.com/user-attachments/assets/8451528c-7efd-44fa-8294-419981590b84">
<img width="432" alt="Screenshot 2024-10-03 at 10 16 28 AM" src="https://github.com/user-attachments/assets/e4bad67f-810e-4958-b983-9facfdbe3a48">


### v) Image Resizing
```Python
import cv2
image = cv2.imread('/content/uiop.jpg', 1)
cv2_imshow(image)
cv2_imshow(cv2.resize(image, (image.shape[1] // 2, image.shape[0] // 2)))
cv2.waitKey(0)
cv2.destroyAllWindows()
```
<img width="448" alt="Screenshot 2024-10-03 at 10 15 12 AM" src="https://github.com/user-attachments/assets/51e128fe-452c-4821-a2ce-6b0f9b455125">
<img width="225" alt="Screenshot 2024-10-03 at 10 15 31 AM" src="https://github.com/user-attachments/assets/0a89b035-c3a3-4960-8dac-f530e50cf7e2">


### vi) Image Cropping
```Python
import cv2
image = cv2.imread('/content/uiop.jpg',1)
image = cv2.resize(image,(400,300))
x, y = 50, 50
width, height = 100, 100
roi = image[y:y + height, x:x + width]
cv2_imshow(roi)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

<img width="162" alt="Screenshot 2024-10-03 at 10 14 37 AM" src="https://github.com/user-attachments/assets/5980f5d7-36ae-4487-aefc-0a093016f118">


 ### vii) Image Flipping
 #### (1) Flip the original image horizontally and display it
```Python
import cv2
image = cv2.imread("/content/uiop.jpg")
image = cv2.resize(image,(300,200))
flip=cv2.rotate(image,cv2.ROTATE_180)
cv2_imshow(image)
cv2_imshow(flip)
cv2.waitKey(0)
cv2.destroyAllWindows()
`
```
<img width="445" alt="Screenshot 2024-10-03 at 10 14 03 AM" src="https://github.com/user-attachments/assets/e21e2b51-8fb1-4d05-b2d8-bd4ea32281cb">
<img width="446" alt="Screenshot 2024-10-03 at 10 14 15 AM" src="https://github.com/user-attachments/assets/31e719ae-8406-438b-8554-696bd5b1c922">



#### (2) Flip the original image vertically and display it
```Python
import cv2
image = cv2.imread("/content/uiop.jpg")
image = cv2.resize(image,(300,200))
res=cv2.rotate(image,cv2.ROTATE_90_CLOCKWISE)
cv2_imshow(image)
cv2_imshow(res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
<img width="444" alt="Screenshot 2024-10-03 at 10 13 19 AM" src="https://github.com/user-attachments/assets/dfa8fab5-ea13-4b1e-8bb4-61a6ba560cd5">
<img width="994" alt="Screenshot 2024-10-03 at 10 13 37 AM" src="https://github.com/user-attachments/assets/996ab0c7-2670-48ed-9d68-056354fd30e4">


### viii)Write and Save the Modified Image
```Python
import cv2
img = cv2.imread("/content/uiop.jpg")
img = cv2.resize(img,(300,200))
cv2.imwrite('nature_pic.jpg',img)
```
<img width="88" alt="Screenshot 2024-09-28 at 11 07 33 AM" src="https://github.com/user-attachments/assets/36e0454c-3d96-48cf-8406-c4cf957adb4f">







## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.







