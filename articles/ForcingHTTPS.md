
<!--
.. title: Forcing HTTPS
.. slug: ForcingHTTPS
.. date: 2015-05-13 14:35:28 UTC+01:00
.. tags:
.. category:
.. link:
.. description:
.. type: text
-->




For some web sites you might want to not just offer HTTPS access to your users -- you might want to force all connections to go through HTTPS. There are different ways to do that for different web frameworks. Here are some -- if you don't see the framework you use, let us know with the "Send Feedback" link above.


##Django


Just

    pip install --user django-sslify


Or install it into your virtualenv if you're using one.

Then add the middleware as the first middleware class you have in settings.py. Also note that it won't force SSL if you have `DEBUG = True` in your settings (which in turn means you'll need to make sure that `ALLOWED_HOSTS` is set up properly).


##web2py


Uncomment this line in db.py:

    request.requires_https()



##Flask


Use [this Flask extension](https://github.com/kennethreitz/flask-sslify).


##Bottle


Use [this Bottle extension](https://pypi.python.org/pypi/Bottle-SSLify/0.0.1).