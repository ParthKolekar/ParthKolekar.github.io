---
title: You Can(t) See Me
date: 2016-02-13 10:13 UTC
tags:
  - ctf
  - stegno
---

> On the wonderland of britannia, there are two kinds of dragons Red and Black.
> Master Zero is the commander of blacks and all the black dragons support him. 
> The Red dragons' leader Amiya thinks that the Reds are the best among dragons and blacks are nothing but useless.
> So they want to teach a lesson to black dragons. They encoded a message in 
> this image and sent it to them asking them to decode it. Can they see the message?
>
> ![Attached Image](2016-02-13-you-can-t-see-me/color.png)

## Write-up

by [ParthKolekar](https://github.com/ParthKolekar)

The image of is 7 x 200 pixels. This is a hint to show that it mst be an ascii text where
each pixel is actually a bit of the 8-bit ascii. 

The red is a binary 1 and the black is a binary 0.

On reading this, we get a text 

    3xXKkFstTUpsG2IFDirE6xDrcAF8DSx4iWxd5f9IQ9T205izN8lS2MQUlsF11gT4TFXHHlLHVHprNTtrh6lURfdUW7Lpuzgu1VKzwb1bg1oq6Ae3GnykkLZZsnze3HVLxHlfCYtzyrcV2Oxp0Gb0Z2ELphR4Oxo7TyvHCuWKWlN8t8KIfHysZK7jBNPu6wRVEUPIwVra

This is the flag. This is also a good lesson learnt about why having a flag format is important.
