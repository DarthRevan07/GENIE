# GENIE

## Non-local GNNs for Jet Classification : 

Dataset can be found at : 
`https://zenodo.org/records/2603256`

I used the following libraries for a highly efficient and memory-saving representation and computation of jet features (pre-processing) and for the computation of Persistent Homology as a wrapper for the ParticleNet model. 
![vector](https://github.com/user-attachments/assets/58701d95-bf76-437f-a6c0-fe6b25c0f1d9)
![numba](https://github.com/user-attachments/assets/ef22e868-1dcd-4097-9aa7-cf8edbe8bda7)

For the computation of Persistent Homology of the jet clouds, I use `Pyrivet` which is a Python API for the RIVET library that allows multiparameter persistence models to be fitted on discrete data, describing it in terms of a continuous shape - an `Abstract Simplicial Complex`.

To initially make single-parameter estimators such as that which has been currently implemented in `1d_persistence.py` I have used the topological methods in `gtda` and also `Ripser` library.


The following figure describes the architecture for the conventional `ParticleNet` model that uses the `EdgeConv` operation on the k-NN graph : 


<img width="834" alt="Screenshot 2024-05-23 at 5 59 18 PM" src="https://github.com/user-attachments/assets/9141e356-fe92-4ffb-ac6c-19aab31416cb">

We replace the k-NN graph step by the `Persistence` step. 
The workflow for the project is : 


![joel_network](https://github.com/user-attachments/assets/1e97e7f9-907e-459d-b81d-ffbf5b6f46fe)
