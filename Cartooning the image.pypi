# -*- coding: utf-8 -*-
"""
Created on Sat Nov 21 12:19:26 2020

@author: Bhagyanidhi Patil
"""
#importing libraries

import cv2
import numpy as np

#reading images
img=cv2.imread("file1.jpg",1)

#Edges
gray=cv2.cvtColor(img,cv2.COLOR_BGR2GRAY)
gray=cv2.medianBlur(gray,5)
edges=cv2.adaptiveThreshold(gray,255,cv2.ADAPTIVE_THRESH_MEAN_C,cv2.THRESH_BINARY,9,9)

#cartoonization
color=cv2.bilateralFilter(img,9,250,250)
cartoon=cv2.bitwise_and(color,color,mask=edges)

cv2.imshow(" OriginalImage",img)            #original image
cv2.imshow("Image with edges",edges)          #image with edges
cv2.imshow("Cartoon Image",cartoon)      #cartoon image
cv2.waitKey(0)
cv2.destroyAllWindows()
