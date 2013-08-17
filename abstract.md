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

You can create a web application with Flask in seven lines of code, and you can grow that app to thousands. How do you create reusable, shareable libraries? 

We'll use a simple but real extension I created (Flask-FeatureFlags) to look at the different ways you can make Flask awesome.

AUDIENCE
--------
Users of Flask or developers curious about its capabilities. 

PYTHON LEVEL
------------

Intermediate

OBJECTIVES
----------

Users of Flask will learn how to extend it and make shareable, reuseable libraries. People not familiar with Flask will get an idea of its architecture and capabilities. 

DETAILED ABSTRACT
-----------------

Flask is an 

Why Python 3?

Years ago, developers made an attempt to build a system on Python 2, but they found that it just wasn’t good enough to launch a dog into space, let alone a pug. One of the first problems they encountered was the GIL and the fact that the thrust controllers didn’t perform well enough to launch a dog of short, stocky stature. After switching to Python 3.2, which has an improved implementation of the GIL, the thrust controller performed so much better that analysis shows pugs could potentially join the Curiosity rover on the surface of Mars.

The astropugs are able to communicate back to mission control via a special keyboard to speak their language, represented in a previously unassigned Unicode plane. While developing the communications systems, the developers found that Python 3’s distinction between bytes and text makes their code more readable and easier to understand. They prepared benchmarks comparing a Python 2.7 implementation against a Python 3.3 implementation to show the 3.3 version is more memory efficient thanks to PEP 393.

A new library: multipugging

Early versions of the project only supported one pug per spacecraft. Feeding and cleaning up after multiple pugs was a significant issue, so much that early testing sent the engineers back to the drawing board to start from scratch. In comes multipugging, a system to control multiple feeders and cleaners, removing the common bottleneck of dealing with the needs of multiple pugs in orbit.

This talk will show a live demo of multipugging scaling out to feed 16 pugs at once.

A new test runner: treadmill

Everyone knows the first thing a project should do is write their own test runner, so we did just that with treadmill. It’s like putting a pug on a treadmill, but for code.

OUTLINE
-------

0. About me

1. The Really Quick Overview of Flask (5 min) 
		* A really sweet marriage of WSGI (Werzeug) and templating (Jinja)
	 	* The promise of Flask - lightweight, free to be you.  Here's a toolkit, now go build
 		* The bane of Flask - no batteries included. Here's a toolkit, now go build
 		* It's a toolkit for HTTP, designed with extensibility in mind 
 		* Show sample app

2. The Really Quick Overview of Flask Architecture (5 min)
		* Globals - g, request, and other ways to stash and grab data
		* Blueprints - bundles of application components, useful for bolting on separate code
		* Signals - we'll call you when we hear something
		* Hooks - Flask has tons of 'em
		* Subclassing - it's designed for it

3. A practical example - Flask-FeatureFlags (10min) 
	* adds feature flagging to Flask in ~100 LOC
	* It's tiny, but covers a lot:
		- It uses signals to hook into request lifecycle
		- Stashes functions in the global variable g
		- Provides decorators to customize view behavior
		- Customizes Jinja
		- It even supports Python 3!

4. Pushing the Envelope (5min)
	* Hooking into SQLAlchemy (see Flask-FeatureFlags contrib library or Flask-DebugToolbar)
	* Rework Flask's entire view system: Flask-Classy
	* Add raptors (Flask-Raptor) <-- need better example, this is silly
	* or even monkeypatching (eeeeeevil)

5. Go forth and expand: http://flask.pocoo.org/docs/extensiondev/

6. Questions (5min)

ADDITIONAL NOTES
-----------------

Flask-FeatureFlags is open source and in (internal) production use here at LinkedIn: https://github.com/trustrachel/Flask-FeatureFlags

This would be my first time speaking at a conference like PyCon. I’ve spoken at my company a few times and at PyLadies events. I'll have the opportunity to speak at several user groups beforehand.
