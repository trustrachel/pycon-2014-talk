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

You can create a web application with Flask in seven lines of code. What happens when your app grows to thousands? How do you create reusable, shareable libraries?

We'll use a real but very simple extension I created (Flask-FeatureFlags) to look at the different ways you can hook into Flask applications. 


AUDIENCE
--------
Users of Flask or web application developers curious about its capabilities. 

PYTHON LEVEL
------------

Intermediate

OBJECTIVES
----------

Users of Flask will learn how to extend it and make shareable, reuseable libraries. Application developers not familiar with Flask get an idea of its capabilities for future projects.

DETAILED ABSTRACT
-----------------

tbd

OUTLINE
-------

1. Introduction (5 min)
	* About me
 	* The promise of Flask - lightweight, free to be you.  Here's a toolkit, now go build
 	* The bane of Flask - no batteries included. Here's a toolkit, now go build

2. ?? Flask architecture in 5 min (5min)
	* ?? explain what is WSGI/Werzeug
	* ?? explain signals
	* ?? explain blueprints

3. Flask-FeatureFlags - a basic extension (10min) 
	* adds feature flagging to Flask in ~100 LOC
	* topics covered:
		- Using signals to hook into request lifecycle
		- Storing functions in the global variable g
		- Decorators to customize view behavior
		- Customizing Jinja
		- Installing your extension
		- Python 3 support

5. The Crazy Stuff (5min)
	* ?? how much can you push the envelope?

	* Good libraries to learn from:
		- Flask-SQLAlchemy
		- Flask-DebugToolbar

6. Questions (5min)

ADDITIONAL NOTES
-----------------

* Flask-FeatureFlags is open source: https://github.com/trustrachel/Flask-FeatureFlags

This would be my first time speaking at a conference like PyCon. I’ve spoken at my company a few times and at PyLadies events. I'll have the opportunity to speak at several user groups beforehand.


