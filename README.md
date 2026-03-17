<div align="center">
  
  <!-- Pure terminal, no ASCII art, just raw command output -->
  <pre style="color: #00ff88; font-family: 'Fira Code', 'Courier New', monospace; font-size: 13px; text-align: left; background: #000000; padding: 25px; border: 2px solid #33ff33; width: 85%; margin: 20px auto; box-shadow: 0 0 10px #00ff88;">
<span style="color: #ffff00;">$</span> <span style="color: #ffffff;">uname -a</span>
<span style="color: #00ff88;">OpenBSD ffdiracex.obsd 7.5 GENERIC#0 amd64</span>

<span style="color: #ffff00;">$</span> <span style="color: #ffffff;">id</span>
<span style="color: #00ff88;">uid=1000(ffdiracex) gid=1000(ffdiracex) groups=1000(ffdiracex),0(wheel),4(kmem),5(operator),20(staff)</span>

<span style="color: #ffff00;">$</span> <span style="color: #ffffff;">cat /etc/release</span>
<span style="color: #00ff88;">OpenBSD/amd64 7.5</span>

<span style="color: #ffff00;">$</span> <span style="color: #ffffff;">sysctl kern.version</span>
<span style="color: #00ff88;">kern.version=OpenBSD 7.5 (GENERIC) #0: Mon Mar 20 14:00:00 MDT 2024
    deraadt@amd64.openbsd.org:/usr/src/sys/arch/amd64/compile/GENERIC</span>

<span style="color: #ffff00;">$</span> <span style="color: #ffffff;">pkg_info -a | grep -E '^(python|gcc|rust)'</span>
<span style="color: #00ff88;">python-3.11.6         interpreted object-oriented programming language
gcc-11.4.0            GNU C compiler
rust-1.74.0           safe, concurrent, practical language</span>

<span style="color: #ffff00;">$</span> <span style="color: #ffffff;">which python3 g++ rustc doas vim tmux</span>
<span style="color: #00ff88;">/usr/local/bin/python3
/usr/local/bin/g++
/usr/local/bin/rustc
/usr/bin/doas
/usr/local/bin/vim
/usr/local/bin/tmux</span>

<span style="color: #ffff00;">$</span> <span style="color: #ffffff;">readlink -f /usr/local/bin/python3</span>
<span style="color: #00ff88;">/usr/local/bin/python3.11</span>

<span style="color: #ffff00;">$</span> <span style="color: #ffffff;">file /usr/local/bin/python3.11</span>
<span style="color: #00ff88;">/usr/local/bin/python3.11: ELF 64-bit LSB executable, x86-64, version 1 - OpenBSD</span>

<span style="color: #ffff00;">$</span> <span style="color: #ffffff;">ls -la /usr/local/bin | grep -E '(python|g\+\+|rustc|gcc)' | head -5</span>
<span style="color: #00ff88;">lrwxr-xr-x  1 root  bin      21 Mar 20 14:00 python@ -> /usr/local/bin/python3
-rwxr-xr-x  1 root  bin  12.2M Mar 20 14:00 python3.11*
lrwxr-xr-x  1 root  bin      16 Mar 20 14:00 python3@ -> python3.11
-rwxr-xr-x  1 root  bin  89.3M Mar 20 14:00 g++*
-rwxr-xr-x  1 root  bin  78.2M Mar 20 14:00 gcc*</span>

<span style="color: #ffff00;">$</span> <span style="color: #ffffff;">cat ~/.profile</span>
<span style="color: #00ff88;">#!/bin/sh
#
# ffdiracex's OpenBSD .profile
#
export PATH=/home/ffdiracex/bin:/usr/local/bin:/usr/bin:/bin:/usr/sbin:/sbin
export EDITOR=vim
export VISUAL=vim
export TERM=xterm-256color
export PKG_PATH=https://cdn.openbsd.org/pub/OpenBSD/7.5/packages/amd64/
export CVSROOT=anoncvs@anoncvs.eu.openbsd.org:/cvs

alias ls='ls -G'
alias ll='ls -l'
alias la='ls -a'
alias cvs='cvs -z3'
alias doas='doas'
alias vi='vim'</span>

