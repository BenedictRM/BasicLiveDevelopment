---
layout: layout.hbs
---

# Basic Live Development Environment

This is a basic package to develop javascript pages using metalsmith to 
track and reload pages live as you develop.  Follow these steps to set up your 
environment.

# Requirements
* Firebase -- setup a firebase account and link it to the build in firebase.json under "firebase": "your firebase account"
** This allows you start up a firebase server to your project for local hosting -- alternatively you can setup a different server

* node -- install node locally -- his project contains the build.js file required to set up the environment

# Install

    $ npm install

# Test / Development
##### ** Key ** -- to do the live development you must run each of the following commands in separate terminals in the following order: 

### Build:
#### Start tracking changes with metalsmith:
	$ node build.js 

### Serve:
#### In a second shell start a firebase server (you can alternatively use any local server e.g. python serve): 
	$ firebase serve	

The server is default to `http://localhost:5000` -- use your browser to navigate to this port

# Deploy -- firebase will host your page 

	$ firebase deploy

# Files to Edit:
* Do not edit files in the build folder -- these get auto-generated 
* Edit files in src and templates -- with materialize you can create .hbs files in templates and materialize will convert to html

## src
* src -> apps : put built out apps here with the file structure for the apps
* To edit the initial landing page edit src -> index.md -- metalsmith-markdown will convert to browser readable for you

### *Initial file system is just a recommendation as to how to separate concerns