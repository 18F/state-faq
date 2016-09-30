# FAQ for 18F's state and local partners

We've heard a lot of questions from our state and local partners.  This is where we've tried to put them all in one place and answer them, so they and future partners can have a resource to turn to.

## Running locally

You will need [Jekyll](https://jekyllrb.com/) in order to run locally.  From the
root directory, you can just run `jekyll serve` which will create a local web
server and automatically rebuild the site as you make changes.  It will also
print out the URL to look at your local copy of the site.

## Adding a page

To add a new page, just create a new Markdown file in the `pages` directory.  Put this at the very top of your new markdown file:

```
---
layout: post
title: [Full title]
category: Modular procurement
permalink: /[short-title]/
---
```

The full title will be displayed at the top of your page.  Go ahead and make it descriptive.  The `short-title` will be used in the URL (e.g., [https://pages.18f.gov/state-faq/short-title/](), so try to make it something short, meaningful, and no spaces!  After that, just put in your markdown!

## Getting it published

Ideally you will make your changes on your own branch, push that to Github, and then create a [pull request](pulls).  By default, the pull request will go to the 18f-pages branch.  Once someone reviews it (you may need to ping in Slack to get attention, or assign it to someone if you know they'll want to review), they will merge it and a short while later (usually less than a minute!) your changes will be live on the site.

## Public domain

This project is in the worldwide [public domain](LICENSE.md).   As stated
in [CONTRIBUTING](CONTRIBUTING.md):

> This project is in the public domain within   the United States, and
copyright and related rights in the work worldwide are waived through
the [CC0 1.0 Universal public domain dedication](https://creativecommons.org/publicdomain/zero/1.0/).

> All contributions to this project will be released under the CC0 dedication.
By submitting a pull request, you are agreeing to comply with this waiver of
copyright interest.
