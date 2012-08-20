Apple iCal integration with HTML website
########################################
:date: 2010-11-14 15:21
:category: Django

.. raw:: html

   <p>

Currently i work in a customer service outsourcing company, where we use
a system called TotalView for taskforce management. This means that
every agent can log into this system and check when they have to work
and how they are doing while they work. I like the concept, however it
is really annoying that i have to check both my own calendar and
TotalView. I've been considering to manually insert the data - but why
not make a system that does it automatically? This means, that i've
spent the last 4 hours making a system, that collects all relevant data
from TotalView for the current and the next month and delivers it in the
iCalendar format, which is compatible with all major calendar apps. The
system is (of course) made with `django`_ and I'm using a library for
`parsing the HTML`_\ and one for `formatting the iCalendar output`_.
Here is the code:

.. raw:: html

   <script src="http://pastebin.com/embed_js.php?i=JPyG4cne"></script>

.. raw:: html

   </p>

.. _django: http://www.djangoproject.com
.. _parsing the HTML: http://www.crummy.com/software/BeautifulSoup/
.. _formatting the iCalendar output: http://codespeak.net/icalendar/
