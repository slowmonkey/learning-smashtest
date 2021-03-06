This project goes through the steps to set up [smash test](https://smashtest.io).

[git-repo](https://github.com/smashtestio/smashtest)

# Setup

1. Create new project folder.
2. Run `git init` to set up the git repo.
3. Run `npm init` to set  up the npm project.
4. Run `npm install smashtest --save-dev` to add smashtest to the project.
5. Create `demo.smash` file as the demo smash test file.
6. Update the npm test script in package.json to `bash -c 'PATH=$PATH:webDrivers/ smashtest'` 


# Setting up the Selenium WebDrivers

## Chrome

In the smash test file add the `Open Chrome` line. If the Chrome web driver is not available it will produce an error with a link to the chrome web driver downloads page. From here open your Chrome browser and check for the version before downloading the required Chrome web driver. Add it to the webDrivers folder in the repository.

## Firefox

Copy the same steps as for Chrome but use `Open Firefox`

# Useful findings.

1. Run `smastest -s` skips running branches that passed in the previous run.
2. In a CI/CD pipeline it's advisable to run `smashtest --no-debug` to ensure the test run ignores any `~`, `~~`, `$` characters left over from the test development.
