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

#. Copy JunPy file in to linux system
#. Direct to ./tools direction which has the file ``envirement.yml``
#. Using anaconda or miniconda to create an envirement::

      conda env create -n Envirement_Name -f envirement.yml

#. Goback to home direction of JunPy package
#. Activate the envirement::

      conda activate Envirement_Name

#. Confirm current environment::

      which pip

#. Enter following command in the terminal::
   
      export CC=gcc

#. Enter following command in the terminal::

      export CXX=g++

.. pip install .
#. Enter following command in the terminal::
   
      python setup.py install

#. If it success, it will start to install

.. Tip::
      If you want to modify the content of JunPy, please enter the following command to enter the developer mode::

            python setup.py develop
      
      After enter this command, all the revises of JunPy will be timely response to the imported package
.. caution::
      We can also install JunPy through fowllowing command::
            
            pip install .

      The relative content will be updated later

 

Install for windows
========================
.. caution:: 
   Not sure will do or not