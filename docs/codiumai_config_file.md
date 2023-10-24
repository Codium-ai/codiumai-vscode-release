The CodiumAI extension can be configured via a `.toml` configuration file.

Please create a file named `.codiumai.toml` or `.codiumai.local.toml` in your source directory.

The file can be next to the code under test or inside any parent directory.

#### Precedence rules:
* A `.local` file will take precedence (intended to be `.gitignore`ed).
* If multiple config files are found in nested directories - the configuration items are accumulated, where the most specific one (the one closest to the file under test) takes precedence.

### The following sections and keys are available:

`[tests]`

* `framework`: the test framework used to test your code. Possible values are `Jest`, `Mocha`, `Vitest`, `Karma`, `Jasmine`, `QUnit` or `React Testing Library` in Javascript projects, or `Pytest` or `Unittest` in Python projects.

* `utility_library`: An additional Javascript utility library used to test your code, if any. Possible values are `None`, `Testing Library`, `Enzyme`, or `Chai`. Not applicable to Python projects.

* `reference_test`: A multiline string serving as an example test that represents what you would like the generated tests to look like in terms of style, setup, etc.

* `use_mocks`: If applicable, use mocks in the generated code

`[tests.javascript]`
In a Javascript / Typescript project, use the following configuration values to control the test runner:

* `overrideTestRunScript`: the command used to run your tests, i.e. `npx jest --runInBand`
* `overrideTestRunCwd`: a path relative to the location of the config file to be used as the test process' working directory. Defaults to the config file's location if omitted. 
* `overrideImports`: a multiline string containing import declaration to use in each test file.

### Example config file for a mocha/chai javascript environment:
```
[tests]
framework = "Mocha"
reference_test = """
describe("foo", () => {
  it("says 'bar'", () => {
    expect(foo.say()).to.equal("bar");
  });
});"""

[tests.javascript]
overrideTestRunCwd = "./test"
overrideTestRunScript = "npx mocha"
overrideImports = """ 
import {expect} from 'chai'; """
```