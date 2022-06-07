# Portfolio Github Page

This is a github page to showcase all of my projects.

## Setup Instructions

In depth instructions located here:
[Github Pages Gem Repo](https://github.com/github/pages-gem)

### Docker based workflow
1. Clone repo
2. `make image` @ root of repo
3. `source $PATH_TO_THIS_DIRECTORY/contrib/func.sh` added to `.bashrc`
4. `github-pages [$path-to-site] [$port]` to host in local container

### Issues Encountered & Solutions
- **Problem:** the theme does not appear to be loading properly.
  - Needed to copy default layout into `_layouts/default.html` even though it appeared the theme was loading properly from the output of the github-pages command

