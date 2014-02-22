# About

Boilerplate for Drupal/Behat tests. You may use this as a starting point for rolling your own Behat tests.

## Installation

1. [Get Composer](https://getcomposer.org/doc/00-intro.md).
2. Checkout the repo, install Behat via Composer.
```bash
git clone https://github.com/ucsf-drupal/drupal-behat-boilerplate.git
cd drupal-behat-boilerplate
composer install
```

## Usage

* In `behat.yml`, set the `base_url` value to URL of the site that you want to test.
* Define your [features](http://docs.behat.org/quick_intro.html#define-your-feature) and [scenarios](http://docs.behat.org/quick_intro.html#define-a-scenario). You may use `features/_template.feature` as a guiding example.
* Back up your features by (implementing step definitions)[http://docs.behat.org/quick_intro.html#writing-your-step-definitions] in `features/bootstrap/FeatureContext.php`.
* Run behat from inside your project root directory.
```bash
bin/behat
```

## Learn more

* [Quick Intro into Behat](http://docs.behat.org/quick_intro.html)
* [Drupal Extension for Behat](http://dspeak.com/drupalextension/)
