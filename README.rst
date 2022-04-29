
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

   make build

Happy network analysis! 

Documentation
--------------

To use the built-in methods, import package by using this: ::

   from tsupy import tsubasa

Methods:

Init(): Initiate the data structures for future network construction (in-memory).

InitDB([database-name], [database-pwd]): Initiate the data structures for future network construction. The statistics after sketch will be stored in database.

ReadFilesByLocation([path-to-data], [locations-range-file]): Read data from the specific directory, which contains all NetCDF files. The seconds argument is the file containing the information to limit the locations. For example, 120,170,-5,5 denotes min longitude, max longitude, min latitude and max latitude, respectively.

GetTimeSeriesNum(): After reading data from the files, the users can use this method to get the total number of time series.

GetTimeSeriesLength(): After reading data from the files, the users can use this method to get the length of time series.

SetBasicWindowSize([integer]): Set the size of basic window.

Sketch(): Sketch all time series with a specific basic window size.

GetCorrelationMatrix([query-window-start-index], [query-window-length]) -> [correlation-matrix]: This is the query function to construct the correlartion matrix. The first argument is the start index of the query window, and the second argument is the total length of query window (the number of basic windows in this query window).

GetNetworkUnweighted([query-window-start-index], [query-window-length], [thres]) -> [unweighted-correlation-matrix]: This is the query function to construct the unweighted correlartion matrix. The first argument is the start index of the query window, and the second argument is the total length of query window (the number of basic windows in this query window). The third argument is the threshold, which is a float value in the range of [0, 1]

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
