PyCon Talk 
==========

TITLE
------
Developing Flask Extensions [need less boring title]

CATEGORY
---------

Best Practices/Patterns

DURATION
--------

30 minutes

DESCRIPTION
-----------

"The idea of Flask is to build a good foundation for all applications. Everything else is up to you or extensions." - Armin Ronacher, creator of Flask. 

You can create a web application with Flask in seven lines of code, and you can grow that app to thousands. How do you create reusable, shareable libraries? What can this microframework do?

We'll use a simple but real extension I created (Flask-FeatureFlags) to look at the different ways you can make Flask awesome.

AUDIENCE
--------
Users of Flask or web application developers curious about its capabilities. 

PYTHON LEVEL
------------

Intermediate

OBJECTIVES
----------

Users of Flask will learn how to extend it and make shareable, reuseable libraries. Application developers not familiar with Flask will get an idea of its capabilities and totally want to use it. 

DETAILED ABSTRACT
-----------------


OUTLINE
-------

1. Introduction (5 min)
	* About me
 	* The promise of Flask - lightweight, free to be you.  Here's a toolkit, now go build
 	* The bane of Flask - no batteries included. Here's a toolkit, now go build

2. Flask architecture in 5 min (5min)
	* Flask is a WSGI framework (Werkzeug) married to a template language (Jinja)
	* What the hell is a WSGI?
	* Signals - don't call us, we'll call you
	* Blueprints - the easy way to bundle code

3. Flask-FeatureFlags - a basic extension (10min) 
	* adds feature flagging to Flask in ~100 LOC
	* It's tiny, but covers a lot:
		- It uses signals to hook into request lifecycle
		- It stores functions in the global variable g
		- Exposes decorators to customize view behavior
		- Customizes Jinja
		- It even supports Python 3 (with a bit of extra code)

5. Pushing the Envelope (5min)
	* Hooking into SQLAlchemy (see Flask-FeatureFlags contrib library or Flask-DebugToolbar)
	* Rework Flask's entire view system: Flask-Classy
	* Add raptors (Flask-Raptor)
	* other libraries as I have time

6. Go forth and expand: http://flask.pocoo.org/docs/extensiondev/

7. Questions (5min)

ADDITIONAL NOTES
-----------------

Flask-FeatureFlags is open source and in (internal) production use here at LinkedIn: https://github.com/trustrachel/Flask-FeatureFlags

This would be my first time speaking at a conference like PyCon. I’ve spoken at my company a few times and at PyLadies events. I'll have the opportunity to speak at several user groups beforehand.


