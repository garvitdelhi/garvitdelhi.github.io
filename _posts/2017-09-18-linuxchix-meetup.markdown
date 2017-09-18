---
layout: post
title:  "LinuxChix Meetup"
date:   2017-09-18 4:00:00
tags: Talk File-System Linux Tech
draft: 1
---

Yesterday, I gave a talk on Linux file systems at LinuxChix Delhi meetup group. I have to firstly apologize for all the participants and the organizers, Shivani Bhardwaj and Priyal Trivedi for reaching the venue late. It is a great effort by both of them to enlighten the youth and female community about the advancements in Linux. They are trying their best to help them learn basics, benefits and enormous opportunities that Linux exposes. It is optimistic to see the female community taking such
initiative in the software industry. The best part of the group is that they welcome all, young, male, female, professionals and students to join and share their thoughts.

Coming back to me being late, I had my scheduled at 5:00 pm and I reached 5:10 pm at the venue and sadly missed all the talks for that day. I heard that talk by **_Suhaib's_** on [*"How SSH Works"*](https://drive.google.com/file/d/0B52KsQVy2Z4TZ1dxdVdrck9Eanc/view) was fantastic and so was **_Anu's_** talk sharing her experience on Linux. You can find more about Anu's talk and get the slides from her [blog](http://anu-mittal.blogspot.in/2017/09/linuxchix-meet-up-experience.html). Apparently, all
of the speakers were from [Zomato](https://zomato.com). Hence felt like a reunion to meet them at the meetup.

About my talk, it started with the history of why the extended file system (Ext) came into existence. I covered the file system with which Linux started, i.e., Minix (Mini-Unix) file system. Continuing to the presence of Ext and Ext2 along with Xia file system. Here is a snippet from my presentation which shows a quick comparison between all the filesystems mentioned above:

![Comparison between Minix, Ext, Ext2, and Xia File systems]({{ site.url }}/assets/article_images/2017-09-15-linuxchix-meetup/file_system_comparison.png "Comparison between Minix, Ext, Ext2, and Xia File systems")

Further, I explained the basic elements of a file system, i.e., inodes, directories, and links. I explained the need for a virtual file system layer that was added by _Chris Provenzano_ and how it helped abstracting out file systems for application layer while never wandering about the implementation of the actual file system on the hardware. It was much of learning for me too as I found many facts and stories while looking out for the content for this presentation. You can find my presentation
hosted on the drive, with this [link](https://docs.google.com/presentation/d/1KfvcYccbXzVP5F8Oh6a1zVi9GpA6zWO14NVbdpuPBVw/edit?usp=sharing). I took most of my inspiration from the research paper published by Rémy Card, Theodore Ts'o, and Stephen Tweedie. You can find their research paper [here](http://e2fsprogs.sourceforge.net/ext2intro.html).

To end this blog, as the organization of LinuxChix says they need more participation from the female community and they want them to come forward and share their experience. So from this blog, I am inviting all the readers to join the linuxChix group and be a part of this initiative. You can find them from [meetup page](https://www.meetup.com/LinuxChix-India-Meetup/) and also join [telegram group](https://t.me/joinchat/BzYbR0NlHezSUou42Q78JQ).

Adios till my next blog, happy hacking :)
