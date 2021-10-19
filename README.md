# pysimCoder
Simulink like editor for Python

A Virtual Machine (Virtual Box) is available. Please write to me to get
the address and password to download it.

See "README" for more info

http://robertobucher.dti.supsi.ch/pysimcoder/

23.01.2019 roberto.bucher@supsi.ch

# Installation

Install dependencies
```

sudo apt install python3-venv python3-pip libxml2-dev libxmlsec1-dev libcomedi-dev python-pyqt5 python-scipy

sudo python3 ubuntu_dependency_installer.py
pip install -U numpy
pip install tornado
```

Install python libs
```
sudo python3 python_libs_install.py
```

Switch to superuser
```
su
```

Install additional python libs
```
pip install scikit-build
pip install cmake
```

Make
```
make
```

Exit superuser
```
exit
```

Make as user
```
make user
```

Launch application
```
pysimCoder
```

It is now possible to generate a docker container and image to run pysimCoder:

Install docker (see https://docs.docker.com/engine/install/ubuntu/).

Enter the pysimCoder folder and launch
```
docker build  -t pysimc ."

set DISPLAY=<your net address>   (example set DISPLAY=192.168.178.109)
docker run -it --env="DISPLAY" --net=host pysimc
```

In the bash launch:
```
make -f make4docker.mak
source ~/.bashrc
psc
```
I've tested this chain under Debian bookworm by installing the bullseye version of docker



