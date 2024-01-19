---
title: The Plain Text Life
date: 2023-09-27T10:21:00
draft: false
---

I finally flipped the table over my frustration with "modern" applications and tech stacks when it comes to simple note taking, calendar and lists.

My current setup is a folder containing the following text files:

- todo.txt
- done.txt
- calendar.txt
- contacts.txt
- self-tracking.txt (helping me rid caffeine and alcohol)
- links.txt
- ideas.txt
- goals.txt

These are kept in sync via [Syncthing](https://syncthing.net/) over my WireGuard mesh on each device. I can open any of the above in any text editor or pull the info I need in multiple ways via in-app search, `ripgrep`, `grep`. There's no uncertainty in getting the data out, no ties to a specific protocol or app and will work on _any_ operating system.

For instance, I live in the terminal so I created the following alias `agenda` along with an `echo` statement in my `~/.zshrc` to display today and tomorrow's entries when I launch a shell:

```
alias agenda='grep -A 1 --colour=always $(date +"%Y-%m-%d") "$HOME/Productivity/calendar.txt"'
echo agenda
```

Which displays the following when launching a new shell or running `agenda`:

```
Last login: Tue Sep 26 18:14:08 on ttys000

Today's Agenda:
2023-09-26 w39 Tue  @Video 14:30 Boring Meeting.
2023-09-27 w39 Wed  16 Pick-up kids.

[✓] >
```

Another example, using tags and the `done.txt` I've managed to automate an annoying weekly email I have to send to my manager using a small shell script and regex. I'm not familiar with Windows these days, but I'm sure you could rig the above via PowerShell or whichever nonsense they use.

I don't think I can ever go back to CalDAV, CardDAV, ${NOTE_APP} or ${CLIENT}. I can freely move around Neovim, iA Writer, Xed or Sublime Text. No surveillance capitalism or other funny business at play and easy to keep backups.

**Links**

- [todo.sh](https://github.com/todotxt/todo.txt-cli) (If you're on iOS, I recommend [SwifttoDo](https://itunes.apple.com/us/app/swiftodo-task-list-for-todo.txt/id1073798440?ls=1&mt=8))
- [Calendar.txt](https://terokarvinen.com/2021/calendar-txt/)
- [The Plaintext Project](https://plaintextproject.online/articles.html)
- [10 Plain Text Files You Should Have on Your Desktop for Higher Productivity](https://zapier.com/blog/plain-text-files-for-productivity/)
	- I hate links prefaced with "10 Things You Should Do to X!," but I genuinely found these useful.

<!--more-->
