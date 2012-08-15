numba is a NumPy aware dynamic compiler for Python.  It creates LLVM bit-code from Python syntax and then creates a wrapper around that bitcode to call from Python

Example
=======

.. code-block:: python

   from numba import double
   from numba.decorators import jit

   @jit(arg_types=[double[:,:]], ret_type = double)
   def sum2d(arr):
       M, N = arr.shape
       result = 0.0
       for i in range(M):
           for j in range(N):
               result += arr[i,j]


QuickStart
==========

 * Get llvmpy at http://www.llvmpy.org
 * Get and install numba

.. code-block:: bash

   git clone https://github.com/numba/numba.git
   cd numba 
   git submodule init 
   git submodule update
   python setup.py install

This project is maintained by `Continuum Analytics <http://www.continuum.io>`_

.. toctree::
   :hidden:

   doc
   download
