---
title: How I made this website
date: 2024-06-14
categories: [tutorials, website]
tags: [en]
---

> First, a huge disclaimer: I know absolutely nothing about websites so the target audience for this is people that, like me, don't know where to start and that find it difficult to deal with the most basic things for setting this up. I'm sure many of the stuff I say are wrong, this is just my personal experience. If you **do** know about this and want to collaborate, you are most welcome!
{: .prompt-warning }

## Why I chose github pages
I never had a blog but always wanted to. I feel that there are some topics I'd like to talk about but constantly feel that I don't know enough or that it's pointless -we have way too many people giving opinions about everything anyway-. At some point I decided I didn't care, I just wanted a place to dump some of the notes I took. Everytime I get into hyperfocus research, I write a bunch of messy notes and end up deleting them because I have no use for them. So I decided to start organising those notes and making some blog posts. Then the question was where. I looked into WordPress and GitHub pages. When I started researching github I noticed that it wasn't that easy cause I know nothing about jekyll or ruby or even css, and realised that going for github would mean that I was going to try to set it up, find it too hard, get frustrated and just abandon the blog idea forever. So I went to look at the possibilites with WordPress, thought it was pretty easy, created an account and then saw the themes available for free and... hated all of them. So I went back to GitHub pages, determined to make it work. It has everything I need, it's free, looks great. Of course, the challenge and the idea of having the code on my github was a plus. You know, like when you crack the sims and feel like total hacker.

## Now let's begin!
### Installations
I started by doing some basic research and found out that, for making the kind of website I wanted, I could use some Jekyll themes for blogs so I went to the [Jekyll documentation](https://jekyllrb.com/docs/installation/#requirements){:target="_blank"} to install everything I needed. And failed. Horribly. 

It took me two days to install Ruby, I'm still not completely sure why. I ended up reinstalling anaconda and still didn't work. The problem was that I couldn't modify the `/.zshrc` like it says to do [here](https://jekyllrb.com/docs/installation/macos/){:target="_blank"} because I didn't have permission. I tried multiple ways to give the necessary permissions through the terminal, and finally managed to do it by manually changing the permissions of the file through the Finder (right click on the file -> Get Info -> Sharing & Permissions -> giving my user Read & Write privileges). I think the problem is that most turorials I followed were for intel macs and not silicon, my computer is new and I don't have everything set up yet.

I ended up installing Ruby following [this documentation](https://mac.install.guide/ruby/6){:target="_blank"}.

### Blog theme
Once the awful installations were done, it all went down much more peacefully.

I looked for a simple tutorial on youtube and this one did exactly what I wanted.

{% include embed/youtube.html id='m1RYsmOMPLs' %}


There are a bunch of [Jekyll themes out there](https://jekyllrb.com/docs/themes/){:target="_blank"} but, after carefull consideration, I chose that same one, [Chirpy](https://github.com/cotes2020/jekyll-theme-chirpy), since it has almost everything I need and it looks pretty. Still trying to find out how to change the font color though.

I'm using the [Chirpy guide to writing posts](https://chirpy.cotes.page/posts/write-a-new-post/){:target="_blank"} for the style and syntax right here.


### Customisation
I only did a few changes: 

 - I modified the tabs order ( `_tabs/` ) cause I wanted the `about` tab to show first.

 - Removed the `email` link and added the `mastodon` link. You can find the way to do that in `_data/contact.yml` and commenting and uncommenting the links you want or don't want.

 - Removed the light theme because **why would you want a light theme anyway, you freak**. (Scroll down a bit on the `_config.yml` until you find `theme_mode` and delete the one that says `light` )

 - And, my favourite, added comments! At first, I didn't realise that it was possible to do this from the theme itself so I went looking for a way to do it myself. I found [giscus](https://giscus.app/){:target="_blank"} and made it work, but then I noticed that if you scroll down a little on the `_config.yml` (a bit below the `theme_mode` ), you will find the `comments` section. You can choose the provider app. I chose giscus again. Then go to the `giscus` section and fill all the needed parameters that you can get from [giscus.app](https://giscus.app/){:target="_blank"} and you are good to go! Giscus uses github comments which is pretty cool and it works great. You can also get reactions.


## And I guess that is pretty much it!
Not too easy, not too hard. But sure it was fun!



Thanks for reading.