===================
Jenkins Job Builder
===================

Jenkins Job Builder takes simple descriptions of Jenkins jobs in YAML format,
and uses them to configure Jenkins. You can keep your job descriptions in human
readable text format in a version control system to make changes and auditing
easier. It also has a flexible template system, so creating many similarly
configured jobs is easy.

To install::

    $ sudo python setup.py install

Online documentation:

* http://ci.openstack.org/jenkins-job-builder/

Developers
==========
Bug report:

* https://storyboard.openstack.org/#!/project/723

Cloning:

* https://git.openstack.org/openstack-infra/jenkins-job-builder

Patches are submitted via Gerrit at:

* https://review.openstack.org/

Please do not submit GitHub pull requests, they will be automatically closed.

More details on how you can contribute is available on our wiki at:

* http://docs.openstack.org/infra/manual/developers.html

Writing a patch
===============

We ask that all code submissions be pep8_ and pyflakes_ clean.  The
easiest way to do that is to run tox_ before submitting code for
review in Gerrit.  It will run ``pep8`` and ``pyflakes`` in the same
manner as the automated test suite that will run on proposed
patchsets.

When creating new YAML components, please observe the following style
conventions:

* All YAML identifiers (including component names and arguments)
  should be lower-case and multiple word identifiers should use
  hyphens.  E.g., "build-trigger".
* The Python functions that implement components should have the same
  name as the YAML keyword, but should use underscores instead of
  hyphens. E.g., "build_trigger".

This consistency will help users avoid simple mistakes when writing
YAML, as well as developers when matching YAML components to Python
implementation.

Installing without setup.py
===========================

For YAML support, you will need libyaml_ installed.

Mac OS X::

    $ brew install libyaml

Then install the required python packages using pip_::

    $ sudo pip install PyYAML python-jenkins

.. _pep8: https://pypi.python.org/pypi/pep8
.. _pyflakes: https://pypi.python.org/pypi/pyflakes
.. _tox: https://testrun.org/tox
.. _libyaml: http://pyyaml.org/wiki/LibYAML
.. _pip: https://pypi.python.org/pypi/pip
