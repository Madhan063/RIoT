# RIoT
Relative Localization of IoT Devices

## System Requirements

Requires the following packages in advance :

* numpy
* scipy
* h5py
* seaborn
* plotly
* matplotlib
* mpl_toolkits
* pandas

## For Running the Code on a dataset :

The dataset should contain the latitude and longitude or x,y,z coordinates which can be used to calculate the EDM matrix by our algorithm.

After calculating the EDM matrix, we get an output Point Matrix from our solver which is later transformed rigidly to match with our initial matrix to identify error values. 

Input the Dataset as "./csv" and convert it into 3-D and send into the solver by setting the corresponding opts and lopts parameters accordingly.

## For Examining Results obtained : 

Open 'RIoT.ipynb' and you can find all the plots and theoretical basis behind the working of our code along with tabulated errors and their patterns.

## Available Datasets 

* worldcitiespop.csv : World cities and their latitudes and longitudes
From here we are using only cities of India to chalk out an outline of india. This was used to identify the performance on large datasets.

* dist.csv : Location Data from around 10 friends
This was collected to test our algorithm for small scale data and how the error varies for this kind of data.

* pipe.csv : 3D point cloud for Sewer Defect Detection
This dataset is a point cloud which represents the structure of a sewer pipe. It can check for any sort of defects or obstructions by reconstructing the spatial orientation from the distances available. This data was used to check the spatial structure reconstruction capability of the algorithm.

* atom : Inter-Atomic distances and their spatial orientation identification
This dataset is a subset of 1coh.pdb file which is used to visualise molecular structures. From this we got the coordinates of all the atoms in each of the amino acids and calculated the corresponding EDM matrix. After masking a considerable number of these entries, we tried to arrive at the spatial orientation of these atoms. This dataset was added to give a more practical application to our algorithm.
