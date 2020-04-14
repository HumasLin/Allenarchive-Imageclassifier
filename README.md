# Allenarchive-Imageclassifier

Building model for recognizing different kinds of files in omeka dataset:

### Setting the environments and tools:

Fatkun:https://chrome.google.com/webstore/detail/fatkun-batch-download-ima/nnjjahlikiabnchcpehcpkdeckfgnohf

Docker: Just Google ‘Docker’ and get the download link for different systems. Make sure you get Docker Quickstart Terminal:

<p align="center">
  <img src="https://github.com/HumasLin/Allenarchive-Imageclassifier/blob/master/image/image2.png" width="100" title="Terminal">
</p>

Collecting samples:

Google the kind of images you want to classify and the other class(es) different from the class you want to recognize:

<p align="center">
  <img src="https://github.com/HumasLin/Allenarchive-Imageclassifier/blob/master/image/image1.png" width="400" title="search image">
</p>

### Use Fatkun to select and download the pictures that should be recognized as the specific class:

<p align="center">
  <img src="https://github.com/HumasLin/Allenarchive-Imageclassifier/blob/master/image/image3.png" width="200" title="download image">
</p>

Select and download the pictures you think fit the class.

Put the samples in a folder named “data” in the following way:
        /data
             /class1
             /class2
             /class3
             ….
             
### Train the model:

Download all the files in this repo, put all the files along with the “data” folder in the same folder, except the “image-classifier.ipynb” and “omeka_files.csv” file.

Run docker using Docker Quickstart Terminal, make sure it connects to the serve with: 
  
    docker is configured to use the default machine with IP xxx

In Terminal with Docker running, run: 

    ./train.sh [any_path]/my_own_classifier.

Note: The training result includes “retrained_graph.pb” and “retrained_labels.txt”, which will be used later.

### Use the model:

Open “map.ipynb” in Google Colab, then upload “omeka_files.csv”, “retrained_graph.pb”, and “retrained_labels.txt” to the file tab.

Click “Run all”, wait for the program to end and download the “results.txt”


