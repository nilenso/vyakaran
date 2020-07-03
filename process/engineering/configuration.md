# Configuration

## The Basics

* files per env
  * development.json
  * production.json
  * staging.json
  * test.json
* Rails envs are _samples_
* file-based or token-based
  * token-based: heroku
  * token-based: cascading \(priority\) config trees

## Push vs. Pull

* pull
  * environment variables
* push
  * conf:check  \(read & verify\)
  * conf:update \(write & push\)

## What and is not configuration?

### This is configuration:

* dev / meta:
  * db
  * external services
  * flags
  * timeouts
  * i18n? \(debatable but probably not\)

### This is not configuration:

* i18n
* user preferences, even if that user is an "admin" of any sort
  * on the desktop, preferences may be user-level config \(e.g. Slack\)

