---
title: How to resolve hugo version conflicts with the default version on netlify
author: Aaron Simumba
date: '2017-09-13'
slug: how-to-resolve-hugo-version-conflicts-with-the-default-version-on-netlify
tags:
  - netlify
  - hugo
  - continous deployment
description: Resolving desired hugo version conflict with the default hugo build on netlify.
#image: "images/background.jpg"
authoravatar: "../../images/avatar.png"
---

There is nothing as frustrating as getting stuck with a computer operation/code bug, which you know no better how to get around it. That was my frustration while trying to deploy my website through netlify. Having changed the theme I was initially working with to the new theme, [Cactus](https://themes.gohugo.io/cactus/). I later discovered, the theme is only compatible with version 0.20 and above of the static site generator [hugo](https://gohugo.io/). After hours of trying to debug what the problem might be to no avail. Before I could finally give up for another day, I stumbled upon this [post](https://www.netlify.com/blog/2017/04/11/netlify-plus-hugo-0.20-and-beyond/) that opened my eyes to look in the right place.

After all, the solution is quite simple and straight forward to implement. [netlify](https://www.netlify.com/) uses version 0.17 as the default hugo build for deploying sites built under the hugo platform. And some hugo themes uses the more recent versions which are above version `0.17`. 


A quick work around is to define the build environment with the version of hugo you desire or that fits with the theme being used. Under the site settings, you navigating to the build & deploy panel, locate the build environment variables. In the `key` value slot you type `HUGO_VERSION` and in the `value` place-holder, you define the hugo version. For instance version `0.27` as can be seen in the screenshot below. 
With this in place, you can expect a smooth build of the site and deployment. 


![](https://user-images.githubusercontent.com/24398851/30351782-bb5cb162-9825-11e7-9821-967de86b7214.png)
Happy blogging...


