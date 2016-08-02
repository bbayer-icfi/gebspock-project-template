# Geb Spock Project Template


## Overview

This is a single module maven project which will execute the Geb Spock Project Template
Automated Tests


## To Run the Automated Tests:
To run the automated tests, execute the following:

mvn clean test *command-line-arguments*


### Command Line Arguments
#### Specify Browser
-Dgeb.env=...

**Example:**
`-Dgeb.env=chrome`

#### Specify Target Environment
-Dspock.run.target=...

**Example:**
`-Dspock.run.target=qa`

#### Specify Tests To Include (Only Run)
-Dspock.run.includes=...

**Example:**
`-Dspock.run.includes=allexcludedfromhtmlunit,ondemand`

#### Specify Tests To Exclude
-Dspock.run.excludes=...

**Example:**
`-Dspock.run.excludes=javascript`

#### Specify Override Of Default And Context Exclusion
`Dspock.run.excludes.context=ignore`


### Minimal Requirements
* By default, tests will use the headless HtmlUnit browser (whose driver
  is bundled into Selenium Webdriver)
* Firefox installed (if running the tests using the firefox environment switch)

To run with specific browser drivers, look in the GebConfig.groovy file for any
configured environments and pass the value to your maven command using the
 'geb.env' command line argument.

**Example:**
`mvn clean test -Dgeb.env=firefox`


## Requirements
* Maven 3.x
* JDK 1.8
