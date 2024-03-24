# ssd-mobilenet-v2-fpnlite-320 Model 
I trained ssd-mobilenet-v2-fpnlite-320 model on this same dataset , if you want you can check it  I explained step by step how to train custom SSD-mobilenet models  : https://github.com/siromermer/Money-Counter-TurkishCurrency<br><br>



<br><br>
# Yolov7 Model

##  Data 
I collected 208 images of coin using my phone camera. These images showcase various backgrounds and different combinations of currency notes and coins (for instance, 3 units of 1 Turkish Lira, 5 units of 0.25 Turkish Lira...).<br>
For now dataset is very small , but i will increase image number in future and train it again <br><br>
even with this small dataset , model detect most of the coins accurately , sometimes it can confuse 5 kurus with 25 and 10 kurus  ( i am sure about  that is because of there were very few sample of 5 kurus in training set)
<br><br> The model performs well not only in images but also in videos. ( you can find video in test_results_yolo)

## Folders 
History-Curves-Models   :   it contains information about training ,  curves(f1 score , precision , recall ) , and images from training stage <br><br>
test_results_yolo   :   Images and videos  that i tested after training model , you can find how to do predictions on an image  inside of  "# Steps of Training Yolov7 Model .txt"  txt file <br><br>
yolo_money_best.pt   :   Custom Yolov7 best model 

## How to Train Custom Yolo Object Detection Model ?
you can look for  txt file  for training custom models with Yolo  , it is inside of this repository : # Steps of Training Yolov7 Model .txt

## Labels
Labels may seem strange to you because I convert pascal  to yolo and labels are not pointing coins exactly  , check below :<br> 

5 kurus : 4   <br>
10 kurus : 3 <br>
25 kurus : 1 <br>
50 kurus : 2<br>
1 turkish lira : 0 


# Results
You can check metrics(precision,recall ..) inside of History-Curves-Models folder 
<br>Sometimes model  can confuse 5 kurus with 10 kurus and 25 kurus  (mostly 25 kurus) , i think if i increase data size model will perform better for 5 kurus , because there were very few sample of 5 kurus in training set <br>
<br>Result seems good even when there are so many coin in image , in ssd-mobilenet-v2-fpnlite-320 model , model didnt detect coins when there are so money<br>

# Examples
 here i will share some images that i tested (images are not from train or validation datasets , they are compeletly different images , you can find this images inside of test_results_yolo folder)<br>







![test1](https://github.com/siromermer/Yolov7-CustomModel-Money-Counter-TurkishCurrency/assets/113242649/46765021-51b9-419d-b3f9-3a0312ae7c43)<br><br>
![test2](https://github.com/siromermer/Yolov7-CustomModel-Money-Counter-TurkishCurrency/assets/113242649/dfd1a36b-e29c-4dab-a83f-f971d74927d4)<br><br>
![test3](https://github.com/siromermer/Yolov7-CustomModel-Money-Counter-TurkishCurrency/assets/113242649/5f6c00cb-9ce7-4c05-9b57-d8a84d5094d0)
