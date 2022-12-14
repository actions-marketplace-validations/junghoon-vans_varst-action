============
varst-action
============

Github action to replace substitutions in rst file using varST_.

Example workflow
================

Refer example workflow if you want to replace substitutions in ``README.rst`` and push it to repository.

.. parsed-literal::

   steps:
     - uses: actions/checkout@v3
     - name: Replace substitution
     - uses: junghoon-vans/varst-action@\ |release|
       with:
         substitutions: "name=value"
     - uses: stefanzweifel/git-auto-commit-action@v4

Full example is |Sample Workflow|_.

Inputs
======

input-file
~~~~~~~~~~

**Optional**
The file path to read contents.

Default: ``./README.rst``

output-file
~~~~~~~~~~~

**Optional**
The file path to write contents.

Default: ``input-file``

substitutions
~~~~~~~~~~~~~

**Required**
A key-value of substitutions.

If multiple values need to be defined, use folded block scalar style.


.. code:: yml

   substitutions: >-
     'name1=value1'
     'name2=value2'
     ...

License
=======

`MIT
License <https://github.com/junghoon-vans/rst-substitution-action/blob/main/LICENSE>`__


.. _varST: https://github.com/junghoon-vans/varst
.. |release| replace:: v1.2.0

.. |Sample Workflow| replace:: here
.. _Sample Workflow: https://github.com/junghoon-vans/varst-action/blob/main/.github/workflows/bump-version.yml