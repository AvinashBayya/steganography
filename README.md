# Steganography-to-hide-text
Python program to hide the intended information within any image/audio/video and also decode images

Steganography is a technique of hiding information behind the scene. It’s is not like cryptography which focuses on encrypting data(through different algorithms like SHA1, MD5 etc), steganography focuses more on hiding the data (data can be a file, image, message or video) within another file, image, message or video to avoid any attraction.

So here we demonnstrate a simple python program that hides the information behind the image without noticiable changes in the looks of the image. There are two main parts of the program – first is a decoding function that can extract secret information from an image file and second is a encoding function that will encode secret messages into images.

## Basic concepts of Pixels used

Pixels are the smallest individual element of an image. So, each pixel represents a part of the original image. It means, higher the pixel-higher or much accurate representations of the actual picture.

In a black and white image (not greyscale), black pixel has a value 1 and a white pixel as a value of 0. Whereas in colored images, they have three main color components(RGB- Red, Green, Blue), with pixel values of 0-255 for each pixel. So a pixel of (255, 255, 255) will represent a white and (0,0,0) means black. As the maximum number an 8-bit binary number can represent 255, is the maximum number we can go.

As the base of binary-number is 2, we can convert the binary number into decimal very easily. Let, our binary number is 01010101, then its equivalent decimal number(base 10) will be 85 and so on.

## Encode the data :

Every byte of data is converted to its 8-bit binary code using ASCII values. Now pixels are read from left to right in a group of 3 containing a total of 9 values. The first 8-values are used to store the binary data. The value is made odd, if 1 occurs and even, if 0 occurs. 

## Decode the data :

To decode, three pixels are read at a time, till the last value is odd, which means the message is over. Every 3-pixels contain a binary data, which can be extracted by the same encoding logic. If the value if odd the binary bit is 1 else 0.
