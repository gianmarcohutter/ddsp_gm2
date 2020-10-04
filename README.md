# DDSP_gm2  

This Library is an adaption of the [DDSP](https://github.com/magenta/ddsp) to work on timbre transfer on singing voices. Check out the "using_vocoder" branch for the latest changes.
The corresponding audio files can be found at https://n.ethz.ch/~ghutter/webpage/sound.html
For training with singing voices we recommend the datasets [from Wilkinson et al.](https://zenodo.org/record/1193957) or the [NUS-48](https://smcnus.comp.nus.edu.sg/nus-48e-sung-and-spoken-lyrics-corpus/)

The final and complete architecture can be seen in Figure 1:
![Figure 1](https://github.com/gianmarcohutter/ddsp_gm2/blob/master/final.png)

The project is ready to be used in Google Colab using the "notebooks" from the same-named folder:

## singing_dataset_from_youtube.ipynb
This notebook you downloads any given list of songs from youtube, performs audio source separation (using spleeter) to extract the voices from the songs and if desired, removes all the silences and adds the snippets together to one long audio file. The output is automatically saved in your google drive in a folder with the name defined at "folder_name"

## train_no_vocoder.ipynb
Contains all necessary steps to set up the environment to train the autoencoder on any unsupervised singing data saved on the connected google drive and save the resulting model to be used. 


## transfer_no_vocoder.ipynb
When provided with the model (or multiple intermediate model save points) and the audio to be transformed this notebook saves the output of each model save point to the google drive to be compared to each other and evaluate the transformation quality.

## train_with_vocoder.ipynb
Same as the train_no_vocoder.ipynb file but takes the "alternative audio" as input to the z-encoder to better generalize the input voices and rid them of the singer specific timbre. Can be used for other purposes as well in case backtranslation would be implemented or other effects added to the voice. The notebook actually clones the repo from the "vocoder" branch, not from the master. 

## transfer_with_vocoder.ipynb
Pendant to "transfer_no_vocoder.ipynb" again taking the alternative audio to use the vocoded input. 

## better_harmonic_inharmonic.ipynb
Can be used instead of "transfer_no_vocoder.ipynb" to generate one output transformation with the improved mixing technique of the filtered noise and the harmonic synthesizer.


