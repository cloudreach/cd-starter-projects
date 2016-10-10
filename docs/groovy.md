# Groovy

## Links
* http://groovy-lang.org/documentation.html#gettingstarted

## QuickStart and Tips
* Supports duck typing and strongly typed variables
* String `def disString='asdf'` or `def disString="asdf"`
* List `def disList=[1,2,3]`
* Map ```def disMap=[a:'1',b:'2']```
* Default getters and setters are automatically generated for groovy classes
* Groovy fully supports all java syntax and calls
* Groovy can be run as a script or called like a normal java library
* Use curly braces to enclose all variables within a string ex. ```def foo="Running ${job}"```
* Single quotes does not interpolate variables i.e.

    ```
    def bar='ABC'
    println 'foo ${bar}'
    ```

    resolves to ```foo bar```
