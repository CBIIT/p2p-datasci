# GitHub Pages Instructions

## Notes

* The following sections are in reverse chronological order (i.e., starting from scratch, I started from the bottom section, not the top one). This allows me to keep the most recent section's documentation at the top. Hence the reverse section numbering.

## Stuff to incorporate from old README

* TLDR:
  * Clone the repository to somewhere on your computer (or Biowulf): `git clone https://github.com/CBIIT/p2p-datasci.git`
    * I already cloned a version you can use at `/data/BIDS-HPC/public/software/checkouts/CBIIT/p2p-datasci` on Biowulf if you'd prefer
  * Checkout the `gh-pages` branch: `git checkout gh-pages`
  * Modify the `*.md` files (or create new ones) therein
  * Commit and push your changes using the usual `git` commands, e.g.,
    * `git commit -a -m "My commit message"`
    * `git push`
* [`git` references](https://try.github.io)
* Full website instructions [here](https://github.com/daattali/beautiful-jekyll)
* Site URL: [https://cbiit.github.com/p2p-datasci](https://cbiit.github.com/p2p-datasci)
* [Markdown tutorial](https://markdowntutorial.com)
* Be sure to use the `gh-pages` branch (`git checkout gh-pages`) in order to modify the site
* Use the `master` branch (`git checkout master`) to version-control files related to the program
* Most configuration settings are located in [`_config.yml`](https://github.com/CBIIT/p2p-datasci/blob/gh-pages/_config.yml)
* The homepage is [https://cbiit.github.com/p2p-datasci](https://cbiit.github.com/p2p-datasci) and corresponds to the file [`index.md`](https://github.com/CBIIT/p2p-datasci/blob/gh-pages/index.md)
* Other files/pages are https://cbiit.github.com/p2p-datasci/PAGENAME and correspond to the files `PAGENAME.md`
* Instructions to set up the site the first time (after creating the repository as usual):
  * `git branch gh-pages`
  * `git checkout gh-pages`
  * `git remote add upstream https://github.com/daattali/beautiful-jekyll`
  * `git fetch upstream`
  * `git merge upstream/master`
* To pull in from the upstream repository in order to get any updates to the template (from the `gh-pages` branch):
  * `git fetch upstream`
  * `git merge upstream/master`
* Git repository [homepage](https://github.com/CBIIT/p2p-datasci)
* Note there is an easier way to edit the site not using command line tools I believe; see [prose.io](https://prose.io). You can also edit the files straight on GitHub.

## 3. Site guidelines

### Full webpage and cover image listing as of 6/29/20

Note: All "cover images" are from [here](https://insite.cancer.gov/docs/DOC-2238)

Starting from the [top directory](https://github.com/CBIIT/p2p-datasci/tree/gh-pages):

* /assets/img/antibodies.jpg (main image)
  * index.html (blog post listing / landing page)
  * _posts/2020-04-07-program_announcement.md (original program announcement)
  * tags.html (tag listing, i.e., when you click on a tag)
* /assets/img/zebrafish.jpg (material-availability tags)
  * _posts/2020-04-21-data_science_course_licenses.md
  * _posts/2020-06-25-materials_from_mortality_tracker_workshop_now_available.md
* /assets/img/library.jpg (events, including events.md main page and event-announcement tags)
  * events.md
  * _posts/2020-06-15-real-time_fair_mortality_tracking.md
  * _posts/2020-06-29-machine_learning_for_drug_function_classification.md
* /assets/img/tem.jpg
  * gettingstarted.md
* /assets/img/yanling.jpg
  * beginner-resources.md
* /assets/img/kedar.jpg
  * intadv-resources.md
* /assets/img/collaboration.jpg
  * collabtools.md

Viable unused images:

* /assets/img/atrf.jpg
* /assets/img/atrium.jpg
* /assets/img/data_center.jpg
* /assets/img/eric.jpg

## 2. How to merge the current DSLX website into the test one

For reference, the commit number of the test website ([https://andrew-weisman.github.io/p2p-datasci-test](https://andrew-weisman.github.io/p2p-datasci-test)) is `62e3f65c4b9db060f44ac3bc200a1fcac1011913`.

The commit number of the current DSLX website ([https://cbiit.github.io/p2p-datasci](https://cbiit.github.io/p2p-datasci)) is `5f579e50d0ac7f0b6ff134abcab5b428871ba395`.

Now trying the following commands from the `gh-pages` branch of `https://github.com/andrew-weisman/p2p-datasci-test`:

```bash
git remote add production https://github.com/CBIIT/p2p-datasci
git fetch production
git merge production/gh-pages
```

Upon fixing merge conflicts, this worked! I am now refactoring the website here (i.e., at the test website).

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
