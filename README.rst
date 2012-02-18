Template files to bootstrap a Python projects distribution
==========================================================

It includes:

- a heavily commented "fill-in the blanks" setup.py file with sane defaults and recommandations so you don't have spend another couple of hours to figure the parameters out.
- a basic .gitignore file specialized for Python and ignoring setuptools generated files

How to install
===============

No install. Just copy all the files except this README. Recommanded layout:

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

Edit setup.py, filling-in the blanks. Follow the instructions in comments.

Once your done, you can register your project::

     python setup.py register

It ask you what you want to go. Create an account if you don't have one an re run the command. Then identity, and it should upload.

Then generate the distribution and upload it::

     python setup.py sdist 

Then upload it::
     
     python setup.py sdist upload

Sometimes uploading fails, in that case you can just upload the archive you created with `python setup.py sdist" manually on the pypi website. It's just a form to fill.

