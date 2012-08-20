Python rounding to 05
#####################
:date: 2011-08-29 13:55
:category: Python

Here in Switzerland they decided (for some reason, that can't be good)
not to pay the correct amount, but round it to the nearest 0/5 cent -
which is a pain when doing python stuff. Therefore i made a Decimal
rounding function for python, check it out:

.. code-block:: python

    from decimal import Decimal, ROUND_HALF_UP
    
    def decimal_round(d, digits=0, to_five=True):
        if to_five:
            d = (d/Decimal("5"))
        d = d.quantize(Decimal("1") / (Decimal('10') ** digits), rounding=ROUND_HALF_UP)
        if to_five:
            d = d * Decimal("5")
        return d
