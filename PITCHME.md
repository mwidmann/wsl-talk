# Post-Mac Web Development with @css[max](Windows 10 and WSL) <small>@VlbgWebDev, 2018/08/14</small>

---?image=assets/img/me.jpg&size=cover&position=center bottom

@snap[north bio]
@css[bio-name](Martin Widmann)
@css[bio-about](Señor Developer<br>@russmedia digital)
@css[bio-byline](@fa[twitter pad-fa] mwidmann)
@snapend

Note:
- been a Mac user for many years
  - started with a 12" Powerbook
  - updated to an Intel Macbook Pro as soon as they came out
  - been a Mac user since
  - last Mac was a 2015 retina iMac with i7 and 16GB of Ram
- switched completely to Windows in April 2018 after being an avid Surface User for the past couple of years
  - switch made possible thanks to WSL

---

## Web Development on Windows? srsly?
@ul[plain]
![Srsly](https://media.giphy.com/media/3o6fISHv9ZLyBA66qI/giphy.gif)
@ulend

Note:
- You don't hear so many good things about Windows in the past, but Microsoft has done plenty of good work in the past couple of years to make this better, even becoming the *top open source contributor on GitHub*

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
- BSD core for a very similar environment than on most servers @note[there can be very drastic differences though in the way the commands work]
- [homebrew](https://brew.sh)
@ulend

---

## Why Windows for Web Development?

@ul
- Much wider variety of devices to choose from @note[cheaper and with more features in many cases]
- pretty (and) stable operating system (ymmv)
- Good tools @note[We'll talk alternatives later...]
- Almost all tools are available for Windows as well
- [Chocolatey](https://chocolatey.org/)
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

## Features

@ul
- have access to almost all linux programs (by distribution)
- run windows and linux programs seamlessly @note[there's wslbridge for running linux commands in windows context, paths are converted automatically]
- install various linux distributions in parallel
- use ssh without using putty
- run cron jobs, install network services, do cool stuff
@ulend

---

## Things not so nice in WSL...

@ul
- The difference in paths still remains
- Need to install (and maintain) tools twice @note[windows IDEs rely on windows tools]
- I/O performance is worse @note[can be made better by excluding files/folders in Windows Defender]
- git on windows/wsl can make your life hell @note[need to force eol to lf and filemode to false]
- files in WSL filesystem can't be edited with Windows tools
@ulend

---

## Installation

@ul
- enable WSL feature in Windows 10
- choose distribution of choice in Windows Store @note[ubuntu 18.04, debian Strech, Suse Leap or Enterprise, Kali Linux]
- run installed distro to finish the installation
@ulend

---

## My Setup

@ul
- Server environment running in Docker for Windows
- Services composed through docker-compose
- A mix of Visual Studio Code and PhpStorm
  - with VIM extensions @note[driving me crazy sometimes]
- debian as the primary WSL distro, Ubuntu 18.04 alongside it
- zsh with prezto and pure theme @note[because of async git polling which makes it snappy even in large repositories]
- git mostly in Shell @note[but once the issues with line ends and filemodes, gui can be used as well]
@ulend

Note:
- mainly develop in php, javascript
- Webserver still Apache with mod_php for easier maintenance
- CLI tools installed in Docker accessing the windows installation through the API
- Trusted self signed certificates with minica for local PWA development

---

# Alternatives on Windows

---
@snap[north]
<h2>Terminal</h2>
@snapend

@snap[midpoint]
![cmder](assets/img/cmder.png)
<br>
[cmder](http://cmder.net)
<br>
<small>Alternative Hyper, [hyper.is](https://hyper.is)</small>
@snapend

Note:
- iTerm2
- Mac Terminal
---

@snap[north]
<h2>MySQL client</h2>
@snapend

@snap[midpoint]
![HeidiSQL](https://www.heidisql.com/images/screenshots/database.png)
<br>
[HeidiSQL](https://www.heidisql.com)
@snapend

Note:
- SequelPro
---
@snap[north]
<h2>Quick Look</h2>
@snapend

@snap[midpoint]
![quicklook](https://store-images.s-microsoft.com/image/apps.17552.14405803611253731.f98cdd0b-804a-4451-892c-8f66e59e65a4.4ecde082-1946-4f39-89d2-400bf4c8e0ea?w=1399&h=1035&q=60)
<br>
[Quicklook](https://www.microsoft.com/de-at/p/quicklook/9nv4bs3l1h4s#)
@snapend

Note:
- built in in macOS
---

@snap[north]
<h2>Productivity</h2>
@snapend

@snap[midpoint]
![Wox](http://www.wox.one/images/wox_preview.jpg)
<br>
[Wox](http://www.wox.one)
@snapend

Note:
- Alfred

---

@snap[north]
<h2>Graphics</h2>
@snapend

@snap[midpoint]
![Paint.net](https://www.getpaint.net/screenshots/pdn40_kirkland.jpg)
<br>
[Paint.net](https://www.getpaint.net/index.html)
<br>
<small>Alternatives [Figma](https://www.figma.com/) or [Gravit Designer](https://designer.io/)</small>

@snapend

---

# Questions?

---

![Thank you](https://media.giphy.com/media/xIJLgO6rizUJi/giphy.gif)
