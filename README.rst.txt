DCDAI
================

.. image:: https://img.shields.io/pypi/pyversions/pytesseract.svg
   :target: https://pypi.python.org/pypi/pytesseract
   :alt: Python versions

.. image:: 	https://img.shields.io/github/release/madmaze/pytesseract.svg
   :target: https://github.com/madmaze/pytesseract/releases
   :alt: Github release


DCD AI is known as Digital Contract Data Action Index. It is a text-based Machine Learning application, built for the legal domain. DCD AI is a tool to assist the SAP Legal Team in conducting document review on SAP Order Forms. With tens of thousands of English Order Forms yearly, the time required to conduct manual document review is simply not practical. SAP had to resort to third-party services for the manual review process, which brings up two main problems: cost, and challenges in ensuring data quality. Bad data quality could lead to Sales teams acquiring wrong information, which in turn affects chances of renewals and closing new deals.

USAGE
-----

**Quick Start**

*Note*: The following codes show how to run DCDAI in command line.

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


CONTRIBUTORS
------------

**Product Owner**

* Dr. Susanne Beckers <susanne.beckers@sap.com>

**Scrum Master**

* Ray Han <ray.han@sap.com>

**Developers**

- Ray Han <ray.han@sap.com>

- Traci Lim <traci.lim@sap.com>

- Lijie Quan <lijie.quan@sap.com>

- Rocco Hu <rocco.hu@sap.com>

- Lingxiao Liang <lingxiao.liang@sap.com>

- Joyce Jin [<joyce.jin01@sap.com>

- Xiao Rui <rui.xiao01@sap.com>

- Sandu, Venkata Narasimha Rao <venkata.narasimha.rao.sandu@sap.com>

