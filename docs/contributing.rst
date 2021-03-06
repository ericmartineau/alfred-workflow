
.. _contributing:

============
Contributing
============

Alfred-Workflow is an open-source project and contributions are welcome.

.. important::

    **Do not submit a feature request for Python 3 support**

    Alfred-Workflow is targeted at the system Python installed on macOS.
    I will not consider adding Python 3 support until it's installed
    by default on macOS.

    A *pull request* with Python 3 support, however, would be gratefully
    accepted.


.. _bugs:

Feature requests and bugs
=========================

If you have a bug report or a feature request, please create a new
`issue on GitHub`_.


.. _pull-requests:

Pull requests
=============

If you'd like to submit a pull request, please observe the following:

- Please open pull requests against the ``develop`` branch. I try to keep
  ``master`` in sync with the latest release (at least regarding any files
  included in releases). ``master`` and ``develop`` are *usually* in sync,
  but if I'm working on new features, they'll be in ``develop`` and won't
  be pushed to ``master`` until they're ready for release.
- Alfred-Workflow has very close to 100% test coverage. "Proof-of-concept"
  pull requests without tests are more than welcome. However, please be to
  add the appropriate tests if you want your pull request to be ultimately
  accepted.
- Complete coverage is *only a proxy* for decent tests. Tests should also
  cover a decent variety of valid/invalid input. For example, if the code
  *could potentially* be handed non-ASCII input, it should be tested with
  non-ASCII input.
- Code should be `PEP8`_-compliant as far as is reasonable. Any decent code
  editor has a PEP8 plugin that will warn you of potential transgressions.
- Please choose your function, method and argument names carefully, with an
  eye to the existing names. Obviousness is more important than brevity.
- Document your code using the `Sphinx ReST format`_. Even if your
  function/method isn't user-facing, some other developer will be looking at
  it. Even if it's only a one-liner, the developer may be looking at
  :ref:`the API docs <api>` in a browser, not at the source code.
  If you don't feel comfortable writing English, I'd be happy to write the
  docs for you, but please ensure the code is easily understandable (i.e. comment the code if it's not totally obvious).
- Performance counts. By default, Alfred will try to run a workflow anew on
  every keypress. As a rule, 0.3 seconds execution time is decent, 0.2
  seconds or less is smooth. Alfred-Workflow should do its utmost to
  consume as little of that time as possible.

The main entry point for unit testing is the ``run-tests.sh`` script in the root directory. This will fail *if code coverage is < 100%*. Travis-CI also uses this script. Add `# pragma: no cover` with care.


.. _questions:

Questions and help
==================

If you have feedback or a question regarding Alfred-Workflow, please post in
the `Alfred forum thread`_.



.. _Alfred forum thread: http://www.alfredforum.com/topic/4031-workflow-library-for-python/
.. _GitHub: https://github.com/deanishe/alfred-workflow/
.. _Python Package Index: https://pypi.python.org/pypi/Alfred-Workflow
.. _issue on GitHub: https://github.com/deanishe/alfred-workflow/issues
.. _pip: https://pypi.python.org/pypi/pip
.. _PEP8: http://legacy.python.org/dev/peps/pep-0008/
.. _Sphinx ReST format: http://sphinx-doc.org/
