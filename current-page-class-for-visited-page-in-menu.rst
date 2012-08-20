Current page class, for visited page in menu
############################################
:date: 2011-01-01 20:16
:category: Django

.. raw:: html

   <p>

I found an outdated script on `djangosnippets`_, that doesn't work
anymore and updated it to work with the latest jquery version. Feel free
to comment with suggestions to improve it.

.. code-block:: javascript

    (function() {
        function main() {
        var nav  = $('.menu ul');
        var path = window.location.pathname.split('/').slice(1,-1);
        function act(p) {
            return nav.not(nav.find('li.active').parent()).find('li>a[href="/'+p+'"]').parent().addClass('active').length;
        }
        if (path.length)
        {
            for(; path.length; path.pop())
            {
            act(path.join('/')+'/');
            }
        } else
            act('');
        }
        $(document).ready(main);
    })()

.. raw:: html

   </p>

.. _djangosnippets: http://djangosnippets.org/snippets/435/
