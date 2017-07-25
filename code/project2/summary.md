# What differentiates doodles from drawings

## Pitch
Millions of drawings have been collected by Google to feed a neural network capable of recognizing what is beeing drawn. I would like to focus the project on the unrecognized drawings from the dataset. The drawings that were to bad or to different from what the system expected.
As each drawing is geolocalized, it is possible to find which population has done the highest percentage of unrecognized drawing for each concept. It is also possible to get which concept was the hardest to draw or how many lines did it require to draw, for example, an apple or a car.

## Summary
>The Quick Draw Dataset is a collection of 50 million drawings across 345 categories, contributed by players of the game Quick, Draw!. The drawings were captured as timestamped vectors, tagged with metadata including what the player was asked to draw and in which country the player was located.
[Link to the dataset](https://github.com/googlecreativelab/quickdraw-dataset)  

## Details

**Possible headlines**

1. You VS the Neural Net
2. Who are the bad
3. "I can't draw": Google feels the same way...

**Code repository**

**Possible problems/fears/questions:**
I have to merge a lot of datasets in binary format

**Sketches/inspiration**
[How do you draw a circle?](https://qz.com/994486/the-way-you-draw-circles-says-a-lot-about-you/)

## Work so far
I Learned how to read and unpack the binary files in python and made a simple analysis for the "apple" concept.