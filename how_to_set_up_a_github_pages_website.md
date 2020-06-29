# How to set up a GitHub Pages website

Create an empty public repository on GitHub, e.g., `https://github.com/CBIIT/p2p-datasci` or `https://github.com/andrew-weisman/p2p-datasci-test` (this repository).

The instructions below are loosely based on those [here](https://github.com/daattali/beautiful-jekyll). [Here](https://deanattali.com) is a non-VPN-blocked example of what the template can deliver. Recently, the NIH VPN has blocked the [actual demo site](https://beautifuljekyll.com) for this template.

Create and switch to a `gh-pages` branch in your new repository (note you may have to first initialize the repository by creating an initial commit):

```bash
git branch gh-pages
git checkout gh-pages
```

Note that the website data itself will be in the `gh-pages` branch, whereas you can put actual files you want to version-control using GitHub in the `master` (or any other) branch.

Rather than forking the repository as on the official templates directions webpage above, I would instead simply as the template as a Git remote called `upstream`:

```bash
git remote add upstream https://github.com/daattali/beautiful-jekyll
```

Note that you only need to do this once.

Now pull the template files into your `gh-pages` branch (these are the steps you'll regularly need to do in order to stay up-to-date with the official template):

```bash
git fetch upstream
git merge upstream/master # at least the first time you may need to add the "--allow-unrelated-histories" option is you get the error "fatal: refusing to merge unrelated histories"
```
