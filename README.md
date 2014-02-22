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

* in `behat.yml`, set the `base_url` value to URL of the site that you want to test.
* write some feature specs. You may use `features/_template.feature` as a guiding example.
* back up your features by implementing step methods in `features/bootstrap/FeatureContext.php`.

## Learn more

* [Quick Intro into Behat](http://docs.behat.org/quick_intro.html)
* [Behat Docs](http://docs.behat.org/)
* [Drupal Extension for Behat](http://dspeak.com/drupalextension/)
