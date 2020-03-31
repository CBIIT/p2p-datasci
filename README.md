# p2p-datasci

## Andrew to-do
* Need to add usernames for admins (can sign up for one [here](https://github.com/join))

## Notes
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
* The homepage is [https://cbiit.github.com/p2p-sdsi](https://cbiit.github.com/p2p-sdsi) and corresponds to the file [`index.md`](https://github.com/CBIIT/p2p-datasci/blob/gh-pages/index.md)
* Other files/pages are https://cbiit.github.com/p2p-sdsi/PAGENAME and correspond to the files `PAGENAME.md`
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
* Note there is an easier way to edit the site not using command line tools I believe; see [prose.io](https://prose.io).
