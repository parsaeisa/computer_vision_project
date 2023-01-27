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

Now we can find the vertices very easily . after finding vertices we apply a transform to crop the image . 

![cropped image](https://github.com/parsaeisa/computer_vision_project/blob/master/pictures/cropped.png)


## Networks
### Siamese

The main duty of siamese network is learn the similarity between two images . The size of the input is so small so we need window sliding 
on pictures . Hence it needs a pair of data as input and a label for each pair .

![Siamese network](https://github.com/parsaeisa/computer_vision_project/blob/master/pictures/keras_siamese_networks_process.webp)

A window in a picture is paired with a window with same coordinations in the picture of its pattern . 
And the label is a window in the binary mask image f the crack ( still with same coordination ).

### U-Net