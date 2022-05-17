# Luciana Lab Website

This website is built with [Jekyll](https://jekyllrb.com/).

## Setup

```
brew install ruby
gem install bundler jekyll
```

Clone this repository, then install the dependencies:

```
bundle install
```

## Run

Run the local webserver with:

```
bundle exec jekyll serve
```

## Contribute

### Add new publications
Work in progress
### Add or change a member

New members are stored as markdown files under [_pages/members/_posts](_pages/members/_posts).

Each new member `.md` file must look like this:

``` yaml
---
layout: lab_member
category: choose from; undergraduate, staff, graduate student, investigator, postdoc
title: full name of lab member (including degree if applicible; e.g., Monica Luciana, PhD)
short-name: short name of lab member (e.g, Monica Luciana)
image: file name in folder /assets/images/members (use a square image)
role: describe member's role in labe
alumni: set to either true or false
permalink: members/name-of-member
social:
    twitter: 
    linkedin: 
    google-scholar: 
    github:
    website: 
    research-gate: 
education:
 - (degree) (university) (year)
 - (degree) (university) (year)
contact:
    umn-email: 
    phone: 
---

Write bio text.

```

### Add news

News is stored as `.yml` file under [_data/news.yml](_data/news.yml).

An entry looks like the following:

```yaml
- date: 03/09/19
  title: "Something great"
  tags:
    - some
    - tags
  content: Lorem ipsum dolor sit amet, consectetur adipiscing elit,
    sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
    Eu turpis egestas pretium aenean. Luctus venenatis lectus magna fringilla
    urna porttitor. Lorem ipsum dolor sit amet. Pellentesque massa placerat
    duis ultricies. Commodo viverra maecenas accumsan lacus vel.
```

### Edit templates

We use [Bootstrap](https://getbootstrap.com/) for designing the website. Feel free to modify either the [_pages](_pages/) or the [_layouts](_layouts/) components.
