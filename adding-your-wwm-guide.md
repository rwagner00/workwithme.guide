---
layout: default
---

## Adding Your Work With Me Guide

There are two different repositories with similar names, i.e. `workwithme.guide-myguide` and `workwithme.guide`.  The first repository in the instructions below (i.e. workwithme.guide-myguide) is for your personal work with me profile page, the other repository (i.e. workwithme.guide) in step 3 is this website's repository; think of the website repository as the place where _all_ work with me profile pages can reside.  Let's get started!

1. First we're going to make your personal work with me profile page.  Fork [workwithme.guide-myguide](https://github.com/abloomston/workwithme.guide-myguide) on GitHub.  We'll call this the profile repository.
2. With your forked profile repository, modify `index.md`, optionally adding a profile picture to the top level directory.  Make sure your edits are pushed _your_ fork of the profile repository.
3. Next fork [this project]({{ site.github.repository_url }}) on GitHub.  We'll call this the website repository.  Clone this forked website repository.
4. Now we combine _your_ profile repository with your fork of the website repository by a [submodule command](https://git-scm.com/book/en/v2/Git-Tools-Submodules).  Using your cloned website repository on your local machine, run `git submodule add -b master https://github.com/USERNAME/workwithme.guide-myguide.git WWM_LINK` where `USERNAME` is your GitHub username and `WWM_LINK` is the link you'd like at `workwithme.guide/WWM_LINK`.  To explain what's going on, `https://github.com/USERNAME/workwithme.guide-myguide.git` should be your forked profile repository and `WWM_LINK` creates a folder with the contents of your profile repository. If you don't specify `WWM_LINK`, your link will end up being `https://workwithme.guide/workwithme.guide-myguide`.
5. We should now have _your_ profile repository as a submodule in _your_ website repository.  Push your changes and  make a [Pull Request](https://help.github.com/articles/about-pull-requests/) to this repo `abloomston/workwithme.guide`, not `pages-themes/minimal`. This is how you will make changes to your Work With Me Guide (for now--this is a prototype).
6. Once I merge your Pull Request your Work With Me Guide will be available at `https://workwithme.guide/WWM_LINK`.
