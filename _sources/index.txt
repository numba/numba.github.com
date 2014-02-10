********************
Numba
********************

Numba is an just-in-time specializing compiler which compiles
annotated Python and NumPy code to LLVM (through decorators). Its goal
is to seamlessly integrate with the Python scientific software stack
and produce optimized native code, as well as integrate with native foreign
languages.

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

More examples: `examples <http://numba.pydata.org/numba-doc/dev/examples.html>`_.

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
Distribution: http://continuum.io/downloads.html

If you have anaconda installed already:

.. code-block:: bash

    $ conda install numba

or

.. code-block:: bash

   $ conda update numba

For custom python environments see:

.. toctree::
    :titlesonly:
    :maxdepth: 1

    install.rst

Mailing Lists
=============

Join the numba mailing list numba-users@continuum.io :

    * https://groups.google.com/a/continuum.io/d/forum/numba-users

Some old archives are at:

    * http://librelist.com/browser/numba/

Website
=======

See if our sponsor can help you (which can help this project):

    * http://www.continuum.io
    * http://numba.pydata.org

Continuous Integration
======================

* https://travis-ci.org/numba/numba

