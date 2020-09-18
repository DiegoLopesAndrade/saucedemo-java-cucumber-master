Selenium project with Java and Cucumber to validate the saucedemo.com application.
The following scenarios are being validated in this project:
## Scenarios

| Feature | Scenario | Smoke Test | Regression Test | End to End |
| --- | --- | --- | --- | --- |
| login | Verify valid users can sign in | Yes | Yes | No |
| login | Verify locked out user gets locked out message | No | Yes | No |
| login | Verify invalid users cannot sign in | No | Yes | No |
| orders | Place a single item in the shopping cart | Yes | Yes | No |
| orders | Place multiple items in the shopping cart | No | Yes | No |
| orders | Validate Order Totals | No | Yes | No |

## Organization of the project
- src/test/resources/features: 
Here are the cucumber files (.feature)

- src/test/java: 
- com.saucelabs.example.stepdefs: 
Here is the implementation of the step definitions.
- com.saucelabs.example.pages: 
Here is the abstraction of "locators" and methods for interacting with the components of each page.
- com.saucelabs.example.model: 
Definition of the properties of the inventory page.
- com.saucelabs.example: 
The entire organization of the test suite, enabling execution on different operating systems, different browsers, generation of reports and etc ...

## Full regressions

To run the full test suite, simply run:

    $ mvn test
    
And each scenario will execute.