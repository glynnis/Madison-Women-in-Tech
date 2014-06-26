Madison Women in Tech (madisonwomenintech.com)
=====================

This is the repo for the Madison Women in Tech website. The site is an easy way to point members to our shared spaces online, and to share resources and announcements. It's also the easiest way to sign up for our new newsletter.

## Getting started

The site is built in Jekyll, which is a static site generator based in Ruby. Check out the Jekyll docs here: http://jekyllrb.com/docs/home/

Start by cloning the repo.
```
git clone https://github.com/glynnis/Madison-Women-in-Tech.git
```

You'll need ruby installed on your machine. If you've used Rails before, Jekyll will feel familiar. The site also uses HAML and SASS.

Like Rails, Jekyll uses layouts files to create the main markup of the site. `_layouts/haml/default.haml` is currently the only layout being used.

`_includes` is the directory where you'll find partials--small files that get included in layouts like a header or footer. Any edits you make should be done to the files in the `haml/` directory, as these are the files that will be compiled when you generate the site (and creates HTML).

`index.haml` contains all the main content and copy of the current site. If you have content to add to the homepage, add it here.

## Building the site

When you've modified files and are ready to view the site locally, type `rake preview` in your terminal to build the site (building without running a server can be done with `rake build`). Then visit `http://localhost:4000/` in your browser.

If you're ready for a deploy, add your changes to a branch and submit a pull request. Glynnis will approve the pull request, build the static site locally, and deploy to production.
