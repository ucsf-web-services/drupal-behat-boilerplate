## About

Boilerplate for Drupal/Behat tests. You may use this as a starting point for rolling your own Behat tests.


## Prerequisites

It is assumed that the following software is already installed:

* A recent version of Oracle Java (JRE OR JDK), with the `java` executable in yout PATH.
* PHP 5.3.5+, with the `curl`, `mb_string` and `xml` extensions enabled and the `php` executable in your PATH.
* Git
* The Firefox web-browser.

## Installation

1. Install [Composer](https://getcomposer.org/doc/00-intro.md).
2. Checkout the repo, install Behat via Composer.
```bash
git clone https://github.com/ucsf-drupal/drupal-behat-boilerplate.git
cd drupal-behat-boilerplate
composer install
```

## Getting Started

* In `behat.yml`, set the `base_url` value to URL of the site that you want to test.
* Define your [features](http://docs.behat.org/quick_intro.html#define-your-feature) and [scenarios](http://docs.behat.org/quick_intro.html#define-a-scenario). You may use `features/_template.feature` as a guiding example.
* Back up your features by [implementing step definitions](http://docs.behat.org/quick_intro.html#writing-your-step-definitions) in `features/bootstrap/FeatureContext.php`.


## Running tests through the HTTP client

Run Behat with the default profile from the project's root directory.

```
cd <project>
bin/behat
```

### Running tests in the web-browser

1. In a command line terminal, run Selenium.

    ```
    cd <project>
    java -jar bin/selenium-server.jar
    ```

2. Then open another terminal window and run Behat with the "browser" profile.

    ```
    cd <project>
    bin/behat -p browser
    ```

## Troubleshooting

- Why am I getting "PHP Fatal error:  Class 'DOMDocument' not found..."?

   Make sure your `php-xml` PHP extension is installed or up-to-date.

    ```
    sudo yum install php-xml
    ```


- Why am I getting "PHP Fatal error:  Call to undefined function Behat\Behat\DependencyInjection\mb_internal_encoding()..."?

   Make sure you have installed the `php-mbstring` PHP extension.

    ```
    sudo yum install php-mbstring
    ```

- Why I am not getting colored output from behat tests?

   Behat is probably not picking up the type of terminal you're using.  Forcing it to run in ANSI mode will probably fix it.

    ```
    bin/behat --ansi
    ```
## Learn More

* [Quick Intro into Behat](http://docs.behat.org/quick_intro.html)
* [Drupal Extension for Behat](http://dspeak.com/drupalextension/)
