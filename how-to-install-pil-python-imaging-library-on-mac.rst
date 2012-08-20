How to install PIL (Python Imaging Library) on Mac
##################################################
:date: 2011-02-12 13:02
:category: Django, Mac

I often get the error "ImportError: No module named PIL", when using
ImageFields in django. I had my current mac for about 2 years and i
never found out how to install PIL. Today, however, i really needed it
and i found this `amazing fix`_. In case this perfect description will
be deleted, I've inserted it below for my own reference. **Full credits
to p16blog.com** Execute the following code
``cd /Library/Frameworks sudo ln -s /System/Library/Frameworks/Python.framework/ Python.framework``
`Download`_ and install PIL Remember to add PIL to PYTHONPATH
``export PYTHONPATH=/Library/Frameworks/Python.framework/Versions/2.5/lib/python2.5/site-packages/``
*(should be added to your startup script, e.g. ~/.bash\_profile)*

.. _amazing fix: http://www.p16blog.com/p16/2008/05/appengine-installing-pil-on-os-x-1053.html
.. _Download: http://pythonmac.org/packages/py25-fat/index.html