<span style="color: #ffff00;">$</span> <span style="color: #ffffff;">cat ~/.cshrc</span>
<span style="color: #00ff88;"># $OpenBSD: dot.cshrc,v 1.7 2023/01/15 12:00:00 deraadt Exp $
#
# ffdiracex's cshrc
#
set path = (/home/ffdiracex/bin /usr/local/bin /usr/bin /bin /usr/sbin /sbin)
setenv EDITOR vim
setenv TERM xterm-256color
setenv PKG_PATH https://cdn.openbsd.org/pub/OpenBSD/7.5/packages/amd64/
setenv CVSROOT anoncvs@anoncvs.eu.openbsd.org:/cvs

alias ls ls -G
alias ll ls -l
alias la ls -a
alias h history 25
alias j jobs</span>

<span style="color: #ffff00;">$</span> <span style="color: #ffffff;">cvs -d anoncvs@anoncvs.eu.openbsd.org:/cvs co -P src/usr.bin/vi</span>
<span style="color: #00ff88;">cvs checkout: Updating src/usr.bin/vi
U src/usr.bin/vi/Makefile
U src/usr.bin/vi/README
U src/usr.bin/vi/ex.c
... (output truncated)</span>

<span style="color: #ffff00;">$</span> <span style="color: #ffffff;">doas pkg_add rust python g++</span>
<span style="color: #00ff88;">quirks-6.114 signed on 2024-03-20T14:00:00Z
rust-1.74.0: ok
python-3.11.6: ok
gcc-11.4.0: ok</span>

<span style="color: #ffff00;">$</span> <span style="color: #ffffff;">cat ~/.xsession</span>
<span style="color: #00ff88;">#!/bin/sh
#
# ~/.xsession
#
exec cwm</span>

<span style="color: #ffff00;">$</span> <span style="color: #ffffff;">cat ~/.cwmrc</span>
<span style="color: #00ff88;"># cwm configuration
#
command -t terminal xterm
command -t browser firefox
command -t mail thunderbird

bind-key CM-Restart exec cwm

color activeborder "#8F33DF"
color inactiveborder "#333333"
color menubg "#000000"
color menufg "#00ff88"
color font "#ffffff"</span>

<span style="color: #ffff00;">$</span> <span style="color: #ffffff;">df -h /home /usr /var</span>
<span style="color: #00ff88;">Filesystem     Size    Used   Avail Capacity  Mounted on
/dev/sd0a       99M    6.4M     88M     7%    /
/dev/sd0d      7.9G    3.1G    4.5G    41%    /usr
/dev/sd0e      3.9G    344M    3.4G     9%    /var
/dev/sd0f      9.9G    8.7G    757M    92%    /home</span>

<span style="color: #ffff00;">$</span> <span style="color: #ffffff;">vmstat</span>
<span style="color: #00ff88;"> procs    memory       page                    disks    traps          cpu
 r b w    avm    fre  flt  re  pi  po  fr  sr wd0  intr   syscl  usr  idl
 2 0 0  34124  16274   21   0   0   0  15   5   0    103    2895    3   97</span>

<span style="color: #ffff00;">$</span> <span style="color: #ffffff;">systat vmstat 1 3</span>
<span style="color: #00ff88;">   1 users Load 0.14 0.07 0.03                    ffdiracex@obsd: Wed Mar 20 14:00:00

CPU: |     3.6% |    0.0% |    0.0% |   96.4% 
      user      nice      sys     idle
...
</span>
<span style="color: #ffff00;">$</span> <span style="color: #ffffff;">netstat -rn | grep default</span>
<span style="color: #00ff88;">default            10.0.1.1           UGS       0    12942   em0</span>

<span style="color: #ffff00;">$</span> <span style="color: #ffffff;">ifconfig em0 | grep inet</span>
<span style="color: #00ff88;">        inet 10.0.1.42 netmask 0xffffff00 broadcast 10.0.1.255
        inet6 fe80::1a2b:3c4d:5e6f:7a8b%em0 prefixlen 64 scopeid 0x1</span>

<span style="color: #ffff00;">$</span> <span style="color: #ffffff;">tail -20 /var/log/messages | grep -i error</span>
<span style="color: #00ff88;">Mar 20 13:47:22 obsd /bsd: uvfs: nothing to see here
Mar 20 14:00:00 obsd syslogd: restart</span>

