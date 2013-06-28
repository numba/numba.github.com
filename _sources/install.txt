.. _custom:

Custom Python Environments
==========================

If you're not using anaconda, you will need LLVM with RTTI enabled:

* Compile LLVM 3.2

.. code-block:: bash

    $ wget http://llvm.org/releases/3.2/llvm-3.2.src.tar.gz
    $ tar zxvf llvm-3.2.src.tar.gz
    $ ./configure --enable-optimized
    $ # Be sure your compiler architecture is same as version of Python you will use
    $ #  e.g. -arch i386 or -arch x86_64.  It might be best to be explicit about this.
    $ REQUIRES_RTTI=1 make install

* Installing Numba

.. code-block:: bash

    $ git clone https://github.com/numba/numba.git
    $ cd numba
    $ pip install -r requirements.txt
    $ python setup.py install

or simply

.. code-block:: bash

    $ pip install numba

**NOTE:** Make sure you install *distribute* instead of setuptools. Using setuptools
          may mean that source files do not get cythonized and may result in an
          error during installation.
