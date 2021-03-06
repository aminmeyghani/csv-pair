# csv-pair

> Combines two CSV files merging identical columns

[![NPM][csv-pair-icon] ][csv-pair-url]
[![Build status][csv-pair-ci-image] ][csv-pair-ci-url]
[![semantic-release][semantic-image] ][semantic-url]

[csv-pair-icon]: https://nodei.co/npm/csv-pair.svg?downloads=true
[csv-pair-url]: https://npmjs.org/package/csv-pair
[csv-pair-ci-image]: https://travis-ci.org/bahmutov/csv-pair.svg?branch=master
[csv-pair-ci-url]: https://travis-ci.org/bahmutov/csv-pair
[semantic-image]: https://img.shields.io/badge/%20%20%F0%9F%93%A6%F0%9F%9A%80-semantic--release-e10079.svg
[semantic-url]: https://github.com/semantic-release/semantic-release

Example: combine two CSV files. Some columns are identical, some are different

a.csv

    name,age,occupation
    John,20,student
    Mary,21,student

b.csv

    name,age,occupation
    John,20,teacher
    Mary,21,doctor

Let us combine these two CSV files. Identical columns will be collapsed. Different values
will have duplicate column

    csv-pair a.csv b.csv combined.csv

combined.csv

    name,age,occupation - a.csv,occupation - b.csv
    John,20,student,teacher
    Mary,21,student,doctor

## Install

Need [NodeJS](https://nodejs.org/), you can check if Node is installed locally
by opening a terminal window and trying command

    node --version

Then install this application

    sudo npm install -g csv-pair

Check if the tool has been installed by running from the terminal. It should show the input
parameters

    $ csv-pair
    Usage: <filename1.csv> <filename2.csv> <output.csv>

### Small print

Author: Gleb Bahmutov &copy; 2015

* [@bahmutov](https://twitter.com/bahmutov)
* [glebbahmutov.com](http://glebbahmutov.com)
* [blog](http://glebbahmutov.com/blog/)

License: MIT - do anything with the code, but don't blame me if it does not work.

Spread the word: tweet, star on github, etc.

Support: if you find any problems with this module, email / tweet /
[open issue](https://github.com/bahmutov/csv-pair/issues) on Github

## MIT License

Copyright (c) 2015 Gleb Bahmutov

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
