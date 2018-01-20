# Django boilerplate with GOV.UK Elements-sass, GOV.UK Frontend Toolkit and GOV.UK Frontend*

Demo project to show integration

## Prerequisites:
1) [Nodejs](https://nodejs.org/en/)
2) [Homebrew](https://brew.sh/)
3) Python3 with `brew install python3`

## Setup Django
Advance django/python users can skip this

1) move into the repo directory
2) run `python3 -m venv venv`
3) run `source venv/bin/activate`
4) run `pip install Django`
5) run `pip install libsass django-compressor django-sass-processor`

alternatively, create a directory and install wthid boilerplate with
a) run `django-admin.py startproject --template https://github.com/igloosi/govuk-frontend-django-boilerplate/archive/master.zip govuk_frontend_django_boilerplate .`
b) run `pip install libsass django-compressor django-sass-processor`

## Install NPM modules
1) move into the sample_app directory
2) run `npm install`
This will install dependencies defined in `sample_app/package.json`

## Run app

1) move one level from `sample_app folder`
2) run `python manage.py runserver`


To use GOV.UK Frontend, login to npm  with test user (in private beta) - to make it work without frontend, comment out:
`"@govuk-frontend/all": "0.0.22-alpha"` in `sample_app/package.json` and
`@import "@govuk-frontend/all/all";` in `sample_app/assets/sass/`
and rerun `npm install` and `python manage.py runserver`

To compile Sass partials from `node_packages` we've used
[https://github.com/jrief/django-sass-processor](https://github.com/jrief/django-sass-processor)

Entry point for Sass partials is `assets/sass` and destination is `static/css`

*(access required)
