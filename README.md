mojito-cli-test
==========

This package provides the `test` command for the [`mojito-cli`](https://github.com/yahoo/mojito-cli) tool. Install them together with: `npm install -g mojito-cli`

Usage
-----

The `test` command uses [yuitest](https://github.com/yui/yuitest) to run tests in files ending in "-tests.js".

The command should be invoked at the top directory level of your mojito application, and have mojito installed locally in node_modules.

    % cd path/to/mojito/app
    % mojito test app

To run just a mojit's tests,

    % mojito test mojit mojits/MojitName

or

    % mojito test mojit MojitName

By default, the test results are displayed on stdout, and saved in a JUnitXML-formatted file at `artifacts/test/result.xml`. To specify a different destination, see below.

### Options

Instrument the code and generate a code coverage report, using [yuitest-coverage](https://npmjs.org/package/yuitest-coverage):

    --coverage
    -c

Specify a destination directory for the test results. Default is `artifacts/test`:

    --directory <path>
    -d <path>

Specify a temporary directory that will be used to copy instrumented code for code coverage. By default, the system's default directory for temp files is used, as determined by [`os.tmpdir()`](http://nodejs.org/api/os.html#os_os_tmpdir).

    --tempdir <path>
    -t <path>

Enable diagnostic output to the console with any of the following flags:

    --debug
    --verbose
    -v

Discussion/Forums
-----------------

http://developer.yahoo.com/forum/Yahoo-Mojito

Licensing and Contributions
---------------------------

BSD licensed, see LICENSE.txt. To contribute to the Mojito project, please see [Contributing](https://github.com/yahoo/mojito/wiki/Contributing-Code-to-Mojito).

The Mojito project is a [meritocratic, consensus-based community project](https://github.com/yahoo/mojito/wiki/Governance-Model) which allows anyone to contribute and gain additional responsibilities.
