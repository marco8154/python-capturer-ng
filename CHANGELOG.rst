Changelog
=========

The purpose of this document is to list all of the notable changes to this
project. The format was inspired by `Keep a Changelog`_. This project adheres
to `semantic versioning`_.

.. contents::
   :local:

.. _Keep a Changelog: http://keepachangelog.com/
.. _semantic versioning: http://semver.org/

`Release 4.0`_ (unreleased)
---------------------------

This is the first release of the continuation of :pypi:`capturer`, published
on PyPI as :pypi:`capturer-ng`. The import name is still ``capturer`` and the
API and behavior are unchanged, so it works as a drop-in replacement. Don't
install it next to the original distribution: both ship the same files.

The original author Peter Odding is not involved in this continuation. License
(MIT) and copyright are unchanged. The continuation is maintained by one person
with AI agents, without independent review (see the readme).

**Noteworthy changes:**

- Restored compatibility with Python 3.14 and newer, where the default start
  method of ``multiprocessing`` on Linux is no longer ``fork``.
  Capturing failed with a ``TypeError`` there and could leave the process
  hanging. The ``fork`` start method is now requested explicitly (pull request
  `#16`_ by Scott K Logan).

- Python 3.10 is now the oldest supported version (this is backwards
  incompatible, which is why the major version number was bumped). Python 3.10
  up to 3.15 are tested.

- The requirement on :pypi:`humanfriendly` changed to :pypi:`humanfriendly-ng`.

**Internal changes:**

- The package is built with ``pyproject.toml``, tested with GitHub Actions on
  Linux and macOS and released through PyPI Trusted Publishing.

.. _#16: https://github.com/xolox/python-capturer/pull/16
.. _Release 4.0: https://github.com/marco8154/python-capturer-ng/compare/3.0...4.0

`Release 3.0`_ (2020-03-07)
---------------------------

This is a maintenance release that updates the supported Python
versions, adds a changelog and makes some minor internal changes:

- Added support for Python 3.7 and 3.8.
- Dropped support for Python 2.6 and 3.4.
- Actively deprecate ``interpret_carriage_returns()``.
- Moved test helpers to :mod:`humanfriendly.testing`.
- Include documentation in source distributions.
- Use Python 3 for local development (``Makefile``).
- Restructured the online documentation.
- Updated PyPI domain in documentation.
- Added this changelog.

.. _Release 3.0: https://github.com/xolox/python-capturer/compare/2.4...3.0

`Release 2.4`_ (2017-05-17)
---------------------------

- Allow capturing output without relaying it.
- Make ``OutputBuffer.flush()`` more robust.
- Add Python 3.6 to supported versions.

.. _Release 2.4: https://github.com/xolox/python-capturer/compare/2.3...2.4

`Release 2.3`_ (2016-11-12)
---------------------------

- Clearly document supported operating systems (`#4`_).
- Start testing Python 3.5 and Mac OS X on Travis CI.
- Start publishing wheel distributions.
- PEP-8 and PEP-257 checks.

.. _Release 2.3: https://github.com/xolox/python-capturer/compare/2.2...2.3
.. _#4: https://github.com/xolox/python-capturer/issues/4

`Release 2.2`_ (2016-10-09)
---------------------------

Switch to :func:`humanfriendly.terminal.clean_terminal_output()`.

.. _Release 2.2: https://github.com/xolox/python-capturer/compare/2.1.1...2.2

`Release 2.1.1`_ (2015-10-24)
-----------------------------

Make it easier to run test suite from PyPI release (fixes `#3`_).

.. _Release 2.1.1: https://github.com/xolox/python-capturer/compare/2.1...2.1.1
.. _#3: https://github.com/xolox/python-capturer/issues/3

`Release 2.1`_ (2015-06-21)
---------------------------

Make "nested" output capturing work as expected (issue `#2`_).

.. _Release 2.1: https://github.com/xolox/python-capturer/compare/2.0...2.1
.. _#2: https://github.com/xolox/python-capturer/issues/2

`Release 2.0`_ (2015-06-18)
---------------------------

Experimental support for capturing stdout/stderr separately (issue `#2`_).

.. _Release 2.0: https://github.com/xolox/python-capturer/compare/1.1...2.0
.. _#2: https://github.com/xolox/python-capturer/issues/2

`Release 1.1`_ (2015-06-16)
---------------------------

- Expose captured output as file handle (wiht shortcuts for saving to files).
- Improve documentation of ``interpret_carriage_returns()``.
- Clearly document drawbacks of emulating a terminal.

.. _Release 1.1: https://github.com/xolox/python-capturer/compare/1.0...1.1

`Release 1.0`_ (2015-06-14)
---------------------------

This was the initial release.

.. _Release 1.0: https://github.com/xolox/python-capturer/tree/1.0
