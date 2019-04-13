# KID util
Simple utils to generate and verify KID numbers with either MOD10 or MOD11.

Generating KID from integer string:

    $ python kid.py -g 2345678
    23456783
    $ python kid.py -m mod11 -g 2345678
    23456788

Verifying KID from string:

    $ python kid.py -v 23456783
    True
    $ python kid.py -v 23456788
    False
    $ python kid.py -m mod11 -v 23456788
    True
    $ python kid.py -m mod11 -v 23456783
    False

# Testing

To run the tests:

    python -m unittest discover