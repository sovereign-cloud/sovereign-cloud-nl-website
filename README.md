# Sovereign Cloud NL Community website

## Install Prequisites

To render the website a recent [hugo](https://gohugo.io) installation is required.  To install hugo on your system choose from one of the following options:

1. If you already have `go get` set up, the easiest way to get `hugo` in the required version is: `go get -u github.com/gohugoio/hugo/`.
2. Download and install hugo [from one of their releases](https://github.com/gohugoio/hugo/releases), make sure to download the "hugo_extended_XXXX" file for your OS.  The latest version should work, at the time of writing this it is 0.73.  Either install it, or unpack and put the binary in your path.  On Ubuntu this process can be done with:
   * `cd ~/Downloads`
   * `wget https://github.com/gohugoio/hugo/releases/download/v0.119.0/hugo_0.119.0_linux-amd64.deb`
   * `sudo dpkg -i hugo_0.119.0_linux-amd64.deb`

Another way is installing the hugo packaged by your distro, their version of hugo is likely not the newest release.

## Run local development version

First clone the repository and ensure you include the submodule by running `git clone --recurse-submodules https://github.com/sovereign-cloud/sovereign-cloud-nl-website.git`.
Actually the used theme is included as submodule, which is [Clarity](https://github.com/chipzoller/hugo-clarity).

For viewing a new blogpost/news/article draft run `hugo -D server` and visit the rendered version in your browser at `localhost:1313`. The `-D` is required to show entries which are not yet marked for publishing with `draft: false`.

For commiting new changes, don't forget to sign your commits with a valid GPG key.

## Production releases

For production releases a `Github Actions` workflow is triggered. You may want to follow the status here [Deployment status](https://github.com/sovereign-cloud/sovereign-cloud-nl-website/actions)

## How to add stuff to the website

If you want to make a change to the website, add a news or blog item, fix a
typo or whatever, simply clone this repo and make a pull request against it.
When the admins approve the PR, we will re-generate the website and upload the
new version.

This website uses the Hugo static site generator. Its documentation can be
found here: https://gohugo.io/documentation/

### How to add a news or blog article

If you have Hugo installed in a reachable path, simply run

    hugo new content/posts/2023-XX-XX-short-title.md

or

    hugo new content/archive/2023-XX-XX-short-title.md

and it will create a template for a new article on the blogs or archive page. Alternatively, copy an old news or blog item (if you don't have Hugo running) and modify it accordingly.

Before submitting a pull request, make sure to remove the `draft: true` line
from the file.

### How to add images, icons or other graphics

Images can be added to the `images` folder, which is under `static/images`. Ensure you use optimized pictures like `.png` or `webp` format.

### Where is the configuration located

Configuration can be found under `config` folder, which contains `_default` and at the moment a dummy `production` folder. Changes for production can be moved later to `production`.
In the end an environment configuration setting supersedes a default setting. Keep this in mind!
