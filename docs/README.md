<div align="center">

[![invidious-installer Image](https://raw.githubusercontent.com/ConnerWill/invidious-installer/main/_images/invidious_installer.png)](https://github.com/ConnerWill/invidious-installer/blob/main/_images/invidious_installer.png)

# Invidious-Installer
> *Automatic install script for [Invidious](https://github.com/iv-org/invidious)*

<!--[![ShellCheck Workflow Status][github-workflow-shellcheck-badge]][github-workflow-shellcheck]-->
[![License][license]][license-file]
[![GitHub top language][github-top-language]][invidious-installer]
[![GitHub language count][github-language-count]][invidious-installer]
[![GitHub last commit][github-last-commit]][invidious-installer]
[![GitHub issues][github-issues]][invidious-installer]
[![GitHub repo size][github-repo-size]][invidious-installer]
[![GitHub Repo stars][github-repo-stars]][invidious-installer]
[![GitLab][gitlab-badge]][gitlab]

</div>

---

# Overview

This script is a new and improved version of the Invidious installer option in [Invidious-Updater](https://github.com/ConnerWill/Invidious-Updater)

Version 2.0.0 is completely re-written and might be sourced in the future

# Installation

## Quick Installation

> Download with curl and run the installation script with a default configuration which runs on **localhost:3000** *(http://127.0.0.1:3000)*

```shell
curl -sSL "https://raw.githubusercontent.com/ConnerWill/invidious-installer/main/invidious_installer.sh" | bash || exit 0
```

<details>
  <summary>Download with wget and pipe to bash</summary>

  
> Download with wget and run the installation script with a default  install with a default configuration which runs on **localhost:3000** *(http://127.0.0.1:3000)*
  
```shell
wget -qO - "https://raw.githubusercontent.com/ConnerWill/invidious-installer/main/invidious_installer.sh" | bash || exit 0
```

</details>

## Customized Installation

```shell
curl -sSL "https://raw.githubusercontent.com/ConnerWill/invidious-installer/main/invidious_installer.sh"
chmod +x invidious_installer.sh
```

> Install with default options to run on localhost:

```console
DOMAIN= \
IP=localhost \
PORT=3000 \
PSQLDB=invidious \
HTTPS_ONLY=n \
EXTERNAL_PORT= \
ADMINS= \
SWAP_OPTIONS=n \
./invidious_installer.sh
```

### Install with options to run on HTTPS site:

```console
DOMAIN=domain.com \
IP=123.45.67.89 \
PORT=3000 \
PSQLDB=invidious \
HTTPS_ONLY=y \
EXTERNAL_PORT=443 \
ADMINS=admin \
SWAP_OPTIONS=n \
./invidious_installer.sh
```

- For Captcha key, add `CAPTCHA_KEY=YOUR_CAPTCHA_KEY \` to options.
- PostgreSQL password will be auto-generated.
- For verbose output, use [ -v ] argument
- Use a custom invidious repo/fork with [ -r | --repo user/invidious ]
- installation log in invidious_installer.log
- [slib.sh](/src/slib.sh) function script is sourced remotely if not found locally
  - This script is a combination of functions for spinners, colors and logging
    - Source: Spinner: [swelljoe/spinner](https://github.com/swelljoe/spinner)
    - Source: Run ok: [swelljoe/run_ok](https://github.com/swelljoe/run_ok)
    - Source: Slog: [swelljoe/slog](https://github.com/swelljoe/slog)
    - Source: Slib: [virtualmin/slib](https://github.com/virtualmin/slib)

***Note: you will be prompted to enter root password***

If root password is not set, type:

```shell
sudo passwd root
```

### To keep Invidious up-to-date: [Invidious-Updater](https://github.com/ConnerWill/Invidious-Updater)

## Testing

Tested and working on:

<div align="center">
  
| Debian | Ubuntu | CentOS | Fedora | Arch | PureOS |
| ------ | ------ | ------ | ------ | ------ | ------ |
| [<img src="https://raw.githubusercontent.com/tmiland/Invidious-Updater/master/img/os_icons/debian.svg?sanitize=true" height="128" width="128">](https://raw.githubusercontent.com/tmiland/Invidious-Updater/master/img/os_icons/debian.svg?sanitize=true) | [<img src="https://raw.githubusercontent.com/tmiland/Invidious-Updater/master/img/os_icons/ubuntu.svg?sanitize=true" height="128" width="128">](https://raw.githubusercontent.com/tmiland/Invidious-Updater/master/img/os_icons/ubuntu.svg?sanitize=true) | [<img src="https://raw.githubusercontent.com/tmiland/Invidious-Updater/master/img/os_icons/cent-os.svg?sanitize=true" height="128" width="128">](https://raw.githubusercontent.com/tmiland/Invidious-Updater/master/img/os_icons/cent-os.svg?sanitize=true) | [<img src="https://raw.githubusercontent.com/tmiland/Invidious-Updater/master/img/os_icons/fedora.svg?sanitize=true" height="128" width="128">](https://raw.githubusercontent.com/tmiland/Invidious-Updater/master/img/os_icons/fedora.svg?sanitize=true) | [<img src="https://raw.githubusercontent.com/tmiland/Invidious-Updater/master/img/os_icons/arch.svg?sanitize=true" height="128" width="128">](https://raw.githubusercontent.com/tmiland/Invidious-Updater/master/img/os_icons/arch.svg?sanitize=true) | [<img src="https://raw.githubusercontent.com/tmiland/Invidious-Updater/master/img/os_icons/pureos.svg?sanitize=true" height="128" width="128">](https://raw.githubusercontent.com/tmiland/Invidious-Updater/master/img/os_icons/pureos.svg?sanitize=true)

</div>

## Compatibility and Requirements

* Debian 8 and later
* Ubuntu 16.04 and later
* PureOS (Not tested)
* CentOS 8
* Fedora 33
* Arch Linux

## Feature request and bug reports
- [Bug report](https://github.com/tmiland/Invidious-Updater/issues/new?assignees=tmiland&labels=bug&template=bug_report.md&title=Bug-report:)
- [Feature request](https://github.com/tmiland/Invidious-Updater/issues/new?assignees=tmiland&labels=enhancement&template=feature_request.md&title=Feature-request:)

## Donations
<a href="https://www.buymeacoffee.com/tmiland" target="_blank"><img src="https://cdn.buymeacoffee.com/buttons/v2/default-yellow.png" alt="Buy Me A Coffee" style="height: 60px !important;width: 217px !important;" ></a>
- [PayPal me](https://paypal.me/milanddata)
- [BTC] : 33mjmoPxqfXnWNsvy8gvMZrrcG3gEa3YDM

#### Disclaimer

*** ***Use at own risk*** ***

### License

[![MIT License Image](https://upload.wikimedia.org/wikipedia/commons/thumb/0/0c/MIT_logo.svg/220px-MIT_logo.svg.png)](https://github.com/ConnerWill/invidious-installer/blob/master/LICENSE)

[MIT License](https://github.com/ConnerWill/invidious-installer/blob/master/LICENSE)


<div align="center">

```
╔════════════════════════════════════════════╗
║              Invidious Installer.sh               ║
║       Automatic install script for Invidious      ║
║              Maintained by @t@@@@miland               ║
╚════════════════════════════════════════════╝
```

</div>

<!-- === URL Resources === -->
[invidious-installer]: https://github.com/ConnerWill/invidious-installer
[license]: https://img.shields.io/github/license/ConnerWill/invidious-installer
[license-file]: https://github/ConnerWill/invidious-installer/blob/main/docs/LICENSE
[github-workflow-shellcheck-badge]: https://img.shields.io/github/workflow/status/ConnerWill/invidious-installer/ShellCheck
[github-workflow-shellcheck]: https://github.com/ConnerWill/invidious-installer/actions
[github-workflow-badge]: https://img.shields.io/github/workflow/status/ConnerWill/invidious-installer/<ENTER_WORKFLOW_NAME>
[github-workflow]: https://github.com/ConnerWill/invidious-installer/actions
[github-top-language]: https://img.shields.io/github/languages/top/ConnerWill/invidious-installer
[github-language-count]: https://img.shields.io/github/languages/count/ConnerWill/invidious-installer
[github-last-commit]: https://img.shields.io/github/last-commit/ConnerWill/invidious-installer
[github-issues]: https://img.shields.io/github/issues-raw/ConnerWill/invidious-installer
[github-repo-size]: https://img.shields.io/github/repo-size/ConnerWill/invidious-installer
[github-repo-stars]: https://img.shields.io/github/stars/ConnerWill/invidious-installer?style=social
[gitlab]: https://gitlab.com/ConnerWill/invidious-installer
[gitlab-badge]: https://img.shields.io/static/v1?label=gitlab&logo=gitlab&color=E24329&message=mirrored
[travis-badge]: https://app.travis-ci.com/ConnerWill/invidious-installer.svg?branch=master
[travis]: https://app.travis-ci.com/ConnerWill/invidious-installer/
[godoc-badge]: https://godoc.org/github.com/connerwill/invidious-installer?status.svg
[godoc]: https://godoc.org/github.com/connerwill/invidious-installer
[report-badge]: https://goreportcard.com/badge/github.com/connerwill/invidious-installer
[report]: https://goreportcard.com/report/github.com/connerwill/invidious-installer
[docker-pulls]: https://img.shields.io/docker/pulls/rl9uu6smkj/invidious-installer
[docker-size]: https://img.shields.io/docker/image-size/rl9uu6smkj/invidious-installer
[docker-hub]: https://hub.docker.com/r/rl9uu6smkj/invidious-installer
[docker-cloud-build-status]: https://img.shields.io/docker/cloud/build/rl9uu6smkj/invidious-installer

