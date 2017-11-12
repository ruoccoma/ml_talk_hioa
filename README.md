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


## Using Notebook from remote server
(inspiration from [this](https://coderwall.com/p/ohk6cg/remote-access-to-ipython-notebooks-via-ssh) page)

From the remote machine you need to run:

`> ipython notebook --no-browser --port=8889`

On the local machine, start an SSH tunnel:

`> ssh -N -f -L localhost:8888:localhost:8889 <user>@telenor001.idi.ntnu.no`

the first option -N tells SSH that no remote commands will be executed, and is useful for port forwarding. The second option -f has the effect that SSH will go to background, so the local tunnel-enabling terminal remains usable. The last option -L lists the port forwarding configuration (remote port 8889 to local port 8888).

Now open your browser on the local machine and type in the address bar: `localhost:8888`
