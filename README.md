# multi-camera-architecture-and-re-identification
Multi-camera architecture deploys interconnected cameras for comprehensive area coverage. Re-identification is a vital technique within this setup, using feature extraction and matching algorithms to track individuals or objects across varying camera views, crucial for security.



## Step 1: Data Collection and Preprocessing 

Simulation were created for this project and the results extracted were from this render. Other relavent information were extracted using python script in blender file.


## Step 2: Person Detection and Tracking

YOLO was used to detect person from frame to frame


## Step 3: Feature Extraction

The way of feature extract is from the usecase of lookup table approach.
Lookup table include - All the position of a person to exist with in a frame

Features of lookup table

          - Distance (Person to camera)
          
          - x Axis location of the person (on ground level)
          
          - y Axis location of the person (on ground level)

Distance of the person is found using the formula - ((Height of person * focal lenght) / Bounding box height)
After finding distance x axis Location and y axis Location is matched with relavent distance and positioning from the Lookup Table


## Step 4: Person Re-Identification Model

ORB similarities from opencv library was utilised.

Each person is verified from the saved image folder of people that used to be in the frame for a threshold amount of time.

If the similarities lies above the threshold value then the person is reidentfied from the saved person photo and new image of the person is saved to be refered later.

If the similarities lies below the threshold value then the person is identified as a new person and thier image is saved to be refered later.

## Step 5: Visualization and Demonstration

Relavent Visualization and Demonstration is provided in this repository in "Final_render.mp4" and rest of the .ipynb file.
