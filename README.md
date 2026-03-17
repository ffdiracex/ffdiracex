<div align="center">
  
  <!-- Pure terminal, just raw command output -->
  <pre style="color: #00ff88; font-family: 'Fira Code', 'Courier New', monospace; font-size: 13px; text-align: left; background: #000000; padding: 25px; border: 2px solid #33ff33; width: 85%; margin: 20px auto; box-shadow: 0 0 10px #00ff88;">
<span style="color: #ffff00;">[ffdiracex@archbtw ~]$</span> <span style="color: #ffffff;">whoami</span>
<span style="color: #00ff88;">ffdiracex</span>

<span style="color: #ffff00;">[ffdiracex@archbtw ~]$</span> <span style="color: #ffffff;">cat /etc/passwd | grep ffdiracex</span>
<span style="color: #00ff88;">ffdiracex:x:1000:1000:Pointer to a Lord:/home/ffdiracex:/bin/bash</span>

<span style="color: #ffff00;">[ffdiracex@archbtw ~]$</span> <span style="color: #ffffff;">sudo cat /etc/shadow | grep ffdiracex</span>
<span style="color: #ff0000;">[sudo] password for ffdiracex: </span>
<span style="color: #00ff88;">ffdiracex:$6$rounds=656000$MallocIsLife$NULL.420:19769:0:99999:7:::</span>

<span style="color: #ffff00;">[ffdiracex@archbtw ~]$</span> <span style="color: #ffffff;">echo $USER</span>
<span style="color: #00ff88;">ffdiracex</span>

<span style="color: #ffff00;">[ffdiracex@archbtw ~]$</span> <span style="color: #ffffff;">echo $SKILL_LEVEL</span>
<span style="color: #00ff88;">*(int*)NULL // undefined but massive</span>

<span style="color: #ffff00;">[ffdiracex@archbtw ~]$</span> <span style="color: #ffffff;">echo $INTELLIGENCE</span>
<span style="color: #00ff88;">> /dev/null 2>&1 # too large to display, returns (void*)0</span>

<span style="color: #ffff00;">[ffdiracex@archbtw ~]$</span> <span style="color: #ffffff;">cat ~/.bashrc | grep -i genius</span>
<span style="color: #00ff88;">export GENIUS_LEVEL=unlimited
export BRAIN_CAPACITY=$(df -h /dev/brain | grep -oP '\d+%' | sed 's/%//')% # always 100%
export CC=gcc # obviously
export CFLAGS="-Wall -Wextra -Wpedantic -Werror -O3 -march=native -fno-stack-protector # real programmers don't need stack canaries"</span>

<span style="color: #ffff00;">[ffdiracex@archbtw ~]$</span> <span style="color: #ffffff;">df -h /home/ffdiracex/brain</span>
<span style="color: #00ff88;">Filesystem      Size  Used Avail Use% Mounted on
/dev/brain      1.0P  1.0P     0 100% /home/ffdiracex/brain</span>

<span style="color: #ffff00;">[ffdiracex@archbtw ~]$</span> <span style="color: #ffffff;">cat /proc/cpuinfo | grep "model name" | head -1</span>
<span style="color: #00ff88;">model name      : ffdiracex's Neocortex (9999 cores, 1.21 jiggahertz, direct memory access)</span>

<span style="color: #ffff00;">[ffdiracex@archbtw ~]$</span> <span style="color: #ffffff;">free -h | grep Mem</span>
<span style="color: #00ff88;">Mem:           1.0Y    999T    1.0T    0.0T    0.0T    999T</span>

