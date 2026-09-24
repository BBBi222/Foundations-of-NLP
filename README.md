# Introduction
This notebook presents the training and evaluation of a small character-level Transformer
language model using nanoGPT on the Tiny Shakespeare dataset. The goal is to compare a
baseline model with multiple controlled hyperparameter experiments and to analyze their
effect on optimization dynamics (training stability and convergence), validation performance,
and qualitative text generation. All experiments vary only one hyperparameter at a time
relative to the baseline, following the systematic methodology required in the assignment.
# Setup and dataset
The nanoGPT repository https://github.com/karpathy/nanoGPT.git was used. The setup, including
repository cloning and package installation, was executed within the notebook environment.
An automatic device selection was implemented to improve training efficiency, using a GPU
(cuda) when available and otherwise falling back to CPU. In our case, training was
performed on GPU in Colab for faster execution.
The Tiny Shakespeare dataset was used as specified in the assignment. Preprocessing was
performed using the provided prepare.py script, which converts the text into a character-level
representation and creates binary training and validation files (train.bin and val.bin) as well
as metadata for the character vocabulary. The dataset is relatively small and highly stylized,
which makes it suitable for analyzing the effect of hyperparameters on both convergence
and generated text quality. Due to its small size and repetitive structure, the dataset is prone
to overfitting, making it particularly suitable for analyzing generalization behavior and the
effects of hyperparameters in small scale language models.
To facilitate structured experimentation, separate directories for configurations, logs, plots,
and generated samples were created, enabling consistent experiment tracking and analysis

Before running the code, replace any placeholder file or folder paths with the corresponding paths on your system.
