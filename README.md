HappyEdit is a Vim-inspired text editor with modern features. It is based on modern web technologies and feels like a native app.

**NOTE:** HappyEdit is currently in the prototype stage and is not ready for actual use yet.

Try it out
----------

**Building Ace:**

This step requires Node.js and npm to be installed.

```
$ cd HAPPYEDIT_CHECKOUT
$ git submodule init
$ git submodule update
$ cd ace
$ npm install
$ node Makefile.dryice.js
$ cd ..
$ python make.py
```

**Installing HappyEdit as a Chrome App:**

1. Open Google Chrome
2. Go to Tools -> Extensions, enable the developer mode, then press "Load unpacked extension" select the HAPPYEDIT_CHECKOUT/build/chrome folder.
3. Open a new tab and click the HappyEdit icon.

**Running HappyEdit within the browser:**

1. In your browser, open HAPPYEDIT_CHECKOUT/build/browser/index.html.

Integrating HappyEdit
---------------------

It's possible to write your own server implementation to, for example, let
users edit files on a remote server.

Basically, your server must implement a simple REST interface:

 * POST    /connect
 * GET     /files
 * GET     /files/:path
 * POST    /files/:path

See server.py for reference.

JavaScript Code standards:
--------------------------

 * Variables referring to DOM elements should have a leading '$', e.g. '$ul'.
 * 'Classes' should be written LikeThis.
 * Class members should be written likeThis.
 * Indentation with 4 spaces.
 * Modifying object prototypes and 'inheritance' should be avoided.
 * Each 'class' should be in its separeate .js file named 'YourClass.js'.
