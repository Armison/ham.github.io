[Ham's Notes](https://ham.github.io)
================================

# Getting Started

1. You will need [Ruby](https://www.ruby-lang.org/en/) and [Bundler](https://bundler.io/) to use [Jekyll](https://jekyllrb.com/). Following [Using Jekyll with Bundler](https://jekyllrb.com/tutorials/using-jekyll-with-bundler/) to fullfill the enviromental requirement.

2. Installed dependencies in the `Gemfile`:

```sh
bundle install 
```

3. Serve the website (`localhost:4000` by default):

```sh
bundle exec jekyll serve  # alternatively, npm start
```

# Error Fix
>jekyll/commands/serve/servlet.rb:3:in `require': <font size=3 color=#D2691E>cannot load such file -- webrick</font> (LoadError)


```sh
npm install webrick
bundle add webrick
```

# Development (Build From Source)

To modify the theme, you will need [Grunt](https://gruntjs.com/). There are numbers of tasks you can find in the `Gruntfile.js`, includes minifing JavaScript, compiling `.less` to `.css`, adding banners to keep the Apache 2.0 license intact, watching for changes, etc. 

Yes, they were inherited and are extremely old-fashioned. There is no modularization and transpilation, etc.

Critical Jekyll-related code are located in `_include/` and `_layouts/`. Most of them are [Liquid](https://github.com/Shopify/liquid/wiki) templates.

This theme uses the default code syntax highlighter of jekyll, [Rouge](http://rouge.jneen.net/), which is compatible with Pygments theme so just pick any pygments theme css (e.g. from [here](http://jwarby.github.io/jekyll-pygments-themes/languages/javascript.html) and replace the content of `highlight.less`.


```sh
npm install grunt --save-dev
npm install grunt-contrib-jshint --save-dev
npm install -g grunt-cli 

grunt
```

# License
Apache License 2.0
Copyright (c) 2022-present Ham

This Blog is derived from [Hux BLog](https://github.com/Huxpro/huxpro.github.io)



# use ruby 3.3 

ruby@3.3 is keg-only, which means it was not symlinked into /opt/homebrew,
because this is an alternate version of another formula.

If you need to have ruby@3.3 first in your PATH, run:
  echo 'export PATH="/opt/homebrew/opt/ruby@3.3/bin:$PATH"' >> ~/.zshrc

For compilers to find ruby@3.3 you may need to set:
  export LDFLAGS="-L/opt/homebrew/opt/ruby@3.3/lib"
  export CPPFLAGS="-I/opt/homebrew/opt/ruby@3.3/include"