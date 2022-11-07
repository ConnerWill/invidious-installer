<div align="center">
  
[![invidious-installer Image](https://raw.githubusercontent.com/tmiland/invidious-installer/main/_images/invidious_installer.png)](https://github.com/tmiland/invidious-installer/blob/main/_images/invidious_installer.png)

# Invidious-Installer
> *Automatic install script for [Invidious](https://github.com/iv-org/invidious)*
  
  
[![ShellCheck Workflow Status][github-workflow-shellcheck-badge]][github-workflow-shellcheck]
[![License][license]][license-file]
[![GitHub top language][github-top-language]][{{repo_name}}]
[![GitHub language count][github-language-count]][{{repo_name}}]
[![GitHub last commit][github-last-commit]][{{repo_name}}]
[![GitHub issues][github-issues]][{{repo_name}}]
[![GitHub repo size][github-repo-size]][{{repo_name}}]
[![GitHub Repo stars][github-repo-stars]][{{repo_name}}]
[![GitLab][gitlab-badge]][gitlab]
  
  
  
[![GitHub release](https://img.shields.io/github/release/tmiland/invidious-installer.svg?style=for-the-badge)](https://github.com/tmiland/invidious-installer/releases)
[![licence](https://img.shields.io/github/license/tmiland/invidious-installer.svg?style=for-the-badge)](https://github.com/tmiland/invidious-installer/blob/master/LICENSE)
![Bash](https://img.shields.io/badge/Language-SH-4EAA25.svg?style=for-the-badge)

</div>

---


# Overview

This script is just the install option in [Invidious-Updater](https://github.com/ConnerWill/Invidious-Updater)
: Version 2.0.0 is completely re-written and might be sourced in the future

# Installation

## Quick Installation

Install with default options to be used on localhost

```shell
curl -sSL "https://raw.githubusercontent.com/ConnerWill/invidious-installer/main/invidious_installer.sh" | bash || exit 0
```

<details>
  <summary>Download with wget and pipe to bash</summary>

```shell
wget -qO - "https://raw.githubusercontent.com/ConnerWill/invidious-installer/main/invidious_installer.sh" | bash || exit 0
```
  
</details>

## Customized Installation

```shell
curl -sSL "https://raw.githubusercontent.com/ConnerWill/invidious-installer/main/invidious_installer.sh"
chmod +x invidious_installer.sh
```

### Install with default options to run on localhost:

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

| Debian | Ubuntu | CentOS | Fedora | Arch | PureOS |
| ------ | ------ | ------ | ------ | ------ | ------ |
| [<img src="https://raw.githubusercontent.com/tmiland/Invidious-Updater/master/img/os_icons/debian.svg?sanitize=true" height="128" width="128">](https://raw.githubusercontent.com/tmiland/Invidious-Updater/master/img/os_icons/debian.svg?sanitize=true) | [<img src="https://raw.githubusercontent.com/tmiland/Invidious-Updater/master/img/os_icons/ubuntu.svg?sanitize=true" height="128" width="128">](https://raw.githubusercontent.com/tmiland/Invidious-Updater/master/img/os_icons/ubuntu.svg?sanitize=true) | [<img src="https://raw.githubusercontent.com/tmiland/Invidious-Updater/master/img/os_icons/cent-os.svg?sanitize=true" height="128" width="128">](https://raw.githubusercontent.com/tmiland/Invidious-Updater/master/img/os_icons/cent-os.svg?sanitize=true) | [<img src="https://raw.githubusercontent.com/tmiland/Invidious-Updater/master/img/os_icons/fedora.svg?sanitize=true" height="128" width="128">](https://raw.githubusercontent.com/tmiland/Invidious-Updater/master/img/os_icons/fedora.svg?sanitize=true) | [<img src="https://raw.githubusercontent.com/tmiland/Invidious-Updater/master/img/os_icons/arch.svg?sanitize=true" height="128" width="128">](https://raw.githubusercontent.com/tmiland/Invidious-Updater/master/img/os_icons/arch.svg?sanitize=true) | [<img src="https://raw.githubusercontent.com/tmiland/Invidious-Updater/master/img/os_icons/pureos.svg?sanitize=true" height="128" width="128">](https://raw.githubusercontent.com/tmiland/Invidious-Updater/master/img/os_icons/pureos.svg?sanitize=true)

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

## Web Hosting

Sign up for web hosting using this link, and receive $100 in credit over 60 days.

[DigitalOcean](https://m.do.co/c/f1f2b475fca0)

#### Disclaimer 

*** ***Use at own risk*** ***

### License

[![MIT License Image](https://upload.wikimedia.org/wikipedia/commons/thumb/0/0c/MIT_logo.svg/220px-MIT_logo.svg.png)](https://github.com/tmiland/invidious-installer/blob/master/LICENSE)

[MIT License](https://github.com/tmiland/invidious-installer/blob/master/LICENSE)


<div align="center">

```
╔════════════════════════════════════════════╗
║              Invidious Installer.sh               ║
║       Automatic install script for Invidious      ║
║              Maintained by @tmiland               ║
╚════════════════════════════════════════════╝
```

</div>

<!-- === URL Resources === -->
<!-- {{repo_name}} GitHub Repository URL -->
[{{repo_name}}]: https://github.com/ConnerWill/{{repo_name}}
<!-- BADGES -->
 <!-- GitHub Badges -->
  <!-- LICENSE Badge -->
[license]: https://img.shields.io/github/license/ConnerWill/{{repo_name}}
[license-file]: https://github/ConnerWill/{{repo_name}}/blob/main/docs/LICENSE
  <!-- GitHub Workflow Badges -->
  <!-- GitHub Workflow ShellCheck Status Badges -->
[github-workflow-shellcheck-badge]: https://img.shields.io/github/workflow/status/ConnerWill/{{repo_name}}/ShellCheck
[github-workflow-shellcheck]: https://github.com/ConnerWill/{{repo_name}}/actions
  <!-- GitHub Workflow <ENTER_WORKFLOW_NAME> Status Badges -->
[github-workflow-badge]: https://img.shields.io/github/workflow/status/ConnerWill/{{repo_name}}/<ENTER_WORKFLOW_NAME>
[github-workflow]: https://github.com/ConnerWill/{{repo_name}}/actions
  <!-- GitHub Languages Badges -->
[github-top-language]: https://img.shields.io/github/languages/top/ConnerWill/{{repo_name}}
[github-language-count]: https://img.shields.io/github/languages/count/ConnerWill/{{repo_name}}
  <!-- GitHub Languages Badges -->
[github-last-commit]: https://img.shields.io/github/last-commit/ConnerWill/{{repo_name}}
[github-issues]: https://img.shields.io/github/issues-raw/ConnerWill/{{repo_name}}
[github-repo-size]: https://img.shields.io/github/repo-size/ConnerWill/{{repo_name}}
  <!-- GitHub Stars Badges -->
[github-repo-stars]: https://img.shields.io/github/stars/ConnerWill/{{repo_name}}?style=social
  <!-- GitLab Badge -->
[gitlab]: https://gitlab.com/ConnerWill/{{repo_name}}
[gitlab-badge]: https://img.shields.io/static/v1?label=gitlab&logo=gitlab&color=E24329&message=mirrored
 <!-- Travis CI Badges -->
[travis-badge]: https://app.travis-ci.com/ConnerWill/{{repo_name}}.svg?branch=master
[travis]: https://app.travis-ci.com/ConnerWill/{{repo_name}}/
 <!-- Go Badges -->
  <!-- GoDoc Badges -->
[godoc-badge]: https://godoc.org/github.com/connerwill/{{repo_name}}?status.svg
[godoc]: https://godoc.org/github.com/connerwill/{{repo_name}}
  <!-- Go Report Card Badges -->
[report-badge]: https://goreportcard.com/badge/github.com/connerwill/{{repo_name}}
[report]: https://goreportcard.com/report/github.com/connerwill/{{repo_name}}
 <!-- Docker Badges -->
  <!-- Docker Image Badges -->
[docker-pulls]: https://img.shields.io/docker/pulls/rl9uu6smkj/{{repo_name}}
[docker-size]: https://img.shields.io/docker/image-size/rl9uu6smkj/{{repo_name}}
  <!-- DockerHub Badges -->
[docker-hub]: https://hub.docker.com/r/rl9uu6smkj/{{repo_name}}
[docker-cloud-build-status]: https://img.shields.io/docker/cloud/build/rl9uu6smkj/{{repo_name}}

