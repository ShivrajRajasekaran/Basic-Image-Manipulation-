## Basic_Image_Manipulations
```
Name: SHIVRAJ R 
REGISTER NO:212223110051
```
```
import cv2
import matplotlib.pyplot as plt
image = cv2.imread('d.jpg', cv2.IMREAD_GRAYSCALE)
image.shape
```
![image](https://github.com/user-attachments/assets/39587753-43c0-41b7-ab0f-4ba462739311)
```
plt.figure(figsize=[10, 10])
plt.imshow(image, cmap='gray')
plt.axis('off')  
plt.show()
```
![image](https://github.com/user-attachments/assets/29a2db6c-3d35-44f4-a431-7510c51fad9f)

```
cv2.imwrite('d.png', image)
```
![image](https://github.com/user-attachments/assets/aa376192-313a-4fd8-b993-cca5ff1be43c)
```
import cv2
from matplotlib import pyplot as plt
image = cv2.imread('Emerald_Lakes_New_Zealand.png')
image.shape
```
![image](https://github.com/user-attachments/assets/13278624-030c-41e9-a7b5-57ca1c234930)

```
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
gray_image.shape
```
![image](https://github.com/user-attachments/assets/7e694add-a075-4948-87c7-63bb913c9f29)
```
plt.figure(figsize=[10, 10])
plt.imshow(cv2.cvtColor(gray_image, cv2.COLOR_BGR2RGB), cmap='gray')
plt.axis('off')
plt.show()
```
![image](https://github.com/user-attachments/assets/a9169a18-59da-47b8-8b20-7a0fd1471179)
```
import cv2
import matplotlib.pyplot as plt
img = cv2.imread('New_Zealand_Boat.jpg', cv2.IMREAD_COLOR)
plt.figure(figsize=[3,3])
plt.imshow(img[:, :, ::-1])
```
![image](https://github.com/user-attachments/assets/f571d6eb-a2a4-4987-8ddf-c2e5c212009b)

```
cropped_img = img[100:400, 200:600]
resized_img = cv2.resize(cropped_img, (0, 0), fx=2, fy=2)
flipped_img=cv2.flip(resized_img,1)
plt.figure(figsize=[3,3])
plt.imshow(flipped_img[:,:,::-1])
plt.show()
```
![image](https://github.com/user-attachments/assets/2cee2799-0e9f-4381-8be5-d858820e776b)
```
import cv2
import matplotlib.pyplot as plt
image = cv2.imread('d.jpg')
image.shape
```
![image](https://github.com/user-attachments/assets/cd52a828-5368-4c7b-9728-a5fc834db17d)
```
text = 'Apollo 11 Saturn V Launch, July 16, 1969'
font_face = cv2.FONT_HERSHEY_PLAIN
font_scale = 2
font_color = (255, 255, 255)
font_thickness = 2
```
```
(text_width, text_height), baseline = cv2.getTextSize(text, font_face, font_scale, font_thickness)
```
```
x = (image.shape[1] - text_width) // 2
y = image.shape[0] - text_height - 10 
cv2.putText(image, text, (x, y), font_face, font_scale, font_color, font_thickness, lineType=cv2.LINE_AA)
```
![image](https://github.com/user-attachments/assets/0e24b45e-6fb1-44b1-9ba0-999cb1d7087e)

```
rect_color = (255, 0, 255) 
top_left = (500,50)
bottom_right = (700,620) 
cv2.rectangle(image, top_left, bottom_right, rect_color, 3)
```
![image](https://github.com/user-attachments/assets/ca2afc48-71e8-473c-a4c2-1e98def764c4)
```
plt.figure(figsize=(12, 12))
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.axis('on')
plt.show()
```
![image](https://github.com/user-attachments/assets/a0eda670-5ee3-4d69-8735-c99efc071d5e)
