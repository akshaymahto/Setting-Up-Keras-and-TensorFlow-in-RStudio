# This assignment is regarding how to setup keras and TensrorFlow in R.
# Setting Up Keras and TensorFlow in RStudio

Here’s a formalized tutorial to help you set up Keras and TensorFlow in RStudio. Since
installation of these libraries can sometimes be tedious, this step-by-step guide will ensure that
you can properly install, configure, and use Keras and TensorFlow in R.
Step 1: Install Required Packages in R
To use Keras and TensorFlow, first install the required R packages:
# 1. Open RStudio and start a new R script or open the R console.
# 2. Install the `reticulate` package, which enables R to interface with Python (since TensorFlow is
a Python library):
install.packages("reticulate")
# 3. Install the `tensorflow` and `keras` packages in R. These are the R wrappers for TensorFlow
and Keras:
install.packages("tensorflow")
install.packages("keras")
Step 2: Install Anaconda on your device
Download “Anaconda Installer” that is consistent with your system and install it.
https://www.anaconda.com/download/success
After installing, open Anaconda;
# 1. Open Anaconda Navigator:
Launch Anaconda Navigator from your Start menu (Windows), Applications folder (Mac), or
by typing anaconda-navigator in a terminal (Mac/Linux).
# 2. Navigate to the Terminal Option:
In Anaconda Navigator, locate the Environments tab on the left sidebar.
Select the environment you want to use. If you haven’t created additional environments, the
default environment, usually named “base (root),” will be active.
# 3. Open the Terminal:
With the environment selected, click on the play button (▶) next to the environment name. In
the dropdown menu, choose Open Terminal.
# 4. Start Using the Terminal:
A terminal window will open with the selected environment activated, allowing you to run
commands, install packages, and work directly within the environment.
# 5. Create a new Conda environment for your tensorflow and keras in the terminal with the
following commands
conda create -n r-tensorflow-compatible python=3.10
# 6. Activate the new environment in the terminal
conda activate r-tensorflow-compatible
Step 3: Install Tensorflow in Rstudio
Go back to Rstudio, run the following commands to install tensorflow in the conda environment
you just created.
library(tensorflow)
install_tensorflow(method = "conda", envname = "r-tensorflow-compatible")
Great! Now that TensorFlow should be successfully installed in the compatible environment, you
can proceed with setting up and running your Keras models in R.
Let’s verify TensorFlow Installation, run the test file I shared.
If you encounter the issue "ValueError: Only input tensors may be passed as positional
arguments." when you build the model, try the following sentence and restart your
Rstudio.
remove.packages("keras")
install.packages("keras3")
And change ‘library(keras)’ to ‘library(keras3)’ for the test file and restart the Rstudio!
These steps should set up your model training and testing pipeline. If you encounter any issues
along the way, let me know!
Reference:
# https://github.com/rstudio/keras3/issues/1428#issuecomment-2047357912
# https://stackoverflow.com/questions/77852732/error-using-keras-in-r-valueerror-only-input-
# tensors-may-be-passed-as-positio
