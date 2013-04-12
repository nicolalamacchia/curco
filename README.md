Curco
=====

A dummy CLI currency converter based on
[ExchangeRates](http://rate-exchange.appspot.com/) by [Hippasus
Chu](https://github.com/hippasus/ExchangeRates) (based in turn on Google's
APIs).

Install
-------

Curco needs python (2 or 3).

Run

    # python setup.py install

N.B.: the `#` means that you must be root!

Features
--------

Curco allows you to write in a natural language, useful if you're used to the
Google search bar to convert values.  See the next section for details.

Conversion rates are cached for 3 hours (you can change this value changing
the `CACHEEXPHRS` variable assignment within the curco source code).

Usage by examples
-----------------

10 USD to EUR

    $ curco 10$ to eur
    10 USD = 7.64409112 EUR

    $ curco 10 $ eur
    10 USD = 7.64409112 EUR

    $ curco 10USD EUR
    10 USD = 7.64409112 EUR

    $ curco usd 10.0 to eur
    10 USD = 7.64409112 EUR

    $ curco usd eur
    USD / EUR = 0.764409112

    $ curco usd -\> eur
    USD / EUR = 0.764409112

and so on...

Curco can't read your mind, but will always try to do its best (although it's
far from being a genius).  Of course, nonsense stuff may generate unpredictable
output to you.

    $ curco 10 5$ to $ eur      # Ignores 5$
    10 USD = 7.64409112 EUR

    $ curco 10 20 usd eur       # Ignores 20
    10 USD = 7.64409112 EUR

    $ curco 10 000$ to eur      # Ignores 000$: missing a currency code
    Insert valid currency codes

    $ curco 10 000$ to € eur    # EUR to EUR conversion
    Insert valid currency codes

    $ curco 10,000.00 $ to eur
    10 USD = 7.64409112 EUR

    $ curco usd eur10
    10 USD = 7.64409112 EUR

    $ curco usd 10 20 €
    10 USD = 7.64409112 EUR

    $ curco usd 10 20€          # Ignores 20€
    Insert valid currency codes

    $ curco $ eUr 10
    10 USD = 7.64409112 EUR

    $ curco usd eur cad         # Ignores CAD
    USD / EUR = 0.764409112

Use `--vein` to update the cache

    $ curco usd --vein eur
    USD / EUR = 0.764409112

    $ curco 10USD EUR --vein
    10 USD = 7.64409112 EUR

    $ curco --vein USd € 10
    10 USD = 7.64409112 EUR

License
-------

This software is in the public domain.  Read `UNLICENSE` and/or visit the
[Unlicense website](http://unlicense.org).

Contacts
--------

Feel free to contact me, you should be able to find an email address of mine
from where you obtained this file.
