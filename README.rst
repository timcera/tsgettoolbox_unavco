.. image:: https://img.shields.io/coveralls/github/timcera/tsgettoolbox_unavco
    :alt: Test Coverage
    :target: https://coveralls.io/r/timcera/tsgettoolbox_unavco?branch=master
    :height: 20

.. image:: https://img.shields.io/pypi/v/tsgettoolbox_unavco
    :alt: Latest release
    :target: https://pypi.python.org/pypi/tsgettoolbox_unavco/
    :height: 20

.. image:: https://img.shields.io/pypi/l/tsgettoolbox_unavco
    :alt: BSD-3 clause license
    :target: https://pypi.python.org/pypi/tsgettoolbox_unavco/
    :height: 20

.. image:: https://img.shields.io/pypi/pyversions/tsgettoolbox_unavco
    :alt: PyPI - Python Version
    :target: https://pypi.org/project/tsgettoolbox_unavco/
    :height: 20

tsgettoolbox_unavco - Quick Guide
=================================
The 'tsgettoolbox_unavco' is a plugin-in for 'tsgettoolbox' that supplies
a command line interface and Python library to get time-series data from the
California Data Exchange Center (CDEC).  The tsgettoolbox_unavco will work with
Python and 3.10+.

Documentation
-------------
Reference documentation is at `tsgettoolbox_documentation`_.

Installation
------------
At the command line::

    $ pip install tsgettoolbox_unavco

    OR

    $ conda install -c conda-forge tsgettoolbox_unavco

Usage Summary - Command Line
----------------------------
Just run 'tsgettoolbox --help' to get a list of subcommands.  To get detailed
help for a particular sub-command, for instance 'unavco', type 'tsgettoolbox
unavco --help'.

+-------------+---------+--------+---------+----------+-----------------------+
| Sub-command | Spatial | Time   | Type    | Time     | Description           |
|             | Extent  | Extent |         | Interval |                       |
+=============+=========+========+=========+==========+=======================+
| unavco      | US      | varies | station | varies   | UNAVCO well data      |
+-------------+---------+--------+---------+----------+-----------------------+

Usage Summary - Python Library
------------------------------
To use the tsgettoolbox in a project::

    from tsgettoolbox import tsgettoolbox
    df = tsgettoolbox.unavco(
        "P005",
        "met",
        starttime="2012-05-01T00:00:00",
        endtime="2012-05-02T23:59:59",
    )
    print(df.head())

Refer to the API Documentation at `tsgettoolbox_api`_.

Usage Summary - Command Line
----------------------------

    tsgettoolbox unavco \
        "P005" \
        "met" \
        --starttime="2012-05-01T00:00:00" \
        --endtime="2012-05-02T23:59:59" > output.csv

Refer to the command line documentation at `tsgettoolbox_cli`_.

Development
~~~~~~~~~~~
Development is managed on bitbucket or github.
https://bitbucket.org/timcera/tsgettoolbox_unavco/overview.
https://github.com/timcera/tsgettoolbox_unavco

.. _tsgettoolbox_documentation: https://timcera.bitbucket.io/linked_pkg_dirs/tsgettoolbox/docs/index.html
.. _tsgettoolbox_api: https://timcera.bitbucket.io/linked_pkg_dirs/tsgettoolbox/docs/function_summary.html
.. _tsgettoolbox_cli: https://timcera.bitbucket.io/linked_pkg_dirs/tsgettoolbox/docs/command_line.html
