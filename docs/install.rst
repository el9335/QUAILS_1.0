.. _install: 

============
Installation
============

This page will guide you through installing the Quails dependencies on a unix-based operating system.  Quails currently only supports python 2.7.6.  The next iteration will automatically install all dependencies.

These instructions were recorded over the process of development, but have not been tested on a fresh system.  If you run into any errors during the process, please send me an email at ``leblanc at drexel dot edu``.

1.  Install pip
::

	sudo apt-get install python-pip

2.  Install python-dev
::

	sudo apt-get install python-dev

3.  Install Python's ConfigParser
::

	sudo pip install configparser

4.  Install the Python Requests library
::
	
	sudo pip install requests

5.  Install the Flask RESTful server library
::
	
	sudo pip install flask

6.  Install Natural Language ToolKit
::
	
	sudo pip install nltk

7.  From the command line open a Python interpreter instance and enter the following lines:
::

	import nltk
	nltk.download('all')

Something in the nltk download script causes it to fail, so if/when it happens, just exit the interpreter.  The next version will include a workaround to shield the user from this issue.

8.  Install pexpect, unidecod, and jsonrpclib, all required to run the Stanford Core libraries.
::
	
	sudo pip install pexpect unidecode jsonrpclib

9.  Install git
::

	sudo apt-get install git

10. Install the corenlp-python library
::

	git clone https://bitbucket.org/torotoki/corenlp-python.git
	cd corenlp-python.git
	sudo python setup.py install

11. Install the Stanford Core NLP Jars (``sudo apt-get install wget`` if not already installed)
::

	wget http://nlp.stanford.edu/software/stanford-core-nlp-full-2014-08-27.zip
	unzip stanford-corenlp-full-2014-08-27.zip

12. Install numpy, scipy, and sklearn
::

	sudo apt-get install python-numpy python-scipy
	sudo pip install scikit-learn

13. Install whoosh text indexer for Python
::
	
	sudo pip install whoosh
