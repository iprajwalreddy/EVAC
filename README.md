# EVAC+
This is a repository to run [EVAC+: Multi-scale V-net with Deep Feature CRF Layers for Brain Extraction](https://arxiv.org/abs/2206.02837)

## Pre-requisites

This model depends on the implementation of the CRFasRNNLayer, which is from this repository : https://github.com/MiguelMonteiro/CRFasRNNLayer.

Files were copied for convenience.

Please follow the instructions of that repo which is also written below.

===================================================

Add the correct paths to **nvcc, g++ and CUDA/Include** in build.sh file found inside **permutohedral_lattice** folder. (lines 8, 9, and 10).

Also add the path to **libtensorflow_framework.so** file in CMakeLists.txt file that is found in **permutohedral_lattice** folder. (line 8).

Then compile the code using:
````
sh build.sh
````
Running the above command in the main folder gives you **lattice_filter.so** file. Please make sure that this file is present. If not, the models.py code would throw errors.

See the nested module [permutohedral_lattice](https://github.com/MiguelMonteiro/permutohedral_lattice) for more information on compilation for different image types.

====================================================

Just running the command should be enough to run the model.

Due to the constraints of the implemented CRFasRNNLayer, the model is limited to a Tensorflow version of 2.3.0, which will be edited later to remove this constraint.

## Examples

Please refer to [training.ipynb](training.ipynb) and [testing.ipynb](testing.ipynb).

Specifications of the model can be found in [models.py](models.py)

