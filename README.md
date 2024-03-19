# IMAGE-TRANSFORMATIONS


## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the required packages.
<br>
### Step2:
Load the image file in the program.
<br>

### Step3:
Use the techniques for Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.
<br>

### Step4:
Display the modified image output.
<br>

### Step5:
End the program.
<br>

## Program:
```python
Developed By: YOHESH KUMAR R.M
Register Number: 212222240118
```

i)Image Translation
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image = cv2.imread( "tiger.jpg")
input_image = cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis( 'off')
plt.imshow(input_image)
plt.show()
rows,cols,dim =input_image.shape
M =np.float32([[1,0,100],
               [0,1,100],
               [0,0,1]])
translated_image =cv2.warpPerspective(input_image, M, (cols, rows))
plt.axis('off')
plt.imshow(translated_image)
plt.show()
```
ii) Image Scaling
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("tree.jpg")
in_img=cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
rows,cols,dim=in_img.shape
M=np.float32([[1.5,0 ,0],
              [0,1.8,0],
              [0,0,1]])
scaled_img=cv2.warpPerspective(in_img, M,(cols,rows))
plt.axis('off')
plt.imshow(scaled_img)
plt.show()
```


iii)Image shearing

``` python
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("Building.jpg")
in_img=cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
rows,cols,dim=in_img.shape
M_x=np.float32([[1,0.5,0],
                [0,1 ,0],
                [0,0 ,1]])
M_y=np.float32([[1,  0,0],
                [0.5,1,0],
                [0,  0,1]])
sheared_img_x=cv2.warpPerspective(in_img,M_x,(int(cols),int(rows)))
sheared_img_y=cv2.warpPerspective(in_img,M_y,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(sheared_img_x)
plt.show()
plt.axis('off')
plt.imshow(sheared_img_y)
plt.show()

```

iv)Image Reflection
``` python
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("sea.jpg")
in_img=cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
rows,cols,dim=in_img.shape
M_x=np.float32([[1,  0,0  ],
                [0,-1,rows],
                [0,0,1  ]])
M_y=np.float32([[-1,0,cols],
                [ 0,1,0  ],
                [ 0,0,1  ]])
reflect_x=cv2.warpPerspective(in_img,M_x,(int(cols),int(rows)))
reflect_y=cv2.warpPerspective(in_img,M_y,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(reflect_x)
plt.show()
plt.axis('off')
plt.imshow(reflect_y)
plt.show()  


```


v)Image Rotation


``` python
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("wheel.jpg")
in_img=cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
rows,cols,dim=in_img.shape
angle=np.radians(10)
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],
              [np.sin(angle),np.cos(angle),0],
              [0,0,1]])
rotated_img=cv2.warpPerspective(in_img,M,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(rotated_img)
plt.show() 
```

vi)Image Cropping
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img = cv2.imread("wood.jpg")
in_img = cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
plt.imshow(in_img)
plt.show()
cropped_img=in_img[2000:3000 ,1000:2500]
plt.imshow(cropped_img)
plt.show()
```

## Output:
### i)Image Translation

![Screenshot 2024-03-19 230036](https://github.com/yoheshkumar/IMAGE-TRANSFORMATIONS/assets/119393568/d6fff7d6-9319-4f27-8b5c-0e6542485f5b)


![Screenshot 2024-03-19 230131](https://github.com/yoheshkumar/IMAGE-TRANSFORMATIONS/assets/119393568/5ff9991c-97b9-41ca-97c5-cab81ef700be)



### ii) Image Scaling
![tree](https://github.com/yoheshkumar/IMAGE-TRANSFORMATIONS/assets/119393568/39944950-290a-4933-b8ed-d9c2d91e4121)
![Screenshot 2024-03-19 230145](https://github.com/yoheshkumar/IMAGE-TRANSFORMATIONS/assets/119393568/58f9bd7d-21dc-4e27-9f66-bccfe1c3e571)



### iii)Image shearing
![Screenshot 2024-03-19 230156](https://github.com/yoheshkumar/IMAGE-TRANSFORMATIONS/assets/119393568/8c2f2adf-e245-4f14-8e76-23305ba5d0a1)

![Screenshot 2024-03-19 230202](https://github.com/yoheshkumar/IMAGE-TRANSFORMATIONS/assets/119393568/1475a006-a549-401b-b1d2-9e8b2d42d8ee)


### iv)Image Reflection
![Screenshot 2024-03-19 230215](https://github.com/yoheshkumar/IMAGE-TRANSFORMATIONS/assets/119393568/aec98a36-6bf0-42e3-8e07-6db78bdc61fe)

![Screenshot 2024-03-19 230227](https://github.com/yoheshkumar/IMAGE-TRANSFORMATIONS/assets/119393568/21251c20-67de-4a18-b8a2-a71bc227d80b)



### v)Image Rotation
![european-shorthair](https://github.com/yoheshkumar/IMAGE-TRANSFORMATIONS/assets/119393568/0bcad2d4-5b28-4486-a981-9e7d1de47ee3)
![Screenshot 2024-03-19 230235](https://github.com/yoheshkumar/IMAGE-TRANSFORMATIONS/assets/119393568/2613fe1f-5752-4d01-93a7-5d8fdf2ce195)





### vi)Image Cropping
![Screenshot 2024-03-19 230252](https://github.com/yoheshkumar/IMAGE-TRANSFORMATIONS/assets/119393568/a7cf2215-e3b2-45f2-aaed-bb62c85ccb4c)





## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
