Ways to hook into Flask

* jinja functions, filters, etc
* install functions in g
* monkeypatching 
* listen to signals
	- for timing, you can listen for before/after events and log them

Gotchas

* How do you interface with SQLAlchemy?
* How to integrate with other libraries w/o crashing
* Working with application factories: http://flask.pocoo.org/docs/extensiondev/


Examples of plugins:

* Flask-FeatureFlags
	* Simple, easy to understand (100 LOC)
	* https://github.com/trustrachel/Flask-FeatureFlags

* Flask-DebugToolbar
	* Port of Django's DebugToolbar
	* complex functionality, timing, additional blueprints

* Flask-SQLAlchemy 
	* Makes integration with SQLAlchemy easy
	* good use of signals to do work
	* https://github.com/mitsuhiko/flask-sqlalchemy/blob/master/flask_sqlalchemy/__init__.py


TAGLINE:

"The idea of Flask is to build a good foundation for all applications. Everything else is up to you or extensions."