# Post-Mac Web Development with @css[max](Windows 10 and WSL) <small>@VlbgWebDev, 2018/08/14</small>

---?image=assets/img/me.jpg&size=cover&position=center bottom

@snap[north bio]
@css[bio-name](Martin Widmann)
@css[bio-about](Señor Developer<br>@russmedia digital)
@css[bio-byline](@fa[twitter pad-fa] mwidmann)
@snapend

---

## Web Devlopment on Windows? srsly?
@ul[plain]
![Srsly](assets/img/srsly.gif)
@ulend
---

## But...

---?image=assets/img/google.gif&size=cover&position=center center

---

## Why macOS for Web Development?

@ul
- Nice to look at hardware making one feel special
  - 10 years ago
- pretty (and) stable operating system
- Good/mostly consistent design language
- Good tools
- BSD core for a very similar environment than on the servers running Linux
  - which sometime is pretty different
- homebrew
@ulend

---
## Differences macOS/Windows

@ul
- Command diffences: `Cmd` vs. `Crtl`
- Path separator: `/` vs. `\`
- Line endings: `lf` vs. `crlf`
- Tools:
  - `ls` vs. `dir`
  - `rm` vs. `del`
  - `cp` vs. `(x)copy`
  - ...
- and then...
@ulend

---
@snap[west]
![courtesy Falkor on github](https://raw.githubusercontent.com/Falkor/dotfiles/master/screenshots/screenshot_falkor_iterm.png)
@snapend

@snap[east small]
![cmd](assets/img/cmd.exe.png)
@snapend
---
@snap[west small]
![courtesy Falkor on github](https://raw.githubusercontent.com/Falkor/dotfiles/master/screenshots/screenshot_falkor_iterm.png)
@snapend

@snap[east]
![cmd](assets/img/cmd.exe.png)
@snapend
---

# @css[max](Enter WSL)
(Windows Subsystem for Linux)

---

# Features

@ul
- have access to almost all linux programs (by distribution)
- run windows and linux programs seamlessly @note[there's wslbridge for running linux commands in windows context, paths are converted automatically]
- install various linux distributions in parallel
- use ssh without using putty
- run cron jobs, install network services, do cool stuff
@ulend

---

# Things not so nice in WSL...

@ul
- The difference in paths still remains
- Need to install (and maintain) tools twice @note[windows IDEs rely on windows tools]
- I/O performance is worse @note[can be made better by excluding files/folders in Windows Defender]
- git on windows/wsl can make your life hell @note[need to force eol to lf and filemode to false]
- files in WSL filesystem can't be edited with Windows tools
@ulend

---

# Installation

@ul
- enable WSL feature in Windows 10
- choose distribution of choice in Windows Store @note[ubuntu 18.04, debian Strech, Suse Leap or Enterprise, Kali Linux]
- run installed distro to finish the installation
@ulend

---

# My Setup

@ul
- Server environment running in Docker, services composed through docker-compose @note[running on windows, with the docker client installed in WSL using the api]
- A mix of Visual Studio Code and PhpStorm (just started using it)
- zsh with prezto and pure theme @note[because of async git polling which makes it snappy even in large repositories]
- Git mostly in Shell @note[but once the issues with line ends and filemodes, gui can be used as well]
@ulend

Note:
- mainly develop in php, javascript
- Webserver still Apache with mod_php for easier maintenance
- Trusted self signed certificates with minica for local PWA development

---

# Alternative Programs on Windows

---
## Get a Terminal

![cmder](assets/img/cmder.png)

[cmder](http://cmder.net)<br>
<small>Alternative Hyper, [hyper.is](https://hyper.is)</small>
---

## Install zsh and prezto
