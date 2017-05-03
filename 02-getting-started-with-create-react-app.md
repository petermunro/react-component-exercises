# Getting Started with create-react-app

To get started with React, we will use `create-react-app`.

> Conventions: I use the `$` to indicate a shell prompt and commands you type at the shell

1. Install it like this:

        $ npm install -g create-react-app

2. Create a project `hello`, and start the development server:

        $ create-react-app hello
        $ cd hello
        $ yarn start

3. This should open a browser on your project.


## Appendix: Environment Setup

You can perform all exercises up to and including module 7 in Chrome.
Module 8 needs `create-react-app`.

### Getting started with create-react-app

#### 1. Install node

**Mac**: I use nvm as we don't need to be root, and we can manage multiple node versions.

	1. Install nvm from https://github.com/creationix/nvm
	2. Run `nvm install 7.9`
			// To list available versions: `nvm ls-remote`

**WIN**: Install node from https://nodejs.org/

#### 2. Install create-react-app

	npm install create-react-app -g

#### 3. [Optional extra] Install Yarn

	yarn offers alternate package installation - it's pretty
	much equivalent to npm. To install, download from
	https://yarnpkg.com/

#### 4. Run create-react-app

	create-react-app myapp

