# 1174976\_EcoVision\_Project1



Overview



This project is an investigation to the use of deep learning techniques to predict Soil Organic Carbon (SOC).

The project used,  environmental, climatic, topographic, soil, and remote sensing variables from the NZ\_LUCAS\_SMAP\_NIWA dataset.



A Deep Neural Network (DNN)  Regrssion model was used using TensorFlow and Keras.



Hyperparameters were systematically evaluated to find optimal predictive performance.





Dataset: NZ\_LUCAS\_SMAP\_NIWA.csv

Target Variable: soil\_organic\_carbon\_target



The dataset contains:



Geographic variables

Latitude

Longitude

Terrain variables

Elevation

Slope

Aspect

Topographic Wetness Index

Terrain Ruggedness Index

Climate variables

Rainfall

Temperature

Solar Radiation

Humidity

Frost Days

Soil properties

Clay %

Sand %

Silt %

Soil pH

Bulk Density

Organic Nitrogen

Remote sensing variables

NDVI

EVI

NDWI







The following preprocessing steps were performed:



Removal of the target variable from the feature matrix.

Train, validation, and test dataset splitting.

Feature scaling using StandardScaler.

Random seed initialisation for reproducibility.





The baseline model used


Input Layer -> Dense(32, ReLU) -> Output Layer
Optimizer: Adam

Loss Function: Mean Squared Error (MSE)

Metric: Mean Absolute Error (MAE)

Epochs: 100

Batch Size: 32





Hyperparameter Tuning Evaluated





Hidden Layer Depth : 1,2,3,4



Number of Neurons : 8,16,32,64,128



Activation Functions : ReLU, Leaky ReLU, Tanh, ELU, Swish



Optimisers : Adam, amax, Nadam, RMSprop, SGD



Dropout rate: 0.0, 0.1, 0.2, 0.3, 0.4







Final Model Configuration
Hidden Layers: 3

Neurons per Layer: 8

Activation Function: Leaky ReLU

Optimizer: Adamax

Dropout : 0





The following evaluation metrics were used

Mean Squared Error (MSE)

Mean Absolute Error (MAE)



Lower values indicate better predictive performance.



Technoligies used:

python: 3.12.10

pandas: 3.0.3

numpy: 2.4.5

seaborn: 0.13.2

matplotlib: 3.10.9

scikit-learn: 1.8.0

tensorflow: 2.21.0

keras-tuner: 1.4.8

scikeras: 0.13.0

IPython: 9.13.0

tabulate: 0.10.0



In the folder images are the most relevant images.

It has a subfolder with more images.



Running the project: 



Install the packages:

pip install tensorflow pandas numpy matplotlib scikit-learn



create the folders SRC and DATA



copy the NZ\_LUCAS\_SMAP\_NIWA.csv to the data folder



copy the DL.ipynb to the SRC folder



Run the notebook:

jupyter notebook



Open the notebook:

DL.ipynb









final model saved as:"soil\_carbon\_model.keras"



To load

from tensorflow.keras.models import load\_model



model = load\_model("soil\_carbon\_model.keras")





Author



# 1174976

COMP661 Deep Learning

Lincoln University

Semester 2, 2026





