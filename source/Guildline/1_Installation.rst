Installation
++++++++++++++
.. ========================
.. --------------------------------
.. ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. caution:: 
   Because JunPy is written by python and C++, 
   we suggest running JunPy under linux envirement and anaconda will be more convenient to compile

Install for linux
========================

.. Caution:: 
      If you want to install junpy in the public folder in linux, please change the status to root::
      
            sudo su      
      
      which means the direction of the junpy's environment in step 4 may just be like ``/opt/anaconda/envs/.`` 
      If junpy just be installed in personal folder in linux, the direction may just be ``~/.conda/envs``

#. Copy JunPy file in to linux system
#. Direct to ./tools direction which has the file ``environment.yml``
#. Using anaconda or miniconda to create an envirement::

      conda env create -n <Envirement_Name> -f environment.yml

#. Goback to home direction of JunPy package
#. Activate the envirement::

      conda activate <Envirement_Name>

#. Confirm current environment::

      which pip

#. Enter following command in the terminal::
   
      export CC=gcc

#. Enter following command in the terminal::

      export CXX=g++

#. Enter following command in the terminal::
   
      pip install .

#. If it success, it will start to install......

#. After the installation, we can import junpy in python by using::

      import junpy as jp

.. Caution:: 
      If you cannot import JunPy, with error code::

                  from mpi3py import MPI
            ImportError: libmpi.so.12: cannot open shared object file: No such file or directioty

      which mean the version of mpi4py is too old to use. Please reinstall the package by following command::

            conda install -c conda-forge mpich

Notice
------------------
#. If you want to modify the content of JunPy, please enter the following command to enter the developer mode::

      python setup.py develop

After enter this command, all the revises of JunPy will be timely response to the imported package

#. We can also install JunPy through fowllowing command::
      
      python setup.py install

The relative content will be updated later, but we don't suggention this method.

 

Install for windows
========================
.. caution:: 
   Not sure will do or not