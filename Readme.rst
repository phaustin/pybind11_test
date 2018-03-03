Basic install/test for pybind11 with miniconda3 4.10 and conda build

To build and test with pip (osx):

https://raw.githubusercontent.com/phaustin/pybind11_test/osx/environment_osx.yml

conda env create environment_osx.yml

conda activate test

CXX=$(which $CXX);pip install git+https://github.com/phaustin/pybind11_test.git@osx#egg=pybind_test

python -c 'from hello_pybind.do_add import add_them;print(add_them(1,2))'

prints::

  inside hello_pybind __init__.py
  3








