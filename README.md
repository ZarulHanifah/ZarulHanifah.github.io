# Contributions welcome!

If you want to contribute to the web page, whether it is to fix something somewhere, or to write a blog post, there are two things you need to do.

The first is to be able to run the web page locally so you can see how things are rendered and how they will look online when you finally commit your changes to this repository. The remainder of this document will help you run the web site locally.

The second is to take a look at these tips which will help you to be able to use all the little toys we have for content developers:

http://fastgenomicssolutions.com/web-tips/

# How to run a copy of this website locally

Installing ruby on Mac is always a pain. But you can start with this (newer versions of ruby may cause you trouble with some of the gems):

```
brew install ruby@2.7
```

This step may ask you to add things to your `~/.bash_profile` to update your `$PATH`, which you should do, and then either open a new terminal, or run `source ~/.bash_profile`, so the output for `which ruby` looks something like this:

```
/usr/local/opt/ruby@2.7/bin/ruby
```

Once you're done with these initial steps, you can get a copy of the web site from GitHub:

```
mkdir -p ~/github
cd ~/github/

git clone https://github.com/zarulhanifah/web.git
```

To make sure you have the necesary gems, run:

```
cd web
bundle install
```

And run the following command in this directory:

```
bundle exec jekyll serve --incremental
```

You should see a similar output in your terminal:

```
Configuration file: /home/ahbui/Zarul/ZarulHanifah.github.io/_config.yml
            Source: /home/ahbui/Zarul/ZarulHanifah.github.io
       Destination: /home/ahbui/Zarul/ZarulHanifah.github.io/_site
 Incremental build: disabled. Enable with --incremental
      Generating... 
                    done in 1.515 seconds.
/home/ahbui/Zarul/Software/miniconda3/envs/jekyll/share/rubygems/gems/pathutil-0.16.2/lib/pathutil.rb:502: warning: Using the last argument as keyword parameters is deprecated
 Auto-regeneration: enabled for '/home/ahbui/Zarul/ZarulHanifah.github.io'
    Server address: http://127.0.0.1:4000
  Server running... press ctrl-c to stop.
```

This basically runs a local server for you to see the changes you've made locally. You can access to this server by visiting the URL `http://127.0.0.1:4000/` with your browser.

With the `--incremental` flag every change you will make in any of the files will be reflected to your local website automatically.

If you are not seeing some of the changes you expect to see, press `ctrl-c` to stop the server on your termianl, clean out the static web directory by running the command `rm -rf _site/`, and re-run the server using the command above.

---

Congratulations!
