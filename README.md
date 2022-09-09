[//]: # (Image References)

[image1]: ./images/sample_dog_output.png "Sample Output"
[image2]: ./images/vgg16_model.png "VGG-16 Model Keras Layers"
[image3]: ./images/vgg16_model_draw.png "VGG16 Model Figure"


## Project Overview

Welcome to the Convolutional Neural Networks (CNN) project in the AI Nanodegree! In this project, you will learn how to build a pipeline that can be used within a web or mobile app to process real-world, user-supplied images.  Given an image of a dog, your algorithm will identify an estimate of the canine’s breed.  If supplied an image of a human, the code will identify the resembling dog breed.  

![Sample Output][image1]

Along with exploring state-of-the-art CNN models for classification, you will make important design decisions about the user experience for your app.  Our goal is that by completing this lab, you understand the challenges involved in piecing together a series of models designed to perform various tasks in a data processing pipeline.  Each model has its strengths and weaknesses, and engineering a real-world application often involves solving many problems without a perfect answer.  Your imperfect solution will nonetheless create a fun user experience!

## Project Instructions

### Instructions

1. Clone the repository and navigate to the downloaded folder.
```	
git clone https://gitlab.com/atlonxp/dog-breeds-classification.git
cd dog-breeds-classification
```

2. Download the [dog dataset](https://gitlab.com/atlonxp/siit-deep-learning/-/raw/main/dogImages.zip).  Unzip the folder and place it in the repo, at location `path/to/dog-breeds-classification/dogImages`. 

3. Download the [human dataset](https://gitlab.com/atlonxp/siit-deep-learning/-/raw/main/lfw.zip).  Unzip the folder and place it in the repo, at location `path/to/dog-breeds-classification/lfw`.  If you are using a Windows machine, you are encouraged to use [7zip](http://www.7-zip.org/) to extract the folder. 

4. Download the [VGG-16 bottleneck features](https://gitlab.com/atlonxp/siit-deep-learning/-/raw/main/DogVGG16Data.npz) for the dog dataset. Place it in the repo, at location `path/to/dog-breeds-classification/bottleneck_features`.

5. (Optional) __If you plan to install TensorFlow your local machine__, follow [the guide](https://www.tensorflow.org/install/) to install the necessary NVIDIA software on your system.  If you are using an EC2 GPU instance, you can skip this step.

6. (Optional) **If you are running the project on your local machine**.

	- __Linux__ / __Mac__ / __Windows__: 
	```
	conda create --name dog-breeds-classification python=3.10
	source activate dog-breeds-classification
	pip install -r requirements/requirements.txt
	```
	
7. (Optional) **If you are running the project in Jupyter Lab on your local machine**. 

	- Install Conda
		* >> (Base) conda install -c conda-forge jupyterlab
		* Jupyter Lab/Notebook must be install at the global environment
		* Jupyter Lab/Notebook will not be able to swap kernel if the Jupyter Lab/Notebook is running within its own environment
	- Install Conda extensions
		* >> (Base) conda install ipykernel nb_conda_kernels
		* Use “ipykernel” to manage multiple kernels (aka. Conda environment)
		* Use “nb_conda_kernels” to find all Conda environments 
	- Create Conda environment and update ipykernel
		* >> conda create -n `dog-breeds-classification` ipykernel
	- Generate Jupyter Lab/Notebook configurations
		* 
	- Add Password authentication to your Jupyter Lab
		- Find following lines
		```
		## Hashed password to use for web authentication.
		#  
		#  To generate, type in a python/IPython shell:
		#  
		#    from jupyter_server.auth import passwd; passwd()
		#  
		#  The string should be of the form type:salt:hashed-password.
		#  Default: ''
		```
		- Add following lines underneath it
		```
		from IPython.lib import passwd
		password = passwd("put-your-password-here")
		c.ServerApp.password = password
		```
	- Start Jupyter Lab
		* >> jupyter lab --config /opt/.jupyter/jupyter_lab_config.py --port=8888
	- Browser Jupyter Lab at `http://127.0.0.1:8888`
		* Use your password define in previous step
		
## Evaluation

<!-- Your project will be reviewed by a Udacity reviewer against the CNN project [rubric](https://review.udacity.com/#!/rubrics/810/view).  Review this rubric thoroughly, and self-evaluate your project before submission.  All criteria found in the rubric must meet specifications for you to pass. -->

## Project Submission

When you are ready to submit your project, collect the following files and compress them into a single archive for upload:
- The `dog_app.ipynb` file with fully functional code, all code cells executed and displaying output, and all questions answered.
- PDF technical report with the name `report.pdf`.
- Any additional images used for the project that were not supplied to you for the project. __Please do not include the project data sets in the `dogImages/` or `lfw/` folders.  Likewise, please do not include the `bottleneck_features/` folder.__

Alternatively, your submission could consist of the GitHub link to your repository.
