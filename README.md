# lodown
An npm functional programming library project

1. Fork this repository to your own GitHub account.

2. Clone your forked version of the lodown repository to a new Cloud9 workspace or locally if you prefer.

3. To create a `package.json` configuration file for our lodown library, from the command-line, run the command:
    
        npm init

4. **IMPORTANT CONFIGURATION**: Fill in the prompts with your own details:
    
    1. When asked for a project name, give the it a name following this pattern:

        `lodown-yourGitHubUsername`

    2. When asked for **test command**, enter:
        
        `istanbul cover _mocha -- test/ -R spec`

    3. When asked for your **git repository**, you will probably be given the correct url as the default, so just select this by pressing `return`, otherwise, provide **your forked GitHub repository's url**.

5. Install the required test libraries by running the following command:
    
        npm install i -D mocha chai sinon istanbul

6. Implement your library in the file `index.js`. Remember that `index.js` is a Node.js module, so you must export your API using, for example:
    
        module.exports.each = each;

7. Using the `each` function provided as an example, rewrite the comments from your underpants library
so that they act as live code hints as you work in your module.

8. Release your lodown library to `npm` (node package manager), by following the steps on this page to do so:
    
    [**Publishing NPM Packages**](https://docs.npmjs.com/getting-started/publishing-npm-packages)

**BONUS:** Create unit tests for your library:

1. Write your tests in the file `test/index.spec.js`. Check out the [chai api for ](http://chaijs.com/api/bdd/) and [be careful when asserting/expecting against complex types](http://stackoverflow.com/questions/17526805/chai-test-array-equality-doesnt-work-as-expected) - you'll have to make use of the `.eql` api, and not `.equal`. For example:
    
        expect(lodown.filter([1, 2, 3], function(value) { return value > 2; } )).to.eql([3]);

2. To run your tests, run the following command:
    
        npm test

3. Check the console output for passes and failures.

4. Preview (Cloud9) or open the file at `coverage/lcov-report/index.html` for your coverage report. Make certain all lines of code are traversed in your tests!

## Resources:

### Docs

1. https://mochajs.org
2. http://chaijs.com/api/bdd/
3. http://sinonjs.org/docs/#spies-api

### Reading
1. http://marcofranssen.nl/using-mocha-chai-sinon-to-test-node-js/
2. http://stackoverflow.com/questions/19298118/what-is-the-role-of-describe-in-mocha
3. http://www.vapidspace.com/coding/2014/10/29/code-coverage-metrics-with-mocha-and-istanbul/

### Quick Videos
1. https://egghead.io/lessons/javascript-how-to-write-a-javascript-library-setting-up-unit-testing-with-mocha-and-chai
2. https://egghead.io/lessons/javascript-how-to-write-a-javascript-library-unit-testing-with-mocha-and-chai