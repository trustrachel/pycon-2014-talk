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

Users of Flask will learn how to extend it and make shareable, reuseable libraries. People not familiar with Flask will be introduced to its architecture and capabilities. 

DETAILED ABSTRACT
-----------------

"The idea of Flask is to build a good foundation for all applications. Everything else is up to you or extensions." - Armin Ronacher, creator of Flask. 

No batteries included

Flask purposely ships with almost nothing - it's a no-batteries-included toolkit at heart. Most functionality lies in the extension ecosystem, and if you want to share your own code, you'll need to learn how to create one. We'll talk about the architecture of Flask, and go over how you can extend it to add your own functionality. 

A working example - Flask-FeatureFlags 

When my team moved to continous integration, we needed a way to deploy but hide incomplete features. I wrote a small library to add feature flagging to our application. Other teams were interested so I rewrote it as a general purpose extension and open sourced it.  It's only a hundred lines of code, but it's a great indroduction to how you can extend Flask including signal hooks, decorators, and new Jinja functionality. It even works with Python 3.

Where do you go from here?

We'll end with a sampler of Flask extensions that push the envelope to give you a flavor of where you can go after the basics.

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