<span style="color: #ffff00;">[ffdiracex@archbtw ~]$</span> <span style="color: #ffffff;">uptime</span>
<span style="color: #00ff88;"> 14:00:00 up 1337 days, 42 min,  load average: 0.01, 0.02, 0.01 (i'm just warming up, no segfaults yet)</span>

<span style="color: #ffff00;">[ffdiracex@archbtw ~]$</span> <span style="color: #ffffff;">cat ~/.bashrc | grep -E '(alias|function)'</span>
<span style="color: #00ff88;">alias fuck='sudo $(history -p !!)' # because I never make mistakes
alias please='sudo'
alias rm='rm -i' # I'm not a monster
alias grep='grep --color=auto'
alias ls='ls --color=auto'
alias vim='nvim'
alias :q='exit'
alias :wq='echo "This isn't vi, moron"'
alias python='python3'
alias fuckingpython='python3 -c "import this; print(\"PEP 20 is for plebs\")"'
alias javascript='echo "console.log(\"JavaScript? In MY terminal? Segmentation fault (core dumped)\")"'
alias java='echo "java: command not found. Good riddance. C is love, C is life."'
alias npm='echo "node_modules is 1.2GB and counting... abort"'
alias c='gcc -std=c99 -o $(basename $1 .c) $1 && ./$(basename $1 .c) # real programmers use this'
alias gdb='gdb -q # quiet mode because I know what I'm doing'
alias valgrind='valgrind --leak-check=full --show-leak-kinds=all --track-origins=yes # because I don't leak (usually)'</span>

<span style="color: #ffff00;">[ffdiracex@archbtw ~]$</span> <span style="color: #ffffff;">cat /home/ffdiracex/.config/i3/config | grep bindsym | head -5</span>
<span style="color: #00ff88;">bindsym $mod+Return exec st
bindsym $mod+d exec dmenu_run
bindsym $mod+Shift+q kill
bindsym $mod+Shift+e exec "i3-msg exit | echo 'coward'"
bindsym $mod+Shift+r exec "i3-msg restart | echo 'reloading... like a peasant writing in Python'</span>

<span style="color: #ffff00;">[ffdiracex@archbtw ~]$</span> <span style="color: #ffffff;">history | grep -i "fixed" | wc -l</span>
<span style="color: #00ff88;">0</span>

<span style="color: #ffff00;">[ffdiracex@archbtw ~]$</span> <span style="color: #ffffff;">history | grep -i "broke" | wc -l</span>
<span style="color: #00ff88;">1337</span>

<span style="color: #ffff00;">[ffdiracex@archbtw ~]$</span> <span style="color: #ffffff;">history | tail -10</span>
<span style="color: #00ff88;"> 1330  git commit -m "magic"
 1331  git push origin main --force-with-lease # YOLO
 1332  sudo pacman -Syu --noconfirm
 1333  echo "I use Arch btw"
 1334  vim /etc/pacman.d/mirrorlist
 1335  gcc -o hello hello.c && ./hello
 1336  gdb ./segfaulting_program
 1337  rm -rf /tmp/plebs
 1338  echo "I have no bitches and I must free()"
 1339  neofetch | lolcat</span>

<span style="color: #ffff00;">[ffdiracex@archbtw ~]$</span> <span style="color: #ffffff;">cat /home/ffdiracex/.plan</span>
<span style="color: #00ff88;">────────────────────────────────────────────────────────────────
                       ____    _   _   _   ____  
                      / ___|  | | | | | | |  _ \ 
                     | |      | | | | | | | |_) |
                     | |___   | |_| | |_| |  __/ 
                      \____|   \___/  \___/ |_|   
                                                
                      C IS LOVE, C IS LIFE
────────────────────────────────────────────────────────────────
I live in source code. I dream in pointers.
I write my own malloc. I free() when I'm done.
I've seen things you people wouldn't believe.
Dangling pointers off the shoulder of Orion.
I watched buffer overflows glitter in the dark near the Tannhäuser Gate.
All those moments will be lost in time, like segfaults in rain.
Time to die.

────────────────────────────────────────────────────────────────
CURRENT PROJECTS:
  > rewriting nginx in pure C (because rust is for people afraid of pointers)
  > writing my own WM in C (because i3 is too bloated, dwm is too minimalist)
  > kernel module that plays rickroll on boot (in C, obviously)
  > bitcoin miner in bash (why? because I can, but the core is in C)
  > my own libc (because glibc is for normies)
  > static analysis tool that judges your coding style

────────────────────────────────────────────────────────────────
SKILLS:
  C:           I wrote my own kernel module just to feel something
  Rust:        I use it when I want the compiler to hold my hand
  Python:      I use it for glue code while judging it silently
  C++:         It's okay I guess, but templates give me PTSD
  Assembly:    I speak to the metal and the metal listens (sometimes it segfaults)
  JavaScript:  I don't touch that shit (see: "segfault in rain")
  Make:        .PHONY: all clean install uninstall install-world-domination

────────────────────────────────────────────────────────────────
LANGUAGE RANKINGS:
  1.  C    - The One True Language
  2.  Rust - The Overachiever
  3.  C++  - The Complicated Ex
  4.  Python - The Script Kiddie
  5.  Bash - The Wizard's Staff
  6.  Assembly - The Dark Arts
  7.  Java - The Enterprise Nightmare
  8.  JavaScript - The Plague

────────────────────────────────────────────────────────────────</span>

<span style="color: #ffff00;">[ffdiracex@archbtw ~]$</span> <span style="color: #ffffff;">cat /home/ffdiracex/.github/stats</span>
<span style="color: #00ff88;">────────────────────────────────────────────────────────────────
                    GITHUB STATISTICS
