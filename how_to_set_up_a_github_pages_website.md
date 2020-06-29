# GitHub Pages Instructions

## Notes

* The following sections are in reverse chronological order (i.e., starting from scratch, I started from the bottom section, not the top one). This allows me to keep the most recent section's documentation at the top. Hence the reverse section numbering.

## 2. How to merge the current DSLX website into the test one

For reference, the commit number of the test website ([https://andrew-weisman.github.io/p2p-datasci-test](https://andrew-weisman.github.io/p2p-datasci-test)) is `62e3f65c4b9db060f44ac3bc200a1fcac1011913`.

The commit number of the current DSLX website ([https://cbiit.github.io/p2p-datasci](https://cbiit.github.io/p2p-datasci)) is `5f579e50d0ac7f0b6ff134abcab5b428871ba395`.

Now trying the following commands from the `gh-pages` branch of `https://github.com/andrew-weisman/p2p-datasci-test`:

```bash
git remote add production https://github.com/CBIIT/p2p-datasci
git fetch production
git merge production/gh-pages
```

## 1. How to set up a GitHub Pages website

Create an empty public repository on GitHub, e.g., `https://github.com/CBIIT/p2p-datasci` or `https://github.com/andrew-weisman/p2p-datasci-test` (this repository).

The instructions below are loosely based on those [here](https://github.com/daattali/beautiful-jekyll). [Here](https://deanattali.com) is a non-VPN-blocked example of what the template can deliver. Recently, the NIH VPN has blocked the [actual demo site](https://beautifuljekyll.com) for this template.

Create and switch to a `gh-pages` branch in your new repository (note you may have to first initialize the repository by creating an initial commit):

```bash
git branch gh-pages
git checkout gh-pages
```

Note that the website data itself will be in the `gh-pages` branch, whereas you can put some actual files you want to version-control using GitHub in the `master` (or any other) branch.

Rather than forking the repository as on the official template's directions webpage above, I would instead simply add the template as a Git remote called `upstream`:

```bash
git remote add upstream https://github.com/daattali/beautiful-jekyll
```

Note that you only need to do this once ever.

Now pull the template files into your `gh-pages` branch (these are the steps you'll regularly need to do in order to stay up-to-date with the official template):

```bash
git fetch upstream
git merge upstream/master # at least the first time you may need to add the "--allow-unrelated-histories" option if you get the error "fatal: refusing to merge unrelated histories"
```

Since you have specifically named the branch `gh-pages`, then the GitHub Pages renderer should automatically recognize it as the source for the website and use it to render the site. E.g., it is at this point that going to [https://andrew-weisman.github.io/p2p-datasci-test](https://andrew-weisman.github.io/p2p-datasci-test) works for me. I haven't tested it but I'd imagine that for group accounts like CBIIT, this should work the same way.

In other words, you shouldn't have to go into the GitHub repository Settings (gear icon) at all!