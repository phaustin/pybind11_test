To build and test on linux
++++++++++++++++++++++++++

Using pip
=========

* Using miniconda3 4.10

* Download the environment::

    wget https://raw.githubusercontent.com/phaustin/pybind11_test/linux/environment_linux.yml

    conda env create -f environment_linux.yml

    conda activate test

    CXX=$(which $CXX);pip install git+https://github.com/phaustin/pybind11_test.git@linux#egg=pybind_test

    python -c 'from hello_pybind.do_add import add_them;print(add_them(1,2))'

  prints::

    inside hello_pybind __init__.py
    3


Using conda
===========

* clone the repo and checkout the osx branch::

    git clone https://github.com/phaustin/pybind11_test.git
    pip uninstall hello-pybind
    cd pyind11_test
    conda activate test
    conda build .

* should print out::

    running run_test.py
    inside hello_pybind __init__.py
    sum of 1 and 2: 3









