# Machine Learning - A very Gentle Introduction

## Install libraries with pip
(inspiration from [this](https://github.com/pypa/pip/issues/3813) page)

For users that are not sudoers it is possible to install libraries by using the `--user` option of the `pip`command

`> pip install --user <lib>`

The libraries will be installed in the `~/.local/bin`path. In order to run them, there is the need of including this path in the environment var `PATH`:

`> export PATH=$PATH:~/.local/bin`

or 

`> export PATH=$HOME/.local/bin:$PATH`


## Using virtual environment
(inspiration from [this](http://docs.python-guide.org/en/latest/dev/virtualenvs/) page)

Using virtual environment is a good way to keep your personal space clean and installing libraries at your needs, in your virtual environment. 

1. Initialize a python3 virtual environment in your directory of choice: 

`> virtualenv -p python3 <venv_dir>`

2. Activate the virtual environment: 

`> source <venv_dir>/bin/activate`

3. Now you can install whatever python dependencies you need (using `pip3` for python3), and run your program

4. To deactivate the virtualenvironment: 

`> deactivate`

## Install and Use Jupyter Notebook

1. Install ipython

`> pip2 install ipython`
`> pip2 install jupyter`

2. Run

`> jupyter notebook`

## Install Keras

`> pip install numpy`

`> pip install keras`

`> pip install theano`

`> pip install pandas`





