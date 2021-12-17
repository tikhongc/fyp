# fyp
Music Tagging Project:

Classifiy music into different mood and genre.

Music genre classification:

files:Creating_Dataset,MusicGenre_Deeplearning(1)

Creating_Dataset:

including full 30s audio and splitted 10s audio

dataset contains: 

1.mel-spectrum png files

2.csv file include lots of audio features and mfccs

For MusicGenre_Deeplearning(1), I mainly take the mel-log-specturm png files as inputs and use transfer learing(Xperception model) to train the model.
The accracy is low,need to change the transferred model.

Music Mood classification:
files : Musicmood-dataset,Musicmood-Deeplearning

Musicmood-dataset:
I used spotify API to acquire audio features and song information from a specificed playlist and then tagging.
For example:
I choosed use function to aquire song information from a playlist created by spotify called "Sad songs" and then tagging the genre as "sad" for this dataset.
In other words,I use the spotify inner mood classification algrithom to help me do the tagging.
And then finally combined the four mood csv files into one final "dataset_mood.csv" file.

Musicmood-Deeplearning:
1.I train the model use keras by above dataset and then display the accuracy and confusion matrix
2.
How to predict the song mood:
steps:
(1) find the song you want to predict in spotify
(2) get that distinct song id from the spotify
(3) input into prediction function
(4) prediction function will call the get song features function to get the dataframe of this song's information and audio features through spotify API again
(5) and  scale the feature values then input the features of this song to the trained model.
(6) the model will display the prediction result and print it out.

Next need to do:
If it's for a product,costomer will only provide a slice of an audio and then tell you to predict the mood.
So,I might need to know how the spotify calculate the audio features inside and then I can get a similar features by calculating through a audio. 
Anyway,use spotify to train a model is a good idea.
The accracy is nearly 70%,need to try to use the transferred model.


how to calculate the audio features :
reference:
Inside The Spotify – Echo Nest Skunkworks----https://techcrunch.com/2014/10/19/the-sonic-mad-scientists/
 
