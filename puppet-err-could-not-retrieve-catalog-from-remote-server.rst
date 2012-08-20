Puppet: err: Could not retrieve catalog from remote server
##########################################################
:date: 2011-01-13 20:50
:category: Sysadm

.. raw:: html

   <p>

Yesterday i found `Puppet`_ and shortly after i bought the book `Pulling
Strings With Puppet`_. I got up and running with a few test machines
(while reading the book) within a couple of hours and i managed to do
some basic stuff. Furthermore i installed puppet-dashboard, an overall
pretty undocumented process. Maybe I'll write a post about this later.
However, i used many hours trying to debug this really annoying error:

::

    err: Could not retrieve catalog from remote server: Error 400 on
    SERVER: Could not find class nginx in namespaces <class> at 
    /etc/puppet/manifests/classes/<class>.pp:3 on node <fqdn>

I got this error after installing the nginx module, from "module forge"
- by install i mean git clone the github page. I put in into
/etc/puppet/modules/ and after adding nginx to a class, i was stuck with
this error. The solution, however, is really simple. When you clone the
nginx module, the directory is called puppet-nginx - you need to rename
it, so its called nginx and nothing else. This will remove this error. I
googled this thing for hours, hopefully this will be #1 next time
someone experience this. Please comment if you use Puppet and saw this
article! :-)

.. raw:: html

   </p>

.. _Puppet: http://www.puppetlabs.com/puppet/introduction/
.. _Pulling Strings With Puppet: http://www.apress.com/book/view/1590599780
