# Projects-Collection
A github containing a few of my AI/Programming related projects collated into single Jupyter notebook files readability.

## Sentiment Analysis
This project covers making a Deep Learning AI for sentiment analysis, trained on a large dataset of labelled Amazon reviews.
The project utilizes the Pytorch library for making and training an LSTM network, with several regularisation methods to avoid overfitting.
Also included is a bunch of preprocessing code, to take the text files containing all the separate reviews, loading them, cleaning them, tokenizing and then converting them to tensors. The results are verified during training using an independent validation set, and then finally at the end of testing the AI is also tested on yet another independent test set.
The AI was able to achieve 89-92% accuracy on the test set.

## Graffiti Detection
This project was on the topic of "smart cities" using AI. My idea was to create a system for automatically detecting graffiti using instagram pictures containing location data, and then using a hypothetical graffiti cleaning drone to automatically remove the graffiti. I used a library called instaloader to automatically download instagram images with location data (geotags) from a defined area code. I then made and used an image segmentation AI to detect graffiti in the downloaded images, and if graffiti is found the location data of the corresponding image is saved in a database. I then used a basic pathfinding algorithm to determine the shortest path between the logged graffiti location that a drone could use to clean up the graffiti. For the AI I utilized transfer learning, taking the Resnet-50 network, trained on the COCO dataset, and then fine tuned it on a relatively small graffiti dataset I found. The fine tuned AI achieved an image segmentation accuracy of 72%. The pathfinding algorithm used was Dijkstra's algorithm.

## TchAIkovsky
This project covers artificial creativity. The goal of this project was to make an AI that generates music based on a small priming snippet of music. In this relatively small project we used a parallel GRU network, trained on the notes and note timings from midi files of virtuosic piano performances. The project includes a lot of pre processing, the training of the network and then finally running the network in "generation mode" to create music. The network was trained by taking a sequence of 100 notes with corresponding note durations and then tries to predict the next note. In generation mode the AI is fed a priming sequence of 100 notes and the output is then fed back into the network as input in order to generate new music.
