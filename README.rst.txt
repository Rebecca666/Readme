DCDAI & Contract Digitalization
================

.. image:: https://travis-ci.org/madmaze/pytesseract.svg
    :target: https://travis-ci.org/madmaze/pytesseract
    :alt: Travis build status

.. image:: https://img.shields.io/pypi/pyversions/pytesseract.svg
   :target: https://pypi.python.org/pypi/pytesseract
   :alt: Python versions

.. image:: 	https://img.shields.io/github/release/madmaze/pytesseract.svg
   :target: https://github.com/madmaze/pytesseract/releases
   :alt: Github release

.. image:: https://img.shields.io/pypi/v/pytesseract.svg?color=blue
   :target: https://pypi.python.org/pypi/pytesseract
   :alt: PyPI release

.. image:: https://img.shields.io/conda/vn/conda-forge/pytesseract.svg?color=blue
   :target: https://anaconda.org/conda-forge/pytesseract
   :alt: Conda release

Python-tesseract is an optical character recognition (OCR) tool for python.
That is, it will recognize and "read" the text embedded in images.

Python-tesseract is a wrapper for `Google's Tesseract-OCR Engine <https://github.com/tesseract-ocr/tesseract>`_.
It is also useful as a stand-alone invocation script to tesseract, as it can read all image types
supported by the Pillow and Leptonica imaging libraries, including jpeg, png, gif, bmp, tiff,
and others. Additionally, if used as a script, Python-tesseract will print the recognized
text instead of writing it to a file.

USAGE
-----

*Note*: The following codes show how to run DCDAI in command line.

**Quick Start**

.. code-block:: python

    # General Usage
    python ochestrator.py -h

    # Specify System Used (default is ist; test system)
    python ochestrator.py -o isp ...` or `python ochestrator.py --sytem isp ...`

    # Download PDF from CMS API
    python ochestrator.py -d -t [directory with PDFs are stored]

    # Run PredExt on downloaded PDFs
    python ochestrator.py -xw -t [directory with PDFs are stored]

    # Write existing results to CMS
    python ochestrator.py -w -p [existing results object]

    # Write the entire process
    python ochestrator.py -dxw -i [Consumer ID]

    # Run PredExt on first 10 cases of downloaded PDFs
    python ochestrator.py -x -t test/dcd_engine/100_test_docs -s 0 -e 10

    # Write results of first 10 cases of downloaded PDFs
    python ochestrator.py -xw -t test/dcd_engine/100_test_docs -s 0 -e 10

**Parameters**


``python ochestrator.py -o -d -x -w -i -p -s -e``

* **-o** download document from CMS API, default="ist"p'
* **-d** download document from CMS API
* **-x** make prediction/extraction
* **-w** write back to DCD AI table
* **-i** specify a consumer ID
* **-t** specify a directory with PDF documents
* **-p** provide a payload to write
* **-s** start index of selected case in ordered metadata list
* **-e** end index of selected case in ordered metadata list; end not included



INSTALLATION
------------

Prerequisites:

- Python-tesseract requires Python 2.7 or Python 3.5+
- You will need the Python Imaging Library (PIL) (or the `Pillow <https://pypi.org/project/Pillow/>`_ fork).
  Under Debian/Ubuntu, this is the package **python-imaging** or **python3-imaging**.
- Install `Google Tesseract OCR <https://github.com/tesseract-ocr/tesseract>`_
  (additional info how to install the engine on Linux, Mac OSX and Windows).
  You must be able to invoke the tesseract command as *tesseract*. If this
  isn't the case, for example because tesseract isn't in your PATH, you will
  have to change the "tesseract_cmd" variable ``pytesseract.pytesseract.tesseract_cmd``.
  Under Debian/Ubuntu you can use the package **tesseract-ocr**.
  For Mac OS users. please install homebrew package **tesseract**.

  *Note:* Make sure that you also have installed ``tessconfigs`` and ``configs`` from `tesseract-ocr/tessconfigs <https://github.com/tesseract-ocr/tessconfigs>`_ or via the OS package manager.

| Installing via pip:

Check the `pytesseract package page <https://pypi.python.org/pypi/pytesseract>`_ for more information.

.. code-block:: bash

    $ (env)> pip install pytesseract

| Or if you have git installed:

.. code-block:: bash

    $ (env)> pip install -U git+https://github.com/madmaze/pytesseract.git

| Installing from source:

.. code-block:: bash

    $> git clone https://github.com/madmaze/pytesseract.git
    $ (env)> cd pytesseract && pip install -U .

| Install with conda (via `conda-forge <https://anaconda.org/conda-forge/pytesseract>`_):

.. code-block:: bash

    $> conda install -c conda-forge pytesseract

TESTING
-------

To run this project's test suite, install and run ``tox``. Ensure that you have ``tesseract``
installed and in your PATH.

.. code-block:: bash

    $ (env)> pip install tox
    $ (env)> tox

LICENSE
-------
Check the LICENSE file included in the Python-tesseract repository/distribution.
As of Python-tesseract 0.3.1 the license is Apache License Version 2.0

CONTRIBUTORS
------------
- Originally written by `Samuel Hoffstaetter <https://github.com/h>`_
- `Juarez Bochi <https://github.com/jbochi>`_
- `Matthias Lee <https://github.com/madmaze>`_
- `Lars Kistner <https://github.com/Sr4l>`_
- `Ryan Mitchell <https://github.com/REMitchell>`_
- `Emilio Cecchini <https://github.com/ceccoemi>`_
- `John Hagen <https://github.com/johnthagen>`_
- `Darius Morawiec <https://github.com/nok>`_
- `Eddie Bedada <https://github.com/adbeda>`_