<span style="color: #ffff00;">$</span> <span style="color: #ffffff;">history 10</span>
<span style="color: #00ff88;">  421  cvs up -Pd src
  422  doas pkg_add firefox
  423  vi ~/.cwmrc
  424  xinit
  425  pkg_info -Q rust
  426  doas pkg_add rust
  427  rustc --version
  428  git clone https://github.com/ffdiracex/dotfiles
  429  cd dotfiles && ./install.sh
  430  echo "OpenBSD - secure by default, insane by choice"</span>

<span style="color: #ffff00;">$</span> <span style="color: #ffffff;">cal</span>
<span style="color: #00ff88;">     March 2024
Su Mo Tu We Th Fr Sa
                1  2
 3  4  5  6  7  8  9
10 11 12 13 14 15 16
17 18 19 20 21 22 23
24 25 26 27 28 29 30
31</span>

<span style="color: #ffff00;">$</span> <span style="color: #ffffff;">date</span>
<span style="color: #00ff88;">Wed Mar 20 14:00:00 MDT 2024</span>

<span style="color: #ffff00;">$</span> <span style="color: #ffffff;">uptime</span>
<span style="color: #00ff88;"> 2:00PM  up 42 days,  6:42, 1 user, load averages: 0.07, 0.03, 0.01</span>

<span style="color: #ffff00;">$</span> <span style="color: #ffffff;">echo $SHELL</span>
<span style="color: #00ff88;">/bin/ksh</span>

<span style="color: #ffff00;">$</span> <span style="color: #ffffff;">echo "I use OpenBSD btw (and I still have no bitches)"</span>
<span style="color: #00ff88;">I use OpenBSD btw (and I still have no bitches)</span>

<span style="color: #ffff00;">$</span> <span style="color: #ffffff;">exit</span>
<span style="color: #00ff88;">logout</span>

<span style="color: #ffff00;">$</span> <span style="color: #ffffff;">_</span>
  </pre>

  <!-- GitHub stats as raw numbers, no graphs -->
  <pre style="color: #00ff88; font-family: 'Fira Code', 'Courier New', monospace; font-size: 13px; text-align: left; background: #000000; padding: 15px; border: 1px solid #33ff33; width: 60%; margin: 10px auto;">

<span style="color: #ffff00;">ffdiracex@obsd:~$</span> <span style="color: #ffffff;">cat /home/ffdiracex/.github/stats</span>
<span style="color: #00ff88;">────────────────────────────────────────────────
GITHUB STATISTICS - Last updated: 2024-03-20
────────────────────────────────────────────────
Public Repos:     28
Private Repos:    6
Total Commits:    2,718
Pull Requests:    143
Issues Created:   67
Issues Closed:    58
Stars Received:   42
Followers:        69
Following:        13
────────────────────────────────────────────────
LANGUAGES (bytes):
  C++:       1,234,567
  Python:    987,654
  Rust:      456,789
  Shell:     123,456
  C:          98,765
────────────────────────────────────────────────</span>

<span style="color: #ffff00;">ffdiracex@obsd:~$</span> <span style="color: #ffffff;">tail -5 /home/ffdiracex/.github/activity.log</span>
<span style="color: #00ff88;">2024-03-19T23:42:13  commit: fix null pointer dereference in abyss-wm
2024-03-19T23:58:47  push: origin HEAD -> main (3 commits)
2024-03-20T01:15:22  issue: opened #42 "memory leak in event loop"
2024-03-20T04:32:01  pr: merged #69 "add pledge() and unveil() sandboxing"
2024-03-20T13:47:55  star: starred openbsd/src</span>

<span style="color: #ffff00;">ffdiracex@obsd:~$</span> <span style="color: #ffffff;">_</span>
  </pre>

  <!-- Footer with just a blinking cursor -->
  <pre style="color: #00ff88; font-family: 'Fira Code', 'Courier New', monospace; font-size: 13px; text-align: left; background: #000000; padding: 10px; border: none; width: 85%; margin: 20px auto;">
<span style="color: #ffff00;">ffdiracex@obsd:~$</span> <span style="color: #ffffff;">echo 'EOF'</span>
<span style="color: #00ff88;">EOF</span>

<span style="color: #ffff00;">ffdiracex@obsd:~$</span> <span style="color: #ffffff;">_</span>
  </pre>
</div>