────────────────────────────────────────────────────────────────
  Commits:         git log --oneline | wc -l # it's over 9000
  Lines written:   find . -name "*.c" -o -name "*.h" | xargs wc -l | tail -1
  Bugs introduced: #define BUGS 0 // intentional
  PRs merged:      All of them (maintainers fear my pointer arithmetic)
  Issues opened:   Only against electron apps and JavaScript frameworks
  Stars received:  More than Linus has opinions
  Forks:           Imitation is the sincerest form of flattery
  Followers:       They want to learn my ways
  Following:       Nobody's on my level (except maybe Ken Thompson)
────────────────────────────────────────────────────────────────
LANGUAGE BREAKDOWN (by bytes written):
  C:            ████████████████████ 98.2%
  Rust:         ░░░░░░░░░░░░░░░░░░░░ 1.2%
  Python:       ░░░░░░░░░░░░░░░░░░░░ 0.4%
  C++:          ░░░░░░░░░░░░░░░░░░░░ 0.1%
  Shell:        ░░░░░░░░░░░░░░░░░░░░ 0.1%
  JavaScript:   ░░░░░░░░░░░░░░░░░░░░ 0.0% (intentional)
────────────────────────────────────────────────────────────────</span>

<span style="color: #ffff00;">[ffdiracex@archbtw ~]$</span> <span style="color: #ffffff;">cat /home/ffdiracex/.opinions</span>
<span style="color: #00ff88;">────────────────────────────────────────────────────────────────
                    UNASKED OPINIONS
────────────────────────────────────────────────────────────────
  tabs vs spaces:        Tabs (spaces are for cowards, both are worse than C)
  vim vs emacs:          vim (emacs is an OS, not an editor, but both are worse than ed)
  systemd:               It's fine, I guess (please don't hurt me, but init scripts in C would be better)
  JavaScript:            Segmentation fault (core dumped)
  Python vs C:           There is no comparison. C is the benchmark.
  C vs C++:              C. Always C. KISS principle.
  Rust:                  It's like C with training wheels. Sometimes I need training wheels.
  garbage collection:    free() is love, free() is life
  manual memory management: The only real way to live
  Arch vs everything:    I use Arch btw (compiled from source, obviously)
  bitches:               I have none (and I'm at peace with it, my computer loves me)
────────────────────────────────────────────────────────────────</span>

<span style="color: #ffff00;">[ffdiracex@archbtw ~]$</span> <span style="color: #ffffff;">cat /home/ffdiracex/.favorite_code</span>
<span style="color: #00ff88;">────────────────────────────────────────────────────────────────
                    BEAUTIFUL C CODE
────────────────────────────────────────────────────────────────

#include &lt;stdio.h&gt;
#include &lt;stdlib.h&gt;

int main(void) {
    printf("I use Arch btw\n");
    
    char *love = malloc(42 * sizeof(char));
    if (love == NULL) {
        fprintf(stderr, "Even malloc knows I have no bitches\n");
        return 1;
    }
    
    sprintf(love, "C is love, C is life");
    printf("%s\n", love);
    
    free(love); // always free your love, kids
    return 0;
}

────────────────────────────────────────────────────────────────</span>

<span style="color: #ffff00;">[ffdiracex@archbtw ~]$</span> <span style="color: #ffffff;">echo "I use Arch btw"</span>
<span style="color: #00ff88;">I use Arch btw</span>

<span style="color: #ffff00;">[ffdiracex@archbtw ~]$</span> <span style="color: #ffffff;">gcc --version | head -1</span>
<span style="color: #00ff88;">gcc (GCC) 13.2.1 20230801</span>

<span style="color: #ffff00;">[ffdiracex@archbtw ~]$</span> <span style="color: #ffffff;">exit</span>
<span style="color: #00ff88;">logout</span>

<span style="color: #ffff00;">[ffdiracex@archbtw ~]$</span> <span style="color: #ffffff;">_</span>
  </pre>

  <!-- Footer with just a blinking cursor -->
  <pre style="color: #00ff88; font-family: 'Fira Code', 'Courier New', monospace; font-size: 13px; text-align: left; background: #000000; padding: 10px; border: none; width: 85%; margin: 20px auto;">
<span style="color: #ffff00;">[ffdiracex@archbtw ~]$</span> <span style="color: #ffffff;">echo 'EOF'</span>
<span style="color: #00ff88;">EOF</span>

<span style="color: #ffff00;">[ffdiracex@archbtw ~]$</span> <span style="color: #ffffff;">_</span>
  </pre>
</div>
