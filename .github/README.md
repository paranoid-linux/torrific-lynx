# Torrific Lynx
[heading__top]:
  #torrific-lynx
  "&#x2B06; Enables clear-net browsing over the Tor network via Lynx web browser"


Enables clear-net browsing over the Tor network via Lynx web browser


## [![Byte size of Torrific Lynx][badge__main__torrific_lynx__source_code]][torrific_lynx__main__source_code] [![Open Issues][badge__issues__torrific_lynx]][issues__torrific_lynx] [![Open Pull Requests][badge__pull_requests__torrific_lynx]][pull_requests__torrific_lynx] [![Latest commits][badge__commits__torrific_lynx__main]][commits__torrific_lynx__main]



------


- [:arrow_up: Top of Document][heading__top]

- [:building_construction: Requirements][heading__requirements]

- [:zap: Quick Start][heading__quick_start]

- [&#x1F9F0; Usage][heading__usage]

- [&#x1F5D2; Notes][heading__notes]

- [:card_index: Attribution][heading__attribution]

- [:balance_scale: Licensing][heading__license]


------



## Requirements
[heading__requirements]:
  #requirements
  "&#x1F3D7; Prerequisites and/or dependencies that this project needs to function properly"


Prior to utilizing this project, the Lynx web browser should be installed, and `bash --version` should report a version number of `4` or greater.


Optional dependencies include [`firejail`][firejail__source] and `socat`, for process sandboxing and DNS over Tor respectively.


This repository makes use of Git Submodules to track Bash script dependencies, to avoid incomplete downloads clone with the `--recurse-submodules` option...


```Bash
git clone --recurse-submodules git@github.com:paranoid-linux/torrific-lynx.git
```


To update tracked Git Submodules issue the following commands...


```Bash
git pull

git submodule update --init --merge --recursive
```


To force upgrade of Git Submodules...


```Bash
git submodule update --init --merge --recursive --remote
```


> Note, forcing and update of Git Submodule tracked dependencies may cause instabilities and/or merge conflicts; if however everything operates as expected after an update please consider submitting a Pull Request.


___


## Quick Start
[heading__quick_start]:
  #quick-start
  "&#9889; Perhaps as easy as one, 2.0,..."


Clone this repository along with the submodules it depends upon...


```Bash
mkdir -p ~/git/hub/paranoid-linux

cd ~/git/hub/paranoid-linux

git clone --recurse-submodules git@github.com:paranoid-linux/torrific-lynx.git
```


Install via a symbolic link to a directory listed within your system's `PATH` variable, eg...


```Bash
cd ~/git/hub/paranoid-linux/torrific-lynx

ln -s "${PWD}/torrific-lynx" "${HOME}/bin/"
```


Update configurations files if defaults need modifications...


```Bash
cd ~/git/hub/paranoid-linux/torrific-lynx

sudo ./update-configs.sh --help
```


___


## Usage
[heading__usage]:
  #usage
  "&#x1F9F0;"


Call script with `--help` option to list available parameters...


```Bash
torrific-lynx --help
```


Pass a URL on the command-line to start Lynx and load that site...


```Bash
torrific-lynx 'https://duckduckgo.com'
```


___


## Notes
[heading__notes]:
  #notes
  "&#x1F5D2; Additional things to keep in mind when developing"


This repository may not be feature complete and/or fully functional, Pull Requests that add features or fix bugs are certainly welcomed.


- [Fork][torrific_lynx__fork_it] this repository to an account that you have write permissions for.

- Add remote for fork URL. The URL syntax is _`git@github.com:<NAME>/<REPO>.git`_...


```Bash
cd ~/git/hub/paranoid-linux/torrific-lynx

git remote add fork git@github.com:<NAME>/torrific-lynx.git
```


- Commit your changes and push to your fork, eg. to fix an issue...


```Bash
cd ~/git/hub/paranoid-linux/torrific-lynx


git commit -F- <<'EOF'
:bug: Fixes #42 Issue


**Edits**


- `<SCRIPT-NAME>` script, fixes some bug reported in issue
EOF


git push fork main
```


> Note, the `-u` option may be used to set `fork` as the default remote, eg. _`git push fork main`_ however, this will also default the `fork` remote for pulling from too! Meaning that pulling updates from `origin` must be done explicitly, eg. _`git pull origin main`_


- Then on GitHub submit a Pull Request through the Web-UI, the URL syntax is _`https://github.com/<NAME>/<REPO>/pull/new/<BRANCH>`_


> Note; to decrease the chances of your Pull Request needing modifications before being accepted, please check the [dot-github](https://github.com/paranoid-linux/.github) repository for detailed contributing guidelines.


___


## Attribution
[heading__attribution]:
  #attribution
  "&#x1F4C7; Resources that where helpful in building this project so far."


- [GitHub -- `github-utilities/make-readme`](https://github.com/github-utilities/make-readme)

- [Reddit -- Hou to use Lynx over Tor?](https://www.reddit.com/r/TOR/comments/72aqlj/how_to_use_lynx_over_tor/dnh5gcj/)

- [Lynx -- Description of settings in lynx configuration file](https://lynx.invisible-island.net/lynx_help/body.html)

- [StackOverflow -- How do I set proxy for Lynx?](https://stackoverflow.com/questions/32822161/how-do-i-set-proxy-for-lynx#32836626)

- [Unix StackExchange -- Lynx things all certificates are untrusted with my configuration file](https://unix.stackexchange.com/questions/364561/lynx-thinks-all-certificates-are-untrusted-with-my-configuration-file)

- [Tor StackExchange -- This is a socks proxy not an HTTP proxy](https://tor.stackexchange.com/questions/16554/this-is-a-socks-proxy-not-an-http-proxy)

- [Cloud Flare -- Introducing DNS Resolver for Tor](https://blog.cloudflare.com/welcome-hidden-resolver/)

- [CommandLineFu -- Join the content of a bash array with commas](https://www.commandlinefu.com/commands/view/12759/join-the-content-of-a-bash-array-with-commas)


___


## License
[heading__license]:
  #license
  "&#x2696; Legal side of Open Source"


```
Enables clear-net browsing over the Tor network via Lynx web browser
Copyright (C) 2020 S0AndS0

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU Affero General Public License as published
by the Free Software Foundation, version 3 of the License.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU Affero General Public License for more details.

You should have received a copy of the GNU Affero General Public License
along with this program.  If not, see <https://www.gnu.org/licenses/>.
```


For further details review full length version of [AGPL-3.0][branch__current__license] License.



[branch__current__license]:
  /LICENSE
  "&#x2696; Full length version of AGPL-3.0 License"


[badge__commits__torrific_lynx__main]:
  https://img.shields.io/github/last-commit/paranoid-linux/torrific-lynx/main.svg

[commits__torrific_lynx__main]:
  https://github.com/paranoid-linux/torrific-lynx/commits/main
  "&#x1F4DD; History of changes on this branch"


[torrific_lynx__community]:
  https://github.com/paranoid-linux/torrific-lynx/community
  "&#x1F331; Dedicated to functioning code"


[issues__torrific_lynx]:
  https://github.com/paranoid-linux/torrific-lynx/issues
  "&#x2622; Search for and _bump_ existing issues or open new issues for project maintainer to address."

[torrific_lynx__fork_it]:
  https://github.com/paranoid-linux/torrific-lynx/
  "&#x1F531; Fork it!"

[pull_requests__torrific_lynx]:
  https://github.com/paranoid-linux/torrific-lynx/pulls
  "&#x1F3D7; Pull Request friendly, though please check the Community guidelines"

[torrific_lynx__main__source_code]:
  https://github.com/paranoid-linux/torrific-lynx/
  "&#x2328; Project source!"

[badge__issues__torrific_lynx]:
  https://img.shields.io/github/issues/paranoid-linux/torrific-lynx.svg

[badge__pull_requests__torrific_lynx]:
  https://img.shields.io/github/issues-pr/paranoid-linux/torrific-lynx.svg

[badge__main__torrific_lynx__source_code]:
  https://img.shields.io/github/repo-size/paranoid-linux/torrific-lynx


[firejail__source]:
  https://github.com/netblue30/firejail
  "Source code repository for Firejail"
