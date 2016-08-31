# FAQ for 18F's State Child Welfare partners

A collection of questions frequently received from our state child welfare partners.

## Running Locally

You will need [Jekyll](https://jekyllrb.com/) in order to run locally.  From the
root directory, you can just run `jekyll serve` which will create a local web
server and automatically rebuild the site as you make changes.  It will also
print out the URL to look at your local copy of the site.

## Adding a question

Currently questions fall into a handful of existing categories: agile,
evaluation, costs, multi-system, cots, and technical.  If your question falls
outside of these existing categories, also see the next section.

1. Create a new file in the `_posts` directory named like this:
`YYYY-MM-DD-post-name.markdown`, where `YYYY-MM-DD` represents a
date and `post-name` is a useful name to make the file easier to find.

  * The date is required by Jekyll, and is used for sorting purposes.  The
  files with the most recent date in their filename will appear at the top.
  The question/answer pairs can be rearranged within a category just be
  renaming files.

2. At the very top of this new file, add the Jekyll "front matter" to describe it:

  ```
  ---
  layout: post
  title: <The question>
  category: Agile
  ---
  ```

  * "The question" should be the text of the question; e.g., "What is the best
  color for a horse?"
  * The category is one of the five described above (or the new one you're
  creating, in which case see the next section).

3. Add your content under the "front matter."  This can be in markdown, so go
to town with the formatting!

4. Commit your changes to the git repo.

## Adding a Category

There's only one primary step to adding a new category.  In the file
`index.html` at the project root, you will need to add a display name
and category name in the front matter:

```
---
layout: default
categories:
  Agile Development: Agile
  My New Category: new-category
---
```

Then, when you create your question (as described in the previous section), in
the front matter, set `category: new-category`.

## Public domain

This project is in the worldwide [public domain](LICENSE.md).   As stated
in [CONTRIBUTING](CONTRIBUTING.md):

> This project is in the public domain within   the United States, and
copyright and related rights in the work worldwide are waived through
the [CC0 1.0 Universal public domain dedication](https://creativecommons.org/publicdomain/zero/1.0/).

> All contributions to this project will be released under the CC0 dedication.
By submitting a pull request, you are agreeing to comply with this waiver of
copyright interest.
