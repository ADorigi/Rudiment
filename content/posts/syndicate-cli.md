---
title: "Syndicate CLI"
date: 2024-02-22T18:16:18-05:00
description: "A TUI for Syndicate"
draft: false
author: "Adnan Gulegulzar"
cover: "/images/syndicate-cli/syndicate-cli-high-resolution-logo.png"
tags: ["TUI","GO","open-source","CLI"]
theme: "light"
---

![Syndicate CLI|big](/images/syndicate-cli/syndicate-cli-high-resolution-logo.png)

I believe you peeps know about the amazing Syndicate. Go check it out at [Rudiment/Syndicate](https://rudiment.gule-gulzar.com/posts/syndicate/). Nevermind, even [Pepe](https://rudiment.gule-gulzar.com/posts/initrudiment/) ususally ignores such links to other posts. Its not a good thing to do. Rethink your decision.

![Need help?|inline](/images/syndicate-cli/stop-it-get-some-help.gif)


Anyways, to explain briefly, Syndicate is a GUI application which gives you basic information about your system. Its functionality is decoupled into another repo, [adorigi/systeminfo](https://github.com/ADorigi/systeminfo), and the GUI acts as a wrapper to use this repo's functionality. By design, it is a complete GUI(Graphic User Interface) application.

# What if you don't want a fully blown GUI?

Don't worry, I've got you covered. This post is dedicated to another way you can take advantage of Syndicate, right from the comfort of your terminal. I've packaged the functionality of Syndicate into a binary with an intuitive and simple interface accessible from inside the terminal.

# What is syndicate-cli?

It is another wrapper of [systeminfo](https://github.com/ADorigi/systeminfo) which works like a [charm](https://charm.sh/)(huehue :skull:). I employed [Bubble Tea](https://github.com/charmbracelet/bubbletea) from the charm bracelet to charm up your terminal(okay this is the last of the puns). Github actions clubbed with goreleaser, builds and pushes the required binaries to my personal brew tap hosted on my github profile. 

# How does it look?

The interface is pretty simple. It currently has 3 tabs, System Information, Disk Information and Network Information. I have plans to evolve it in the future and its interface might change, so "WATCH OUT". 

![How it looks|inline](/images/syndicate-cli/syndicate-cli.gif)

# What's under the hood?

Under the covers, the cli is built following the ELM architecture, which is kinda the only choice when using BubbleTea. Gotta say Lipgloss and BubbleTea are pretty cool. Also, lots of praises to Goreleaser. All it needs is the tap repository and it builds and publishes the binary to the tap. 

# What do I need to use it?

I built this application on MacOS with ARM64 architecture. But I have tested this on an Ubuntu VM with AMD64 architecture and it works identically.  

Apart from that, all you need is Homebrew. Thats the beauty of Go. The binaries are standalone and dont need any accompaning software or library.  

Here are the steps to get you going with syndicate-cli:
- Install Homebrew from its official website, [Brew.sh](https://brew.sh):

```
> brew -v
```

- Add my custom homebrew tap to access the binaries for syndicate-cli and then update brew: 

```
> brew tap adorigi/adorigi
```

- Install the syndicate-cli 

```
> brew install syndicate-cli
```

# How do I use it?

Once you have syndicate-cli installed, all you need to do is run the following command from anywhere in your terminal to access it.

```
> syndicate-cli
```

# My views on the app

Firstly I completely agree its not a finished product. It needs small adjustments like a title;it needs modularity, testing; it needs minor bug fixes and what not. But its a working product. I needed to get it out there. And I needed "this" post to post a link to on LinkedIn. I guess I will do it soon. But I would love to hear from you about how I can improve it. Roast me in the comments 🤓 .

# Important links

- [Charm](https://charm.sh)
- [Bubble Tea](https://github.com/charmbracelet/bubbletea)
- [Github repo for syndicate-cli](https://github.com/ADorigi/syndicate-cli)
- [Go Releaser](https://goreleaser.com)
- [Homebrew](https://brew.sh)

