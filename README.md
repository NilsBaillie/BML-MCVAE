# BML-MCVAE

The code of this repository is based on the code made by the authors of the article "Monte Carlo Variational Auto-Encoders", it is available at : https://github.com/stat-ml/mcvae/

The .py files in the 'models' folder have not been modified. We were not able to run the initial code so we did adjustements for the main.py and utils.py files.

It is important to use the 1.1 version of the pytorch-lightning package, other packages are also needed, they can be obtained by uncommenting the first lines of the notebooks. Also, you will need to comment the files 134 and 135 of the file located at : 
pytorch-lightning/trainer/optimizers.py

The "Toy_experiment" notebook can be run directly on cpu, the 'PPCA' notebook however needs to train several models so it is advised to run it with a gpu on colab for instance.
The run this notebook on colab you need to follow the steps : 

1) Download every needed file to colab :
main.py, utils.py and put the files : __init__,auxilary,encoders,decoders,vaes,samplers,models,normflows(.py) 
in a folder named 'models'.

2) Go to the folder containing all the packages and rename 'torchtext' to something else (we used 'slt'). 
(usr/local/lib/python3.10/dist-packages)

3) Go to the file pytorch-lightning/trainer/optimizers.py and comment lines 134 and 135.

4) Make sure to run the command with '--gpus 1' at the end so the gpu is used, and not simply detected.

