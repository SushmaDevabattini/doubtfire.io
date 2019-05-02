# Middleman Project Bootstrapper Website

A bootstrapper for generating basic, static Middleman websites.

![Sample Website](https://i.imgur.com/OLwEw2G.png)

## Getting started

Start by ensuring you have ruby on your system. You **must** install [rbenv](https://github.com/rbenv/rbenv) to keep your ruby versions under control. Refer to rbenv's [installation guide](https://github.com/rbenv/rbenv#installation) on how to do so.

Ensure you have installed ruby version 2.3.1:

```bash
$ rbenv install 2.3.1
$ rbenv rehash
```

Then, install [bundler](http://bundler.io) to sort out your ruby dependencies:

```bash
$ gem install bundler
$ bundle install
```

#### El Capitan and OpenSSL issues

If you are using OS X El Capitan, install OpenSSL using `brew` and set the bundle
config to point to this install:

```bash
$ brew install openssl
$ bundle config build.eventmachine --with-cppflags="-I/usr/local/opt/openssl/include -L/usr/local/opt/openssl/lib"
```

## Changing MyProject to Your Project

Under a text editor of your choice, do a search and replace for `MyProject`. These are references for where you will need to replace MyProject to relevant content of your choice. The main pieces of data that need to ne changed are:

1. `data/global/footer.yml`
1. `data/landing_page.yml`
1. `source/layouts/index.html.erb`
1. `source/partials/_navbar.html.erb`
1. `source/articles/contributing/index.html.md.erb`
1. `source/articles/index.html.erb`
1. `source/articles/installation/{mac,ubuntu,windows}/index.html.erb`

You can also change theme colors and typography under `stylesheets/modules/_{colors,typography}.scss`.

## Developing

Develop using:

```bash
$ bundle exec middleman
```

Your website will be watched and hosted locally at **[http://localhost:4567/](http://localhost:4567/)**.

## Bootstrap

We currently rely on a [Ruby Bootstrap gem](https://github.com/twbs/bootstrap-rubygem/tree/v4.0.0.alpha4) compiled with Bootstrap 4.0.0-alpha4.
Relevant SASS files can be found [here](https://github.com/twbs/bootstrap-rubygem/tree/v4.0.0.alpha4/assets/stylesheets).

## Disclaimer

This bootstrapper was generalised from the [SplashKit](https://github.com/splashkit/splashkit.io) website. There may be some files lurking around that still reference SplashKit-specific details. You can ignore these.

## Publishing

Publish using:

```bash
$ rake publish
```

If this fails, try rebuilding the build folder from scratch then redeploy:

```bash
$ rm -rf build
$ rake publish
```

## License

Licensed under the MIT Licence.








## Ontrack 

OnTrack is a web assessment tool that provides students with a task oriented approach to portfolio assessment to stay aligned by completing tasks as part of their learning. Students will work through a series of tasks in order to achieve a target grade to complete their unit learning outcomes.

OnTrack helps students to achieve their learning outcomes by taking the focus away from grades and placing the importance on learning of the content delivered by the unit. Grades will not be allocated for tasks during the course of their learning, instead, their learning will be assessed using the learning outcomes at the end of the unit.

The above will be achieved by the summative assessments completed at the end of the unit, by determining student grades with the evidence they present in their portfolio. The portfolio will consist of work that the student complete as part of tasks assigned in the unit. These tasks are designed in order to help students learn and demonstrate their achievements as part of learning outcomes of a unit.

## Create and Manage units

 [Details](https://doubtfire-lms.github.io/doubtfire.io/articles/guides/tags/unit_chair_guides/creating-and-managing-units/)
