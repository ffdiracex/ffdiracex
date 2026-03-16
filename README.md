<div align="center">
  
  <!-- Terminal header -->
  <pre style="color: #00ff88; font-family: 'Fira Code', monospace; font-size: 14px; text-align: left; background: #0a0c0f; padding: 20px; border-radius: 8px; border: 1px solid #444; width: 80%; margin: 20px auto;">
<span style="color: #8F33DF;">ffdiracex@abyss:~$</span> neofetch --stdout
<span style="color: #00ff88;">            .-:::::-.            ffdiracex@abyss
          .-:::::::::-.          OS: Arch Linux x86_64
         .-:::::::::::-.         Host: Custom Built
        .::::::::::::::.         Kernel: 6.6.1-arch1-1
        ::::::::::::::::         Uptime: I don't reboot
       ::::::::::::::::::        Shell: Nietzsche 5.9
      :::::::::::::::::::.       Terminal: /dev/chaos
     .::::::::::::::::::::.      CPU: Will to Power (∞ cores)
     ::::::::::::::::::::::      GPU: Abyss GTX 4090
     ::::::::::::::::::::::      Memory: 16384MiB / what doesn't kill me
     ::::::::::::::::::::::      
      :::::::::::::::::::.      
       ::::::::::::::::::       
        ::::::::::::::::        
         ::::::::::::::         
          .::::::::::.          
            .-:::::-.</span>

<span style="color: #8F33DF;">ffdiracex@abyss:~$</span> ls -la /usr/bin/
<span style="color: #ffffff;">total 42
lrwxrwxrwx   1 root root       21 Jan 01  1970 <span style="color: #00ff88;">python</span> -> /usr/bin/python3
-rwxr-xr-x   1 root root  16242432 Jan 01  1970 <span style="color: #00ff88;">python3</span>
lrwxrwxrwx   1 root root       24 Jan 01  1970 <span style="color: #00ff88;">g++</span> -> /usr/bin/g++-13
-rwxr-xr-x   1 root root 112748032 Jan 01  1970 <span style="color: #00ff88;">g++-13</span>
lrwxrwxrwx   1 root root       22 Jan 01  1970 <span style="color: #00ff88;">rustc</span> -> /usr/bin/rustc-1.73
-rwxr-xr-x   1 root root  82657280 Jan 01  1970 <span style="color: #00ff88;">rustc-1.73</span>
lrwxrwxrwx   1 root root       23 Jan 01  1970 <span style="color: #00ff88;">gcc</span> -> /usr/bin/gcc-13
-rwxr-xr-x   1 root root  98713600 Jan 01  1970 <span style="color: #00ff88;">gcc-13</span>
-rwxr-xr-x   1 root root   4210688 Jan 01  1970 <span style="color: #00ff88;">git</span>
-rwxr-xr-x   1 root root   2842624 Jan 01  1970 <span style="color: #00ff88;">vim</span>
-rwxr-xr-x   1 root root   1966080 Jan 01  1970 <span style="color: #00ff88;">tmux</span>
-rwxr-xr-x   1 root root    991232 Jan 01  1970 <span style="color: #00ff88;">htop</span></span>

<span style="color: #8F33DF;">ffdiracex@abyss:~$</span> cat ~/.bashrc | grep PATH
<span style="color: #00ff88;">export PATH=$PATH:/usr/local/bin:/usr/bin:/bin:/usr/local/sbin:/usr/sbin:/sbin
export PATH=$PATH:~/.local/bin
export PATH=$PATH:~/.cargo/bin</span>

<span style="color: #8F33DF;">ffdiracex@abyss:~$</span> which python3 rustc g++ git
<span style="color: #00ff88;">/usr/bin/python3
/usr/bin/rustc
/usr/bin/g++
/usr/bin/git</span>

<span style="color: #8F33DF;">ffdiracex@abyss:~$</span> readlink -f /usr/bin/python3
<span style="color: #00ff88;">/usr/bin/python3.12</span>

<span style="color: #8F33DF;">ffdiracex@abyss:~$</span> file /usr/bin/python3
<span style="color: #00ff88;">/usr/bin/python3: ELF 64-bit LSB executable, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, for GNU/Linux 5.4.0, stripped</span>

<span style="color: #8F33DF;">ffdiracex@abyss:~$</span> ldd /usr/bin/python3
<span style="color: #00ff88;">        linux-vdso.so.1 (0x00007ffe3b9f7000)
        libc.so.6 => /usr/lib/libc.so.6 (0x00007f8a4a200000)
        libpthread.so.0 => /usr/lib/libpthread.so.0 (0x00007f8a4a1fc000)
        libdl.so.2 => /usr/lib/libdl.so.2 (0x00007f8a4a1f6000)
        libutil.so.1 => /usr/lib/libutil.so.1 (0x00007f8a4a1f1000)
        libm.so.6 => /usr/lib/libm.so.6 (0x00007f8a4a0ac000)
        /lib64/ld-linux-x86-64.so.2 => /usr/lib64/ld-linux-x86-64.so.2 (0x00007f8a4a5f3000)</span>

