# Intro to Django

## Getting started with Django

### Install Django
Before you can use Django, you’ll need to install it. Our complete installation guide covers all the possibilities; this guide will get you to a simple, minimal installation that’ll work while you walk through the introduction.

### How Django Works Behind the Scenes


Django is a Python-based web framework used by millions of developers and billions of consumers through popular apps like Instagram. It is open source, meaning the code is available for free on Github and can be downloaded onto any developer’s computer and used alongside the official documentation. However, I find that even professional Django developers have little insight into “how” Django is actually run, both technically and legally/financially, so this post is my attempt to provide a concise overview of it all.

Django was originally developed at the Lawrence Journal-World newspaper by Adrian Holovaty, Simon Willison, and Jacob Kaplan-Moss. The code was open-sourced in 2005 and developers immediately started making contributions to the codebase. Fourteen years later, Django remains under active development, with new major releases every nine months, minor security releases almost monthly, an official issue tracker, and robust discussion on the django-developers Google group.

As with all open source projects, the two major issues that crop up are funding and control. Let’s start with funding: why does an open-source project need funding?

It turns out that while writing code is fun and developers are generally willing to contribute their time for free to do so, there are a host of decidedly less fun tasks needed to maintain and sustain an open source project. This includes handling any legal/trademark issues, triaging tickets, guiding community discussions, organizing conferences, managing releases, and so on. As a result, almost all popular open source packages have some degree of funding involved, typically in one of three forms:

1) Corporate Sponsor - A group of engineers within a larger, for-profit company decide to open-source internal code. This is how React (Facebook) and Angular (Google) emerged. Typically engineers at the company are paid, in part, to work on open source though community involvement from developers outside of the core company occurs as well. While this structure has the stability of a wealthy benefactor, there can be confusion around the licensing aspects at times.

2) Solo - An individual developer initially creates code, open sources it, and retains default control. This is the case for VueJS, Tailwind CSS, and Laravel, among others. Typically the lead developer either raises contributions directly like Evan You of VueJS, offer add-on services like Spark for Laravel, or the founders provide highly-paid consulting services.

3) Non-profit - This was Django’s approach early on, in 2008, when the Django Software Foundation was formed to promote, support, and advance Django.