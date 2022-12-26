# Drawsiness-Detection-Project
Drawsiness Detection Based on the Images and OpenCV

Install all the dependencies and required library packages 
pip install python 
pip install Js2Py
pip install cmake
pip install dlib
pip install numpy , matplotlib

We are using a face landmark with 68 x-y coordinates 
 ![face with 68-(x,y) coordinates](https://user-images.githubusercontent.com/43695086/209581423-24d5103b-0ceb-4f0b-b6a3-7d19e54368a3.jpg)

In this problem our Region of Interest is eyes . 
so we will have 6 point coordinate on eyes . 
eye coordinates points are :  (37, 38, 39, 40, 41, 42) and (43, 44, 45, 46, 47, 48)

![Eye-6-Points](https://user-images.githubusercontent.com/43695086/209581638-18fc871a-1b79-4b01-bb3f-2008e87d1ce7.jpg)

Based on theese points we will calculate distance betwen theese points . 
That is called Eye Aspect Ratio ( EAR ) to predict the drowesiness . 
Formula for EAR is given as :
    EAR = (dist(p2, p6) + dist(p3, p5)) /2* dist(p1, p4)
    
    if EAR >0.25 then State = Active 
    if EAR >0.20 and EAR<0.25 then State = Drowsy
    if EAR <0.20 the Status = Sleeping
    
    
