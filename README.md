# `compass compile` for Grunt.js

This is a custom grunt.js multitask that executes `compass compile` for you and prints the COMPASS output to `grunt.log.write()`.

1. Install this grunt plugin next to your project's grunt.js gruntfile with: `npm install grunt-compass`.
2. Call `grunt.loadNpmTasks('grunt-compass')` in your gruntfile.
3. Configure `grunt watch` to watch your scss files and call the task.
	e.g.:

	```javascript
	watch: {
	    files: ['assets/scss/partials/*.scss'],
	    tasks: ['compass:somename']
	}
	```

4. Setup the config for compass in your grunt config, or setup a compass config file:
	* Option 1: Set the configuration for compass in your grunt.js file:

		```javascript
		compass: {
            somename: {
                src: 'assets/scss/partials',
                dest: 'assets/css/partials'
            }
		}
		```

		"src" is the folder with sass/scss files.
		"dest" is the file where the css files will be place.
	* Option 2: Setup a compass project
		```
		compass install compass
		```
5. You can set your custom output style like this:

    ```javascript
    compass: {
        somename: {
            outputstyle: 'compressed'
        }
    }
    ```
6. You can disable line comments like this:

    ```javascript
    compass: {
        somename: {
            linecomments: false
        }
    }
    ```
7. Run "grunt watch" and change some SASS files :)

----

# LICENSE MIT

Copyright (c) 2012 Kahlil Lechelt

Permission is hereby granted, free of charge, to any person
obtaining a copy of this software and associated documentation
files (the "Software"), to deal in the Software without
restriction, including without limitation the rights to use,
copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the
Software is furnished to do so, subject to the following
conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES
OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND
NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT
HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY,
WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING
FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR
OTHER DEALINGS IN THE SOFTWARE.