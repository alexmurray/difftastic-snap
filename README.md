# [difftastic](https://github.com/wilfred/difftastic) in a snap #

-------------------------------------------------------------------------------

[![difftastic](https://snapcraft.io/difftastic/badge.svg)](https://snapcraft.io/difftastic)

## Installation ##

[![Get it from the Snap Store](https://snapcraft.io/static/images/badges/en/snap-store-black.svg)](https://snapcraft.io/difftastic)

``` shell
sudo snap install difftastic
```
## Usage with git as a diff tool ##

As a snap, difftastic is not able to access the standard `/tmp` directory. This can be worked around by ensuring that when git is invoked, it uses a temporary directory that the difftastic snap can access. To use the difftastic snap as an external diff tool with git, it should be
invoked as follows, using the user's own `/tmp` within their home directory:

```shell
TMPDIR=~/tmp GIT_EXTERNAL_DIFF="difftastic" git diff
```

([Don't have snapd installed?](https://snapcraft.io/docs/core/install))
