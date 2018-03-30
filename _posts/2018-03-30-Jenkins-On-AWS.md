---
layout: post
title: Working with Jenkins, Django and Ubuntu AWS
published: true
---

I've spend the last couple of days scratching the surface of AWS EC2. The goal is to get Jenkins up and running on it for my Continous Intergration setup. This isn't for a production environment though, just an exercise in new technology.

I started out with a Red Hat Linux server, but it didn't have a simple method for installing Firefox, which is a component for the functional tests I'm performing. So, since I had just created the instance, I decided to scratch and create another.

Once the server was up and running, next was insalling Jenkins. Which I did via a setup found via google and [this script](https://github.com/davidmoten/jenkins-ec2-https) provided by David Moten at github.

Using the TDD book configuration I was able to get Python connected, and a few other plugins installed. I tried a build, but it was spitting out errors on f strings, so that's when I realized that the EC2 server had Python 3.5 installed. In addition to just trying to install it, I also ran into space problems, as I created a larger swapfile than I probably needed and trying to install was giving a out-of-space errors. Learning a few Linux commands and bearing down, I sorted out the space issues and used [this page's](https://www.caseylabs.com/how-to-create-a-python-3-6-virtual-environment-on-ubuntu-16-04/) advice to get 3.6 running.

There are still errors, but now they're at least new, different, hopefully progressive errors. We'll see what tomorrow holds.
