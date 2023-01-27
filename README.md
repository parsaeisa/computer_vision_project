# computer_vision_project

A crack detection model on tiles . 

Topics : 
* Pre-processing data . 
* Networks 
    * U-Net
    * Siamese

## Pre-processing

At first we wanted to remove the pattern from the image . 

We used morpholigical closing to remove the sketches from tiles : 

![closing](https://github.com/parsaeisa/computer_vision_project/blob/master/pictures/closing.png)


## Networks
### Siamese

The main duty of siamese network is learn the similarity between two images . The size of the input is so small so we need window sliding 
on pictures . 

A window in a picture is paired with a window with same coordinations in the picture of its pattern . 
And the label is a window in the binary mask image f the crack ( still with same coordination ).

### U-Net