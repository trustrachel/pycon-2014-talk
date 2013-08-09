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
Users of Flask or developers curious about its capabilities. 

PYTHON LEVEL
------------

Intermediate

OBJECTIVES
----------

Users of Flask will learn how to extend it and make shareable, reuseable libraries. People not familiar with Flask will get an idea of its architecture and capabilities.

DETAILED ABSTRACT
-----------------

Built entirely on Python 3, the SpacePug project is one of the first major projects to run on Python 3, and it’s the first to launch pugs into orbit.

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

1. Introduction (5 min)
	* About me
 	* The promise of Flask - lightweight, free to be you.  Here's a toolkit, now go build
 	* The bane of Flask - no batteries included. Here's a toolkit, now go build
 
2. Flask is meant for tinkering, aka Flask architecture in 5 min (5min)
	* What the heck is a WSGI, Werzeug and Jinja
	* Flask has blueprints
	* Flask has hooks (and subclassing)
	* Flask has signals
	* or even monkeypatching (eeeeeevil)

3. Flask-FeatureFlags - a basic extension (10min) 
	* adds feature flagging to Flask in ~100 LOC
	* topics covered:
		- Using signals to hook into request lifecycle
		- Storing functions in the global variable g
		- Decorators to customize view behavior
		- Customizing Jinja
		- Installing your extension
		- Python 3 support

5. The Crazy Stuff, aka pushin' the envelope (5min)
	* Flask-DebugToolbar
		- 
	* monkeypatching
	* SQLAlchemy hooks with Flask-SQLAlchemy

	* Good libraries to learn from:
		- Flask-SQLAlchemy
		- 

6. Questions (5min)

ADDITIONAL NOTES
-----------------

* Flask-FeatureFlags is open source: https://github.com/trustrachel/Flask-FeatureFlags

This would be my first time speaking at a conference like PyCon. I’ve spoken at my company a few times and at PyLadies events. I'll have the opportunity to speak at several user groups beforehand.


