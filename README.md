M_N_M_L
=======
Here's a screenshot of **minimal-path-git** variant:

![alt tag](https://raw.github.com/S1cK94/minimal/master/screen.gif)

There are 4 variants:

* **minimal**: it loads only `minimal` module.
* **minimal-path**: it loads `minimal` and `path` modules.
* **minimal-path-host**: it loads `minimal`, `path` and `host` modules.
* **minimal-path-git**: it loads `minimal`, `path` and `git` modules.
* **minimal-path-git-host**: loads `minimal`, `path`, `git` and `host` modules

minimal
-----------------
The left prompt is very discrete but useful:
```
❯❯❯
```
* The first `❯` will light up (becomes green) if you have super user privileges.
* The second `❯` will light up (becomes green) if you have 1 or more background jobs.
* The third `❯` will become green if the exit status of your last command is 0,
otherwise will become red

minimal-path
----------------------
It will show the last 2 segments of your current directory in the right
prompt.  
Home directory is abbreviated with `~`.
```
❯❯❯                                                           Workspace/minimal
```

minimal-path-host
---------------------------
It will display the hostname (up to the first `.`) in the right prompt.
```
❯❯❯                                                   Workspace/minimal SierraX
```

minimal-path-git
--------------------------
If you work with git, you will appreciate this.  
It will show branch information in the right prompt.
The branch name will be red if is dirty, otherwise will be green.

```
❯❯❯                                                    Workspace/minimal master
```

minimal-path-git-host
-------------------------------
It shouldn't be hard to guess at this point, but here the example anyway.
```
❯❯❯                                            Workspace/minimal master SierraX
```

Customization
=============
If you just don't like the color palette, you can use your own!  
Before you source the theme, you can alter these variable value to suit your
needs:
* **PROMPT_CHAR**: if you need another character in the prompt (default `❯`)
* **ACCENT_COLOR**: by default is `$fg[green]`, is used to show statuses (root
permissions, bg jobs, exit status == 0, branch is clean).
* **ERROR_COLOR**: by default is `$fg[red]`, is used to show error statuses
(exit status != 0, branch is dirty).
* **NORMAL_COLOR**: by default is `$reset_color`, is used to show normal
statuses (user isn't root, no bg jobs).
* **PATH_COLOR**: by default is `[38;5;244m`, is the color used for path
* **HOST_COLOR**: by default is `[38;5;244m`, is the color used for host

LICENSE
=======

MIT (see LICENSE file)
