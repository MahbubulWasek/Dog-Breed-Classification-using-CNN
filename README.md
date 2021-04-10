# Dog-Breed-Classification-using-CNN
Udacity DataScience NanoDegree Capstone Project

### Table of Contents

1. [Instructions](#instructions)
2. [Project Motivation](#motivation)
3. [File Descriptions](#files)
4. [Results](#results)
5. [Licensing, Authors, and Acknowledgements](#licensing)

## Instructions <a name="instructions"></a>



1. Clone the repository and navigate to the downloaded folder.
```	
git clone https://github.com/MahbubulWasek/Dog-Breed-Classification-using-CNN
cd 
```

2. Download the [dog dataset](https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/dogImages.zip).  Unzip the folder and place it in the repo, at location `path/to/dog-project/dogImages`. 

3. Download the [human dataset](https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/lfw.zip).  Unzip the folder and place it in the repo, at location `path/to/dog-project/lfw`.  If you are using a Windows machine, you are encouraged to use [7zip](http://www.7-zip.org/) to extract the folder. 

4. 
- Donwload the [VGG-16 bottleneck features](https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/DogVGG16Data.npz) for the dog dataset.  Place it in the repo, at location `path/to/dog-project/bottleneck_features`.

- Donwload the [Inception-V3 bottleneck features](https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/DogInceptionV3Data.npz) for the dog dataset.  Place it in the repo, at location `path/to/dog-project/bottleneck_features`.


5. (Optional) __If you plan to install TensorFlow with GPU support on your local machine__, follow [the guide](https://www.tensorflow.org/install/) to install the necessary NVIDIA software on your system.  If you are using an EC2 GPU instance, you can skip this step.

6. (Optional) **If you are running the project on your local machine (and not using AWS)**, create (and activate) a new environment.

	- __Linux__ (to install with __GPU support__, change `requirements/dog-linux.yml` to `requirements/dog-linux-gpu.yml`): 
	  ```
	  conda env create -f requirements/dog-linux.yml
	  source activate dog-project
	  ```  
	- __Mac__ (to install with __GPU support__, change `requirements/dog-mac.yml` to `requirements/dog-mac-gpu.yml`): 
	  ```
	  conda env create -f requirements/dog-mac.yml
	  source activate dog-project
	  ```  
	**NOTE:** Some Mac users may need to install a different version of OpenCV
	  ```
	   conda install --channel https://conda.anaconda.org/menpo opencv3
	  ```
	- __Windows__ (to install with __GPU support__, change `requirements/dog-windows.yml` to `requirements/dog-windows-gpu.yml`):  
	  ```
	  conda env create -f requirements/dog-windows.yml
	  activate dog-project
	  ```

7. (Optional) **If you are running the project on your local machine (and not using AWS)** and Step 6 throws errors, try this __alternative__ step to create your environment.

	- __Linux__ or __Mac__ (to install with __GPU support__, change `requirements/requirements.txt` to `requirements/requirements-gpu.txt`): 
	  ```
	  conda create --name dog-project python=3.5
	  source activate dog-project
	  pip install -r requirements/requirements.txt
	  ```
	**NOTE:** Some Mac users may need to install a different version of OpenCV
	  ```
	  conda install --channel https://conda.anaconda.org/menpo opencv3
	  ```
	- __Windows__ (to install with __GPU support__, change `requirements/requirements.txt` to `requirements/requirements-gpu.txt`):  
	  ```
	  conda create --name dog-project python=3.5
	  activate dog-project
	  pip install -r requirements/requirements.txt
	  ```
	
8. (Optional) **If you are using AWS**, install Tensorflow.
    ```
    sudo python3 -m pip install -r requirements/requirements-gpu.txt
    ```
	
9. Switch [Keras backend](https://keras.io/backend/) to TensorFlow.
	- __Linux__ or __Mac__: 
		  ```
		  KERAS_BACKEND=tensorflow python -c "from keras import backend"
		  ```
	- __Windows__: 
		  ```
		  set KERAS_BACKEND=tensorflow
		  python -c "from keras import backend"
		  ```

10. (Optional) **If you are running the project on your local machine (and not using AWS)**, create an [IPython kernel](http://ipython.readthedocs.io/en/stable/install/kernel_install.html) for the `dog-project` environment. 
    ```
    python -m ipykernel install --user --name dog-project --display-name "dog-project"
    ```

11. Open the notebook.
    ```
    jupyter notebook dog_app.ipynb
    ```

12. (Optional) **If you are running the project on your local machine (and not using AWS)**, before running code, change the kernel to match the dog-project environment by using the drop-down menu (**Kernel > Change kernel > dog-project**). Then, follow the instructions in the notebook.


## Project Motivation<a name="motivation"></a>

For this project, I was interested in creating a Dog Breed Identification using Convolutional Neural Networks (CNNs) to process real-world, user-supplied images. In order, to reduce training time without sacrificing accuracy CNNs in this project were trained using transfer learning. The solution can be used for other fine-grained classification problems as well.


## File Descriptions <a name="files"></a>

There are 2 datasets used for this project

i) Dog Image Dataset- 	There are 133 total dog categories and 8351 total dog images in the dog dataset. It has been split into training, validation and testing sets. The training, validation and testing sets contain 6680, 835 and 836 dog images respectively.

ii) Human Face Image Dataset- It contains 13233 total human face images.



###### app
| - template n

| |- master.html # main page of web app

| |- go.html # classification result page of web app

|- run.py # Flask file that runs app

###### data
|- disaster_categories.csv # data to process

|- disaster_messages.csv # data to process

|- process_data.py

|- InsertDatabaseName.db # database to save clean data to

###### models
|- train_classifier.py

|- classifier.pkl # saved model

## Results<a name="results"></a>

Summarised results of the project can be found [here](https://mwase009.medium.com/is-it-a-human-or-a-dog-b7e5732d61f2).

## Licensing, Authors, Acknowledgements<a name="licensing"></a>

Must give credit to Udacity for the project learning.  Otherwise, feel free to use the code here as you would like! 
