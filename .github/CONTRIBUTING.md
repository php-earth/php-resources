# Contributing guide to PHP resources

We love contributors and people willing to help.

## How can you help?

* Report issues
* Fix typos and grammar
* Add new content
* Improve existing chapters

## Contributing procedure

Below describes the procedure for contributing to this repository in particular
and some extra information about it.

* Fork this repository over GitHub
* Create a separate branch, for instance `patch-1`, so you will not need to
  rebase your fork if your master branch is merged

  ```bash
  git clone git@github.com:your_username/docs
  cd docs
  git checkout -b patch-1
  ```
* Make changes, commit them and push to your fork

  ```bash
  git add .
  git commit -m "Fix typo in the FAQ"
  git push origin patch-1
  ```
* Open a pull request

## Style guide

* This repository uses [Markdown](https://daringfireball.net/projects/markdown/)
  syntax and follows
  [cirosantilli/markdown-style-guide](http://www.cirosantilli.com/markdown-style-guide/)
  style guide.

* Code examples follow [PSR-1](http://www.php-fig.org/psr/psr-2/),
  [PSR-2](http://www.php-fig.org/psr/psr-2/) and
  [extended code style guide proposal](https://github.com/php-fig/fig-standards/blob/master/proposed/extended-coding-style-guide.md).

* The preferred spelling of English words is the [American
  English](https://en.wikipedia.org/wiki/American_English) (e.g. behavior, not
  behaviour).

* Titles [capitalization](https://en.wikipedia.org/wiki/Letter_case#Headings_and_publication_titles)
  follow the [ISO](https://www.iso.org) recommendation of sentence-case style,
  where capitalisation follows the same rules that apply for sentences. Instead
  of *Frequently Asked PHP Questions*, use *Frequently asked PHP questions* in
  all titles and subtitles. In rare cases where you need to make the title important,
  and more special, you can use the so called title-case style, which has
  capitalized certain words such as nouns, pronouns, adjectives, verbs, adverbs,
  and subordinate conjunctions, but not articles, short prepositions, and
  conjunctions.

* Use gender-neutral language (instead of *he* or *she* use *they*, *them*,
  *their*, *theirs*, *themselves*).

* Use second person point of view (instead of *I* and *we*, use *you*). Avoid
  [nosism](https://en.wikipedia.org/wiki/Nosism).

## Images

Some images are created with the [draw.io](https://www.draw.io) tool. They are
also located in a [separate repository](https://github.com/phpearth/assets).

## Folder structure

Documentation is organized using a custom yet simple and effective folder
structure. Each folder indicates a documentation section and each `README.md`
file contains a list of chapters for given section. When rendered either on GitHub
or online, the `README.md` is the index file for that particular section.

## YAML front matter

Some content includes YAML front matter blocks with parameters that define
some extra content information.

For example:

```Markdown
---
description: This is the chapter description.
redirect_from:
  - general/chapter
  - old-url/chapter
---

# Chapter title

Chapter content
```

Parameters:

* `permalink` - URL path of the content
* `title` - defines page title, otherwise first H1 is used
* `image` - image used for open graph
* `redirect_from` - 301 redirects of previous URLs

  These files get refactored all the time and redirections should also be done
  at such changes. When a Markdown file is moved, a new redirect_from is added.

* `description` - used as a page description

## GitHub issues labels

Labels are used to organize issues and pull requests into manageable categories.
The following labels are used:

* **duplicate** - Attached when the same issue or pull request already exists.
* **easy pick** - Requires simple work.
* **enhancement** - New feature.
* **faq** - Attached for FAQ section content.
* **hacktoberfest** - Attached for open source
  [Hacktoberfest](https://hacktoberfest.digitalocean.com/) event.
* **invalid** - Attached when
* **needs review** - Attached when further review is required.
* **new content** - For new articles or new FAQs.
* **question** - Attached for questions or discussions.
* **wontfix** - Attached when decided that issue will not be fixed.

## License

By contributing to this repository you agree to share knowledge under the
Creative Commons Attribution-ShareAlike 4.0 International and code under the
public domain. See [LICENSE](https://github.com/phpearth/docs/blob/master/LICENSE)
file for more information.

## Testing

Checking for Markdown errors and issues before publishing documentation online
is happening via [Travis](https://travis-ci.org/phpearth/docs).

## Release process

*(For repository maintainers)*

1. Update the [PHP.earth](https://php.earth/doc) website accordingly.
