# Self-driving-Car
It is a behavioural cloning self-driving car simulation based on the environment of Audacity. <br />
Link: https://github.com/udacity/self-driving-car <br />

## Steps to see my training result ##
### 1. Clone my repository ###
Use git clone to download my self-driving car repository into your local directory. <br />

### 2. Download the necessary packages ###
Make sure you have downloaded the packages: <br />
*flask <br />
*socketio <br />
*eventlet <br />
*tensorflow <br />
*keras <br />
*pillow <br />
*numpy <br />
*opencv 

-------------------------
(example for packages download in virtual environment)
-- conda create --name myenviron <br />
-- conda activate myenviron <br />
-- conda install -c anaconda flask <br />
-- conda install -c conda-forge python-socketio <br />
-- conda install -c conda-forge eventlet <br />
-- conda install -c conda-forge tensorflow <br />
-- conda install -c conda-forge keras <br />
-- conda install -c anaconda pillow <br />
-- conda install -c anaconda numpy <br />
-- conda install -c conda-forge opencv

### 3. Run the driver code ###
-- python driver.py

### 4. Open Udacity simulation ###
Open "Simulation" in the directory and choose your prefered screen resolution and graphics quality. <br />
(Recommend setting: <br />
Screen Resolution: 800 x 600 <br />
Graphics Quality: Fastest) <br /> <br />

### 5. See my training result or train your own self-driving car ###
Select between two tracks and choose one action below depending on your purpose.
* Choose "AUTONOMOUS MODE" to start seeing the car driving itself.
* Choose "TRAINING MODE" and record the process for behavioural cloning. You will get the file "driving_log.csv". Push it to github with the name of repository as "Track". Modify the first line in "self-driving_car.ipynb" into the link to your "Track" repository, and run through all the code in "self-driving_car.ipynb". Then back to step 3 and choose "AUTONOMOUS MODE" in step 5.

## Design process in "self-driving_car.ipynb" ##
1. Read in the data from manual training of Audacity. <br />
2. Balancing the data by removing data with steering count exceeding the limit. <br />
3. Load steering data. <br />
4. Split into training & validation set. ("sklearn") <br />
5. Preprocessing images. (using "augmenters" from "imgaug" library) <br />
6. Batch generator -- Create augmented images on the fly. <br />
7. Train the neural network. ("Keras") <br />
8. Visulize the training result. <br />
