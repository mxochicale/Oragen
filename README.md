# Oragen
Open source machine learning and data visualization for novice and expert







# Starting Orange GUI
```
cd ~/orange/orange3venv/bin
 ./orange-canvas
```

In case of further issues, read:
http://stackoverflow.com/questions/38761998/how-to-run-orange3-after-installing



# INSTALLATION on Ubuntu 14.04 x64


* Install some build requirements via your system's package manager
sudo apt-get install  git python3-dev g++ gfortran libblas-dev liblapack-dev libatlas-base-dev
```
  ERROR sudo apt-get install virtualenv
  ERROR Unable to locate package virtualenv
```
Solution
```
sudo apt-get install python3-pip
sudo pip3 install virtualenv
```
https://www.digitalocean.com/community/tutorials/how-to-install-the-django-web-framework-on-ubuntu-14-04



* Also install Qt dependencies for the GUI
```
sudo apt-get install python3-pyqt4
```

* Create a separate Python environment for Orange and its dependencies, and make it the active one
```
virtualenv --python=python3 --system-site-packages orange3venv
source orange3venv/bin/activate
```

* Clone the repository and move into it
```
git clone https://github.com/biolab/orange3.git
cd orange3
```


* Install the minimum required dependencies first
```
pip install numpy  
pip install scipy  
pip install -r requirements-core.txt  # For Orange Python library  
pip install -r requirements-gui.txt   # For Orange GUI  
pip install -r requirements-sql.txt   # To use SQL support  
pip install -r requirements-opt.txt   # Optional dependencies, may fail  
                                      #Command "python setup.py egg_info" failed with error code 1 in   #/tmp/pip-build-5sa29r7t/qt-graph-helpers/  
```



* Finally install Orange in editable/development mode.  

```
pip install -e .  

.  
.  
.  
Successfully installed Orange3  
```  