<span style="color: #8F33DF;">ffdiracex@abyss:~$</span> pacman -Qo /usr/bin/python3 /usr/bin/g++ /usr/bin/rustc
<span style="color: #00ff88;">/usr/bin/python3 is owned by python 3.12.0-1
/usr/bin/g++ is owned by gcc 13.2.1-1
/usr/bin/rustc is owned by rust 1.73.0-1</span>

<span style="color: #8F33DF;">ffdiracex@abyss:~$</span> stat /usr/bin/python3
<span style="color: #00ff88;">  File: /usr/bin/python3 -> python3.12
  Size: 21              Blocks: 0          IO Block: 4096   symbolic link
Device: 8,2     Inode: 1234567     Links: 1
Access: (0777/lrwxrwxrwx)  Uid: (    0/    root)   Gid: (    0/    root)
Access: 2024-01-01 00:00:00.000000000 +0000
Modify: 2024-01-01 00:00:00.000000000 +0000
Change: 2024-01-01 00:00:00.000000000 +0000</span>

<span style="color: #8F33DF;">ffdiracex@abyss:~$</span> echo "I use Arch btw"
<span style="color: #00ff88;">I use Arch btw</span>

<span style="color: #8F33DF;">ffdiracex@abyss:~$</span> uname -a
<span style="color: #00ff88;">Linux abyss 6.6.1-arch1-1 #1 SMP PREEMPT_DYNAMIC x8664 GNU/Linux</span>

<span style="color: #8F33DF;">ffdiracex@abyss:~$</span> df -h / /home /usr
<span style="color: #00ff88;">Filesystem      Size  Used Avail Use% Mounted on
/dev/sda2        50G   32G   18G  64% /
/dev/sda3       200G  120G   80G  60% /home
/dev/sda1        20G   12G  8.0G  60% /usr</span>

<span style="color: #8F33DF;">ffdiracex@abyss:~$</span> free -h
<span style="color: #00ff88;">               total        used        free      shared  buff/cache   available
Mem:            15Gi       5.2Gi       2.1Gi       345Mi       7.7Gi       9.1Gi
Swap:          8.0Gi       0.0Ki       8.0Gi</span>

<span style="color: #8F33DF;">ffdiracex@abyss:~$</span> history | tail -5
<span style="color: #00ff88;"> 1234  git clone https://github.com/ffdiracex/dotfiles
 1235  cd dotfiles && ./install.sh
 1236  sudo pacman -Syu
 1237  vim ~/.config/i3/config
 1238  echo "I have no bitches and I must scream"</span>

<span style="color: #8F33DF;">ffdiracex@abyss:~$</span> exit
<span style="color: #00ff88;">logout</span>
  </pre>

  <!-- Stats as system info -->
  <pre style="color: #00ff88; font-family: 'Fira Code', monospace; font-size: 12px; text-align: left; background: #0a0c0f; padding: 10px; border-radius: 4px; border: 1px solid #333; width: 60%; margin: 20px auto;">
<span style="color: #8F33DF;">ffdiracex@abyss:~$</span> github-stats --display
<span style="color: #00ff88;">─────────────────────────────────
 ⭐ Total Stars Earned: 42
 📦 Total Commits: 2,718
 🍴 Total Repos: 28
 🔀 Total Forks: 13
 👥 Followers: 69
─────────────────────────────────</span>

<span style="color: #8F33DF;">ffdiracex@abyss:~$</span> gh activity --last-30-days
<span style="color: #00ff88;">2024-12-01  pushed to ffdiracex/dotfiles:main
2024-12-03  opened PR #42 in ffdiracex/neovim-config
2024-12-07  merged PR #69 in ffdiracex/arch-install
2024-12-15  created repo ffdiracex/abyss-wm
2024-12-24  starred 7 repos (merry christmas)
2024-12-31  contributed to linux/linux (typo fix)</span>
  </pre>

  <!-- Contribution graph -->
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=ffdiracex&bg_color=0a0c0f&color=00ff88&line=8F33DF&point=ffffff&area=true&area_color=1a0c2a&hide_border=true" width="90%"/>

  <!-- Footer -->
  <pre style="color: #00ff88; font-family: 'Fira Code', monospace; font-size: 12px; text-align: left; background: #0a0c0f; padding: 10px; border-radius: 4px; border: 1px solid #333; width: 80%; margin: 20px auto;">
<span style="color: #8F33DF;">ffdiracex@abyss:~$</span> echo "Thanks for visiting"
<span style="color: #00ff88;">Thanks for visiting</span>

<span style="color: #8F33DF;">ffdiracex@abyss:~$</span> uptime
<span style="color: #00ff88;"> 18:23:14 up 2 weeks, 0 users,  load average: 0.42, 0.69, 0.13</span>

<span style="color: #8F33DF;">ffdiracex@abyss:~$</span> <span style="color: #ffffff;">_</span>
  </pre>
  
  <p>
    <img src="https://komarev.com/ghpvc/?username=ffdiracex&style=flat-square&color=8F33DF" />
  </p>
</div>
