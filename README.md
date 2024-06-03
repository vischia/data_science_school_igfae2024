    # Machine learning tutorial at Data Science School IGFAE 2024
    
(c) Pietro Vischia (pietro.vischia@cern.ch)


## Tutorial organization

Ideally you would be running the tutorial on your laptop, following the instructions and explanations given by me in the big screen in the room.
If, for any reason, you cannot run the tutorial, you are welcome to just watch the tutorial steps being executed in the big screen by me.

## How to run the tutorial on your local machine

#### 1. Check out the code
```
git clone git@github.com:vischia/data_science_school_igfae2024.git
cd data_science_school_igfae2024/
```
or
```
git clone https://github.com/vischia/data_science_school_igfae2024.git
cd data_science_school_igfae2024/
```

#### 2. Create a python environment and install requirements (follow one of the options 2.1, 2.2, or 2.3)

##### 2.1 Using virtualenv

```
virtualenv -p python3.9 venv_tutorial
source venv_tutorial/bin/activate
pip install -r requirements.txt # or requirements_macos.txt on MacOS Monterey
```

A participant of a previous school (Geoffrey Mullier) reports that on MacOS 12.5 `virtualenv` doesn't work, and that in that case `python3 -m venv venv_tutorial` works as intended.

To deactivate the environment, you should run `deactivate` from the command prompt.

##### 2.2 Using conda

```
conda create --name venv_tutorial python==3.9.13
conda activate venv_tutorial
pip install -r requirements.txt # or requirements_macos.txt on MacOS Monterey
```

To deactivate the environment, you should run `conda deactivate` from the command prompt.


##### 2.3 Using Google Colab (google account needed)

Go to [Google Colab](https://colab.research.google.com/), select `GitHub` as a source, and fill in the path to this repository (`https://github.com/vischia/data_science_school_igfae2024`). Possibly Google will ask for access to your GitHub account, although installing from a public third party repository should not require that, in principle.

When the colab instance is active, open the jupyter notebook `train_hyp.ipynb` and run the cell labelled "*If you are using COLAB*"


#### 3. Run the tutorial

For local environments, run

```
jupyter notebook
```

and open `lesson_1.ipynb` in the browser window that is opened.

From Colab, open `lesson_1.ipynb`.

If you prefer to run a regular python script, you can convert the notebook using the command:

```
jupyter nbconvert --to script lesson_1.ipynb
```

This will create a file `lesson_1.py` that you can pass as a command line argument to the python interpreter.
You may have to add a few `plt.show()` or `plt.savefig()` to the code here and there, to visualize/save outputs, though.
