# Doubtfire Website
Doubtfire is an open-source, innovative, learning management system designed to put the student first.

![Sample Website](webpage.png)

Inside the webiste, you can find :
1. Installation guides for Doubtfire.
2. User guides.
3. Extend Doubtfire and Contributions.
[Go to Website](https://doubtfire-lms.github.io/doubtfire.io/)

## How did we create the website?
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
## create guides
To create a new guide, navigate to the directory where you cloned the repository:
**cd /path/to/doubtfire.io**
Guides are categorised using a tag. Once you have decided for one or more tag for your guide, execute the following command:
**bundle exec middleman article "[Name of Guide]" -t [tags]**
Once you execute this command, you will see that the guide you have named appears under source/articles/guides using the current day’s date. For example, 
**source/articles/guides/20XX-XX-XX-my-guide.html.md.**
create guides as follows:

1. `data/global/footer.yml`
1. `data/landing_page.yml`
1. `source/layouts/index.html.erb`
1. `source/partials/_navbar.html.erb`
1. `source/articles/contributing/index.html.md.erb`
1. `source/articles/index.html.erb`
1. `source/articles/installation/{mac,ubuntu,windows}/index.html.erb`
Add theme colors and typography under `stylesheets/modules/_{colors,typography}.scss`.
 Read more on >> [writing guides](https://doubtfire-lms.github.io/doubtfire.io/articles/contributing/)
 
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
