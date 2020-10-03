# DDSP_gm2  

This Library is an adaption of the [DDSP](https://github.com/magenta/ddsp) to work on timbre transfer on singing voices. Check out the "using_vocoder" branch for the latest changes.

The project is ready to be used in Google Colab using the "notebooks" from the same-named folder:

## singing_dataset_from_youtube.ipynb
This notebook you downloads any given list of songs from youtube, performs audio source separation (using spleeter) to extract the voices from the songs and if desired, removes all the silences and adds the snippets together to one long audio file. The output is automatically saved in your google drive in a folder with the name defined at "folder_name"

## train_no_vocoder.ipynb
Contains all necessary steps to set up the environment to train the autoencoder on any unsupervised singing data saved on the connected google drive and save the resulting model to be used 

## transfer_no_vocoder.ipynb

## train_with_vocoder.ipynb

## transfer_with_vocoder.ipynb

## singing_dataset_from_youtube.ipynb






