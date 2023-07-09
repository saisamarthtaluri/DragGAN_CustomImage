# DragGAN_CustomImage

This repository explains how to use DragGAN (https://github.com/XingangPan/DragGAN) on custom images. I assume you have already installed and setup DragGAN on your system. 

## Instructions to run

Start by running the *PTI_Custom_Image* notebook on a colab session which is GPU-enabled. Run the cells untill you reach Step 4. Run the 1st cell in Step 4 which creates the directories where you need to upload your own image. Refresh the colab file browser and you should see a new directory created under PTI as "image_original" and upload your image into that directory. Then proceed to run the rest of the cells in the notebook which will take a couple of minutes. 

After running all the cells successfully, you are required to find and download 2 files - the .pkl file and the 0.pt file. The .pkl will be available at the bottom of your file browser in colab and to access the 0.pt file, you need to navigate to *PTI/embeddings/image/PTI/image* and download the 0.pt file. Move both the files into the checkpoints directory in your DragGAN installation. 

Start running the DragGAN application on Linux using:
```
sh scripts/gui.sh
```
Or if you are using windows, you can run:
```
.\scripts\gui.bat
```

Once the application loads, replace the path under the Pickle section to your downloaded pkl file. Similarly replace the path under the Latent section with the path to 0.pt file and hit the "Load Latent" button.

Your custom image should now load up on the right. Drag it around and have fun!

A more detailed and comprehensive guide is available at: -tobeupdated-
