# Post-Mac Web Development with @css[max](Windows 10 and WSL) <small>@VlbgWebDev, 2018/08/14</small>

---?image=assets/img/me.jpg&size=cover&position=center bottom

@snap[north bio]
@css[bio-name](Martin Widmann)
@css[bio-about](Señor Developer<br>@russmedia digital)
@css[bio-byline](@fa[twitter pad-fa] mwidmann)
@snapend

---

## Web Devlopment on Windows? srsly?
![Srsly](assets/img/srsly.gif)
---

## But...

---?image=assets/img/google.gif&size=cover&position=center center

---

## Why macOS for Web Development?

@ul
- Nice to look at hardware making one feel special
  - 10 years age
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

# Installation

- enable WSL feature in Windows 10
![enable feature](assets/img/enable-wsl.png)

---

# Installation

- enable WSL feature in Windows 10
- choose distribution of choice in Windows Store<br>
![Ubuntu](assets/img/ubuntu.png)(.wsl-dist)
![Debian](assets/img/debian.png)(.wsl-dist)
![Suse Leap](assets/img/suse-leap.png)(.wsl-dist)
![Suse Enterprise](assets/img/suse-enterprise.png)(.wsl-dist)
![Kali Linux](assets/img/kali.png)(.wsl-dist)
