
====================
Tsupy
====================

.. image:: https://img.shields.io/pypi/pyversions/brainspace
   :alt: PyPI - Python Version



Tsupy is a toolbox primarily intended for dynamic network construction and analysis. It is a Python binding for the tsubasa Go library.

Install
-----------

To install the package successfully, first install `gopy <https://github.com/go-python/gopy>`_. Then, make sure you have the `netCDF C library <https://downloads.unidata.ucar.edu/netcdf/>`_ is installed.

To compile the package, run this inside tsupy directory: ::

   `make build`

Happy network analysis! 

Documentation
--------------

To use the built-in methods, import package by using this: ::

   `from tsupy import tsubasa`

License
-----------

The Tsupy source code is available under the MIT license.

Support
-----------

If you have problems installing the software or questions about usage 
and documentation, or something else related to Tsupy, 
you can post to the Issues section of our `repository <https://github.com/js061/tsupy/issues>`_.

Paper
-----------

If you consider using Tsupy, please cite our manuscript: 


Core development team
-----------------------

* Jinshu Liu - University of Rochester
* Draco(Yunlong) Xu - University of Rochester
* Fatemeh Nargesian - University of Rochester
