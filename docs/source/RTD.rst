Sphinx and Readthedocs Tutorial
===============================

On this page, you will find the steps for how to edit a Readthedocs site that uses Sphinx. The setup process of this site is already complete so
this page with focus on adding content to the site. If you would like to make a new a site from scratch, please see the video below:

.. raw:: html

   <iframe width="560" height="315" src="https://www.youtube.com/embed/oJsUvBQyHBs" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>


Setting up the Github Repository
--------------------------------

The first thing you will need in order to contribute to the repo is access to the repo itself. To do this, someone with the MUNsdh account credentials will have to navigate
to `https://github.com/MUNsdh/readthedocs/settings/access <https://github.com/MUNsdh/readthedocs/settings/access>`_ and add your Github account to the list
of collaborators.

Next, you will need to download Git from `https://git-scm.com/downloads <https://git-scm.com/downloads>`_.

Once Git is downloaded, you will need a promt that is running Python. An example would be Anaconda which can be downloaded from here:
`https://www.anaconda.com/products/individual <https://www.anaconda.com/products/individual>`_

You can open the prompt by searching Anaconda on your device and opening the following program:

.. figure:: ../_static/images/RTD1.PNG
    :figwidth: 500px
    :target: ../_static/images/RTD1.PNG


Next, navigate to the drive that the promt opens in. It is usally the **C** drive. In the drive make a folder and name it whatever you like, in our example,
it will be named "Github". This is where the files for the website will be stored.

When you first open up the promt, you will be in your users directory folder, so in order to get to the folder you just created, type in the follow commands in
the order listed:

.. code-block::

   1. cd/
   2. cd Github

.. figure:: ../_static/images/RTD2.PNG
    :figwidth: 500px
    :target: ../_static/images/RTD2.PNG

**Replace Github with whatever you named your folder**

Now type in **"git clone https://github.com/MUNsdh/readthedocs"**. This will copy the files from the repo onto your device in the folder you just made.

Creating a Document
-------------------

You can now begin creating a document that will be added to the site. The documents for this site use Restructured Text (rst) files. To see examples of how these files are
written, simply navigate to the folder where you cloned the repo and go to **readthedocs > docs > source**. Now, open any of the .rst with your text editor of choice (Ex. Notepad,
Notepad++, Vim, etc.)

To being creating a doucment of your own, make sure your prompt is open and make sure you are in the "source" directory. Type the following commands in the order listed:

.. code-block::

   1. cd/
   2. cd Github/readthedocs/docs/source

**Replace Github with whatever you named your folder**

You now need to make a RST file. Type the follow command: **"echo > "name of your document".rst"**

This will make a blank RST file in the source folder that you can now edit with a text editor.

To make the RST file appear on your page, you will need to give it a title in the document itself using the following format:

.. figure:: ../_static/images/RTD3.PNG
    :figwidth: 500px
    :target: ../_static/images/RTD3.PNG

It is the title of your page underlined lined by equal signs (=).

To create sub headings, do the same thing but instead unline the text with dashes (-).

**For more examples, simply open one of the documents that is already completed in the source folder.**

Now add you need to add the **TITLE OF THE FILE** to the toctree. To do this, open the file **"index"** in the source folder and add the name of the file to
the list in the same format as the names already listed. **It is important to note that the indent before the names is THREE spaces**.

.. figure:: ../_static/images/RTD4.PNG
    :figwidth: 500px
    :target: ../_static/images/RTD4.PNG

**Make sure to save this file after you add in the title.**


Adding content to the page is as simple as just typing. The syntax for formatting the text (adding bullet points, bold, hyperlinks, etc.) can be seen
in one of the already completed RST files or by going to `this link <https://thomas-cokelaer.info/tutorials/sphinx/rest_syntax.html>`_.

Adding Photos
-------------
Make sure that the you put the image you want in your document in the "images" folder which can be found in **readthedocs > docs > _static > images**

To add photos to the document use the following text in your document:

.. code-block::

   .. figure:: ../_static/images/nameofyourimage.PNG
       :figwidth: 500px

Ensure that you have the correct name of the image along with the correct file type. If you are unsure of the file type, simply left click on the image and click
properties.

**Once again, if you need help with this simply view one of the already made RST files in the source folder**

Testing the site
----------------

To test the site before commiting it to Github, you must navigate to the docs directory by typing the following commands in the prompt:

.. code-block::

   1. cd/
   2. cd Github/readthedocs/docs

**replace Github with the name of your folder**

From here type the following command in the prompt:

.. code-block::

   make html

This will make an html file located in **build > html**. To open this file, simply navigate to the folder and open it with a browser, or do the following commands
**while in the docs directory on the prompt**

.. code-block::

   cd build/html
   index.html

This will open the site in your default browser.

Pushing to Github
-----------------

Once the you are ready to publish your changes to the website, you must navigate to the readthedocs directory in the prompt by typing the commands:

.. code-block::

   1. cd/
   2. cd Github/readthedocs

**Once again you may have to repalce "Github" with whatever you named your folder**

Now, you may need to type **git pull** to ensure that your repo is up to date. At this step, it may ask you to log in so, ensure you do so with the account that was added
as a contrinutor to the repo.

Finally, to commit your work to the site, simply type following commands in the order below:

.. code-block::

   1. git add docs
   2. git commit -m "you message here"
   3. git push

Your first time pushing, you will most likely have to log in so, ensure it is with the account that is listed as a contributor.

Once you push your work with no errors appearing, you are done! This Github repo is already automatically connected the readthedocs site, so your changes should appear
within a few minutes!

If you are having any problems with syntax, it is recommended to simply view the other RST files in the repo as they all contain examples of different text formatting
and other feautes in reStructured Text. You can also check out these two ressources for more info on Readthedocs and Sphinx:

* `https://docs.readthedocs.io/en/stable/ <https://docs.readthedocs.io/en/stable/>`_
* `https://sublime-and-sphinx-guide.readthedocs.io/en/latest/index.html <https://sublime-and-sphinx-guide.readthedocs.io/en/latest/index.html>`_






