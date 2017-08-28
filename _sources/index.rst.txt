********************
Numba
********************

Numba gives you the power to speed up your applications with high performance functions written directly in Python.  With a few annotations, array-oriented and math-heavy Python code can be just-in-time compiled to native machine instructions, similar in performance to C, C++ and Fortran, without having to switch languages or Python interpreters.

Numba works by generating optimized machine code using the LLVM compiler infrastructure at import time, runtime, or statically (using the included pycc tool).  Numba supports compilation of Python to run on either CPU or GPU hardware, and is designed to integrate with the Python scientific software stack.

The Numba project is supported by Anaconda, Inc. (formerly known as Continuum Analytics) and `The Gordon and Betty Moore Foundation (Grant GBMF5423) <https://www.continuum.io/blog/developer-blog/gordon-and-betty-moore-foundation-grant-numba-and-dask>`_.

Example
=======

.. code-block:: python

    from numba import jit
    from numpy import arange

    # jit decorator tells Numba to compile this function.
    # The argument types will be inferred by Numba when function is called.
    @jit
    def sum2d(arr):
        M, N = arr.shape
        result = 0.0
        for i in range(M):
            for j in range(N):
                result += arr[i,j]
        return result

    a = arange(9).reshape(3,3)
    print(sum2d(a))

More examples: `examples <http://numba.pydata.org/numba-doc/dev/user/examples.html>`_.

Documentation
=============

* http://numba.pydata.org/doc.html

Source and Downloads
====================

* Github: https://github.com/numba/numba

.. code-block:: bash

    $ git clone git://github.com/numba/numba.git

.. _install_frontpage:

For tarballs see:

.. toctree::
    :titlesonly:
    :maxdepth: 2

    download.rst

.. :ref:`Download Numba <download>`

Installing
==========

The easiest way to install numba and get updates is by using the Anaconda
Distribution: http://anaconda.com/downloads.html

If you have Anaconda installed already:

.. code-block:: bash

    $ conda install numba

or

.. code-block:: bash

   $ conda update numba

For custom python environments see the `README on Github <https://github.com/numba/numba#custom-python-environments>`_.

Mailing Lists
=============

Join the numba mailing list numba-users@continuum.io :

* https://groups.google.com/a/continuum.io/d/forum/numba-users

Some old archives are at:

* http://librelist.com/browser/numba/

Website
=======

See if our sponsor can help you (which can help this project):

* http://www.anaconda.com
* http://numba.pydata.org

Continuous Integration
======================

* https://travis-ci.org/numba/numba

