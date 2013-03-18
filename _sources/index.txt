numba is a NumPy aware dynamic compiler for Python.  It creates LLVM bit-code from Python syntax and then creates a wrapper around that bitcode to call from Python

Example
=======

.. code-block:: python

   from numba import autojit

   @autojit
   def sum2d(arr):
       M, N = arr.shape
       result = 0.0
       for i in range(M):
           for j in range(N):
               result += arr[i,j]
       return result

QuickStart
==========

The easiest way to get started with Numba is to either:

 1) download Anaconda, the free Python distribution, from here: http://continuum.io/downloads.html
 2) Get a Wakari account and interact on-line:  http://wakari.io

If you want to build things yourself, then this can help get you started: 

 * Get and install llvmpy at http://www.llvmpy.org
 * Get and install Meta
 * Get and install numba

.. code-block:: bash

   git clone https://github.com/numba/Meta.git
   cd meta
   python setup.py install
   git clone https://github.com/numba/numba.git
   cd numba 
   python setup.py install

This project is maintained by `Continuum Analytics <http://www.continuum.io>`_

.. toctree::
   :hidden:

   doc
   download
