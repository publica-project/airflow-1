
 .. Licensed to the Apache Software Foundation (ASF) under one
    or more contributor license agreements.  See the NOTICE file
    distributed with this work for additional information
    regarding copyright ownership.  The ASF licenses this file
    to you under the Apache License, Version 2.0 (the
    "License"); you may not use this file except in compliance
    with the License.  You may obtain a copy of the License at

 ..   http://www.apache.org/licenses/LICENSE-2.0

 .. Unless required by applicable law or agreed to in writing,
    software distributed under the License is distributed on an
    "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY
    KIND, either express or implied.  See the License for the
    specific language governing permissions and limitations
    under the License.

``apache-airflow-providers-mysql``
==================================

Content
-------

.. toctree::
    :maxdepth: 1
    :caption: Guides

    Connection types <connections/mysql>
    Operators <operators>

.. toctree::
    :maxdepth: 1
    :caption: References

    Python API <_api/airflow/providers/mysql/index>

.. toctree::
    :maxdepth: 1
    :caption: Resources

    Example DAGs <https://github.com/apache/airflow/tree/main/airflow/providers/mysql/example_dags>

.. toctree::
    :maxdepth: 1
    :caption: Resources

    PyPI Repository <https://pypi.org/project/apache-airflow-providers-mysql/>

.. THE REMAINDER OF THE FILE IS AUTOMATICALLY GENERATED. IT WILL BE OVERWRITTEN AT RELEASE TIME!


.. toctree::
    :maxdepth: 1
    :caption: Commits

    Detailed list of commits <commits>


Package apache-airflow-providers-mysql
------------------------------------------------------

`MySQL <https://www.mysql.com/products/>`__


Release: 2.1.1

Provider package
----------------

This is a provider package for ``mysql`` provider. All classes for this provider package
are in ``airflow.providers.mysql`` python package.

Installation
------------

You can install this package on top of an existing airflow 2.1+ installation via
``pip install apache-airflow-providers-mysql``

PIP requirements
----------------

==========================  ==================
PIP package                 Version required
==========================  ==================
``apache-airflow``          ``>=2.1.0``
``mysql-connector-python``  ``>=8.0.11, <9``
``mysqlclient``             ``>=1.3.6,<3``
==========================  ==================

Cross provider package dependencies
-----------------------------------

Those are dependencies that might be needed in order to use all the features of the package.
You need to install the specified provider packages in order to use them.

You can install such cross-provider dependencies when installing from PyPI. For example:

.. code-block:: bash

    pip install apache-airflow-providers-mysql[amazon]


======================================================================================================  ===========
Dependent package                                                                                       Extra
======================================================================================================  ===========
`apache-airflow-providers-amazon <https://airflow.apache.org/docs/apache-airflow-providers-amazon>`_    ``amazon``
`apache-airflow-providers-presto <https://airflow.apache.org/docs/apache-airflow-providers-presto>`_    ``presto``
`apache-airflow-providers-trino <https://airflow.apache.org/docs/apache-airflow-providers-trino>`_      ``trino``
`apache-airflow-providers-vertica <https://airflow.apache.org/docs/apache-airflow-providers-vertica>`_  ``vertica``
======================================================================================================  ===========

Downloading official packages
-----------------------------

You can download officially released packages and verify their checksums and signatures from the
`Official Apache Download site <https://downloads.apache.org/airflow/providers/>`_

* `The apache-airflow-providers-mysql 2.1.1 sdist package <https://downloads.apache.org/airflow/providers/apache-airflow-providers-mysql-2.1.1.tar.gz>`_ (`asc <https://downloads.apache.org/airflow/providers/apache-airflow-providers-mysql-2.1.1.tar.gz.asc>`__, `sha512 <https://downloads.apache.org/airflow/providers/apache-airflow-providers-mysql-2.1.1.tar.gz.sha512>`__)
* `The apache-airflow-providers-mysql 2.1.1 wheel package <https://downloads.apache.org/airflow/providers/apache_airflow_providers_mysql-2.1.1-py3-none-any.whl>`_ (`asc <https://downloads.apache.org/airflow/providers/apache_airflow_providers_mysql-2.1.1-py3-none-any.whl.asc>`__, `sha512 <https://downloads.apache.org/airflow/providers/apache_airflow_providers_mysql-2.1.1-py3-none-any.whl.sha512>`__)

.. include:: ../../airflow/providers/mysql/CHANGELOG.rst
