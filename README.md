# PhoneGap Simple VueJS and modular CSS Template

Phonegap template to create apps with VueJS 2 and Modular CSS.

## Usage

To create a phonegap project, do the following:

***Phonegap CLI:***

	$ phonegap create myapp --template https://github.com/OmarGM2294/phonegap-vuejs-modularcss.git
	$ cd myapp
	$ sudo npm install
	$ sudo npm run dev

**NOTE:** Change "myapp" for your application's name

***Cordova CLI:***

	$ cordova create my app --template https://github.com/OmarGM2294/phonegap-vuejs-modularcss.git
	$ cd myapp
	$ sudo npm install
	$ sudo npm run dev

**NOTE:** Change "myapp" for your application's name

Once you do this, the server will be runngin in http://localhost:3000.

## Components in Vue

There are 4 components pre-installed in the template:

1. Vue Router. See the documentation [here](http://router.vuejs.org/en/).
2. Vue Resource. See the documentation [here](https://github.com/pagekit/vue-resource).
3. Vuex. See the documentation [here](https://vuex.vuejs.org/en/).
4. Vue i18n. See the documentation [here](http://kazupon.github.io/vue-i18n/).

## Project structure

The projects manage all content in two important folders, assets and components, and inside each one another structure recommended.

An important thing to know, an organized project reflects an organized mind, so do the best to keep this structure if you want.

## Troubleshooting

* If the auto reload is not showing changes at all, please stop the server and run it again.

* If any of the commands shows an error, run it with sudo.

* If you get the error	"/usr/bin/env: node: No such file or directory", try running this:

	$ sudo ln -s /usr/bin/nodejs /usr/bin/node

## Credits

This is a template base in:

[LeMaur - Phonegap Vueify](https://github.com/leMaur/phonegap-vueify)
