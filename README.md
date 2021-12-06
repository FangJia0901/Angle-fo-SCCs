# Bond-Angle-for-SCCs
The code is being sorted out. If you have any questions, please don't hesitate to contact me.(email: 2191200398@zju.edu.cn)

Environments
===
Ubuntu 16.04.7 
CUDA 10.1.243  
Python 3.7.3  
PyTorch 1.1.0 

Required Data
===
The data that support the findings of this study are available in https://www.kaggle.com/c/champs-scalar-coupling/data. we mainly focused on the features related to molecular structure in the feature engineering, ignoring the electronic or magnetic features such as Mulliken charge and magnetic shielding tensor. We believe that the structural characteristics of molecules are the result of the integrated manifestation of all the influencing factors. The influence of these factors is included in the structural information.

Data preprocessing
===
All features which potentially influence SCCs are extracted and engineered with the guidance of prior physicochemical knowledge!The data can first be preprocessed through preprocess.py（runs for hours）and create_crossfolds.py（Divide training, validation, and testing ratios）

DrawMolsToImage
===
If you want to observe the specific structure of the molecule, you can python DrawMolsToGridImage.py to run the RDKit installation package to visualize the molecule
If you have trouble installing RDKit, please refer to  http://www.rdkit.org/ or contact me.

Training started
====
The model can be run via train7.py.If you want to understand the structure of the model, you can refer to model.py. The GAANN model has been trained by Fastai library in PyTorch framework. We train the model by parallel computation.  

Performance evaluation
===
In addition, we provide GAANN performance measurement code（such as scatter_type.py),drawing Molecular Structure code.
