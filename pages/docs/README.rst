How to Guide
============

Background (skip if you do not wish to know how this document website is created)
---------------------------------------------------------------------------------

**Get prerequisite**

.. code-block:: console

  sudo apt-get install -y python3-sphinx
  sudo apt-get install -y python3-sphinx-rtd-theme

**Create folder and setup sphinx site**

.. code-block:: console

  DIR_DOCS=${DIR_ASTRA_SIM_GITHUB_IO}/pages/docs
  cd ${DIR_DOCS}
  sphinx-quickstart

**Change theme to Read the Docs by editing ${DIR_DOCS}/conf.py**

  add 'sphinx_rtd_theme' and 'sphinx.ext.autodoc' to "extensions"

  change value of "html_theme" to 'sphinx_rtd_theme'

**Rebuild site**

.. code-block:: console

  cd ${DIR_DOCS}
  make clean && make html

**View locally**

.. code-block:: console

  firefox ${DIR_DOCS}/_build/html/index.html


Integration with project astra-sim.github.io
--------------------------------------------

**Make desired changes to this project content and then rebuild it by running:**

.. code-block:: console

  cd ${DIR_DOCS}
  make clean && make html

**View locally to validate the changes by running:**

.. code-block:: console

  firefox ${DIR_DOCS}/_build/html/index.html

**View locally to validate the changes on project astra-sim.github.io by running:** 

.. code-block:: console

  cd ${DIR_ASTRA_SIM_GITHUB_IO}
  bundle install
  bundle exec jekyll serve

  (Note: install prerequisite by following https://jekyllrb.com/docs/installation/)

Navigate to http://127.0.0.1:4000 

Commonly used structural syntax:
--------------------------------

**Bold**: place "**" around text 

**Italics**: place "*" around text

**Header**: place "===" below text

**Subheader**: place "---" below text

**Code-sample**: use "``" around text

**Code-block**: use ".. code-block:: console" and place codes below with a leading tab/indent

**Page-tree**: use ".. toctree::" and list pages below with a leading tab/indent

**Cross-reference-to-page**: to jump to a page by clicking text, use ":doc:`PAGE_NAME`", where PAGE_NAME is the actual page name

**Section-label**: to mark a section to be referenced by text, use ".. _SECTION_LABEL:", where SECTION_LABEL is named by you 

**Cross-reference-to-section**: to jump to a section by clicking text, use ":ref:`SECTION_NAME <SECTION_LABEL>`", where SECTION_NAME is the text for reader to click on and be brought to the place marked by SECTION_LABEL




For details, read the tutorial here:

https://docs.readthedocs.io/en/stable/tutorial/

https://www.sphinx-doc.org/en/master/usage/restructuredtext/index.html


