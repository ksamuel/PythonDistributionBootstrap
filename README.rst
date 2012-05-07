Template files to bootstrap a Python projects distribution
==========================================================

It includes:

- a heavily commented "fill-in the blanks" setup.py file with sane defaults and 
  recommandations so you don't have spend another couple of hours to figure 
  the parameters out.
- a basic .gitignore file specialized for Python and ignoring setuptools generated files.

Notable benefits:

- sharing small code targetting unix is just a few fields away;
- sharing code with static files is a no brainer;
- you should not need to change your code layout, and still import should work;
- all options are listed and documented, with all possible values is they exists.

How to install
===============

No install. Just copy all the files except this README. Recommanded project layout::

    --working dir (and VCS repo root)
      |__ all_your_code
      |__ setup.py
      |__ (optionaly) .gitignore
      |__ (optionaly) .git
      |__ (optionaly) README (yours, not this one)
      |__ (optionaly) licence.txt


It's not the most professional layout, but that's the most simple that works.

How to use ?
=============

Edit setup.py and fill-in the blanks. Follow the instructions in comments.

Once your done, you can register your project::

     python setup.py register

It should prompt you for what you want to do. Create an account if you don't have one an re run the command. Then identify, and it should upload.

If it doesn't, you can generate the distribution and upload it using these commands::

     python setup.py sdist      
     python setup.py sdist upload

Sometimes uploading fails, in that case you can just upload the archive you created with `python setup.py sdist" manually on the pypi website. It's just a form to fill.

What are the limitations ?
=========================

This template target unix users wanting to quickly share some code like a quick and dirty script or a django app. 

Anything more complicated can be done, but you will have to figure it out yourself, and that includes:

- commands for non unix operating system;
- compiled extensions;
- exotic layout;

Plus, it doesn't make the PYTHON PATH goes away. It just makes some simple decisions that usually lead to less problems.