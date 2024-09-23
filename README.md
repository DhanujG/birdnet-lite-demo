# birdnet-lite-demo

## Instructions
Authors: Dhanuj Gandikota


### Birdnet Docker

#### Details

Runs on Raspberry Pi 5 with Raspberry OS Lite

This dockerfile was initially created to demo the Birdnet capabilities of an audio sensor. This will run birdnet in the background (with an assumption it is running for Austin, Texas), and will also bring up a png for each new bird that is identified within the ledger. Only the latest five recordings are kept and audio files are deleted after they are converted into ledger information. All the hyperparameters are adjustable within the main.py.

#### Run and Build the Docker

Go to the code folder

1. docker build -t birdnet_pi .

2. docker run --rm -it     --device /dev/snd     --group-add audio     -v /home/dgandikota/output_test:/home/dgandikota/output_test     birdnet_pi