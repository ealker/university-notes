# Image Formation

## Human Eye 

Replicating vision is a non trivial problem.


## Representation 


Image can be thought of a a continuous function, R^2 -> R:  f(x,y). To represent and then manipulate images on a computer, we need to map these continuous values to discrete values. In the context of image processing, this is known as [discretization]( https://staff.fnwi.uva.nl/r.vandenboomgaard/IPCV20172018/LectureNotes/IP/Images/ImageDiscretization.html) and is comprised of two steps: sampling and quantization. 

### Sampling (discretization of the spatial domain). 

- How many bins in the sensor? 

There is a proporational relationship between the number of bins and the resolution of the final image. 

Images are matrices of numbers, which can then be stored in two dimensional arrays. 

> Useful webpage on [2D Arrays](http://www-ee.eng.hawaii.edu/~tep/EE160/Notes/Array/2darray.html). Useful webpage on [storing images in 2D Arrays](http://www.mathcs.emory.edu/~cheung/Courses/170/Syllabus/09/make-pictures.html).



### Quantization (discretization of the image range). 

- How many levels per bin? 

Quantization looks at the luminance values. The more levels per sensor bin, the more accurate the color. As a general rule of thumb, a standard grey image has a bit depth of 8 bits (1 byte). The possible grey values for the image are therefore 2^8 or 256 possible values, ranging from 0 - 255. 