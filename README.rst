Me
==

Oh hi there and welcome to my personal github!

You'll find here a collection of random projects that either javascript or
Python with varying levels of quality and age.

I'll give you a guide to what can be found here:

Photons
-------

I have a tendency to find problems from my job and then making them something
fun to do outside work. This is very much one of those, and I'm super proud of
what I've made here.

Everything now lives in https://github.com/delfick/photons

But it was moved from https://github.com/delfick/photons-core and
https://github.com/delfick/photons-interactor

It's the public version of a framework I started in early 2016 that heavily
uses asyncio to talk to LIFX smart lights.

Docs can be found at https://photons.delfick.com

A docker client
---------------

I'm equally proud of this next project but in a very different way. I like the
code quality of Photons these days, but the code quality in
https://github.com/delfick/harpoon is not great.

I'm proud of it though because what I did there paved the way for what has since
become https://github.com/delfick/delfick_project and is essentially the
foundation of everything that I've written since then.

Also, Harpoon is cool. I haven't met many who agree with that assessment, but
it solved a bunch of problems I had with Docker back in 2014 and I still use
it in some places to make it easy to create multiple docker containers.

A truly imaginatively named project
-----------------------------------

https://github.com/delfick/delfick_project is a small monorepo of quite a few
different projects I created.

* Encapsulating patterns I used everywhere to bootstrap an application
* Helpers to make logging so much more enjoyable
* An error class that has a bunch of features
* A class that helps take a tree of dependencies and return those in layers
* Tools for managing plugins via entry points
* An object that can be used to treat multiple dictionaries as if they are one
* The ability to validate and normalise data

Those last two have a lot of features I can't fit into a single sentence but
all of this can be read at https://delfick_project.readthedocs.io/

Data normalisation
------------------

Part of ``delfick_project`` is the ``input_algorithms`` code that lets us validate
and normalise data to create well structured objects.

In late 2020 I wrote this idea for how I wanted to improve the API it provides:
https://github.com/delfick/delfick_project/blob/ideas/rewrite-norm-api/IDEAS.rst

However I never found the time. Recently (middle of 2022) I decided to achieve this
a bit differently and I created a layer on top of
`cattrs <https://cattrs.readthedocs.io/en/latest/>`_ that means you can do cattrs
transformation whilst also passing down meta information along for the way.

This project is ``strcs``: https://strcs.readthedocs.io/en/latest/

This one is my first attempt at seeing what I can do with Python Type hints and it's
kinda cool :)

My oldest project I still use
-----------------------------

In 2010 I was looking for a way to write rspec like tests in Python. There is a
big blocker to be able to do this in python, and that is you can't create a
multi line lambda. This means that you can't just have an "it" function that
takes in a string and the function to call for that test.

Existing libraries solved this by saying you should write your tests functions
like normal "def it_should_definitely_do_the_thing_i_want_it_to_do(self):" and
then you decorate it with a nice string. I really hate writing sentences like
that.

Eventually I discovered that you can create a custom codec for python and as
long as that codec is registered before you import a file, if the file specifies
that codec, python will translate the file before executing it.

Effectively I made it so describe blocks become classes and it blocks become
functions. And then a bunch of code to handle nested levels of indentation.

https://noseofyeti.readthedocs.io/

The problem with that is tooling, specifically linting and formatting. In 2020
I managed to fix both those problems and now my editor can auto format and lint
those files when I save them. Best of all the worlds!

The most what is happening here
-------------------------------

I have no idea what is happening here https://github.com/delfick/app-play

I was clearly hypomanic when I wrote it!

Virtualenvs
-----------

I used to put everywhere a bash script that when run would figure out if a
virtualenv already exists. If one didn't then it would make one for you,
otherwise it would use what is there. The script would then look at the
dependencies you want in that virtualenv and if the versions of those didn't
match in the virtualenv it would install those to the desired version. Once we
have the virtualenv setup, it'll execute a particular program from the virtualenv.

I eventually decided to make that it's own thing:
https://venvstarter.readthedocs.io/en/latest/

I find this really useful because I don't have to think about dependency
management. I just say what I want and when I run the script it'll make sure
I have those. This is especially useful when you provide something to others
and what they want is the thing to work, they don't care about making sure
dependencies are correct.

The one downside here is there's no lockfile, but there doesn't really exist
programmatic APIs for that functionality in current efforts to improve Python
dependency management.

Everything else
---------------

Clearly I spend way too much of my time programming! But you'll find other
things here, like helpers for a
`web server <https://whirlwind.readthedocs.io/>`_, a thing for
`converting dictionaries to xml <https://github.com/delfick/python-dict2xml>`_,
A `cool tool <https://github.com/delfick/simple-aws-lambda-maker>`_
for making the lambda side of an Alex skill, A pure python
`gpg decryptor <https://github.com/delfick/gpglib2>`_, An alternative
`asyncio plugin <https://github.com/delfick/alt-pytest-asyncio>`_ for pytest,
a python library for
`finding the commit times <https://github.com/delfick/gitmit>`_ of github files,
pure `hilarity <https://github.com/delfick/sshephalopod>`_, and a plugin for
gedit that `makes it modal <https://github.com/delfick/vigedit>`_.

Also my `website <https://delfick.com>`_ and the blog it contains are all written
in svelte (`code <https://github.com/delfick/random-ramblings-of-a-ranga>`_), which is awesome!

I'm more than my programming, but this is my github so I'll only use this to
walk you through my projects!
