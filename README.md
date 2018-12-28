# Bbox-label-Tool-large-img-Phyton35
Modification of Bbox label tool for Python35

Original code Source: https://github.com/BASFProject-2018spring/BBox-Label-Tool-large-img

Files
1. main.py (for BMP image)
2. main_jpg.py (for jpg image)
3. convert.py (convert image label to YOLOV2 format: <object-class> <x> <y> <width> <height>

Where:
<object-class> - integer object number from 0 to (classes-1)
<x_center> <y_center> <width> <height> - float values relative to width and height of image, it can be equal from (0.0 to 1.0]
for example: <x> = <absolute_x> / <image_width> or <height> = <absolute_height> / <image_height>
atention: <x_center> <y_center> - are center of rectangle (are not top-left corner)

4. process.py (split image list into train and test list)

Usage

1. Split training images into N folders so you don't need to label all of them once.
- Put all images to be labeled **each time** into Images/001, Images/002, etc.
(001 has been created for you, if you need more, simply create them)
- Under 'Labels' folder, create empty folders with same names as in Images (001,002,etc.). (001 has been created) 

2. execute 'main.exe' (created by py2exe, under Linux, use main.py instead)

3. Input a number (1 for Images/001, 2 for Images/002, etc...), and click 'Load'.
The images in that folder will be loaded.

4. choose the class of the next bbox you'll make, click 'confirm'. The default is to label interested nematodes,
- if the next nematode you want to label is non-interested, please change class and click 'confirm'.
- if again you want to label interested nematodes, you should change back and click 'confirm'.

5. To create a new bounding box, left-click to select the first vertex. 
Moving the mouse to draw a rectangle, and left-click again to select the second vertex.

- To cancel the bounding box while drawing, just press <Esc>.

- To delete a existing bounding box, select it from the listbox, and click 'Delete'.

- To delete all existing bounding boxes in the image, simply click 'ClearAll'.


6. After finishing one image, click 'Next' to advance. Likewise, click 'Prev' to reverse.
Or, input the index and click 'Go' to navigate to an arbitrary image.
- The labeling result will be saved if and only if the 'Next' button is clicked.  

7. All bounding boxes will be stored in corresponding folders under 'Labels'.
Folder 'Images' and 'Labels'.

8. Execute convert.py to arrange labeled data into YOLOV2 format. 

9. 
