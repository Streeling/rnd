---
layout: post
title:  "How to open Outlook saved emails (.msg) files with Thunderbird "
date:   2015-12-02 16:54:00 +0300
categories: outlook thunderbird
---

Unfortunately Outlook .msg file can not be opened directly by Thunderbird, but we can convert it to .eml ( MIME RFC 822 ) format. Which Thunderbird understands very well.

For this download the project [MSGConvert][msgconvert]. We will need the file `msgconvert.pl` from `scripts` directory. Before running this script ensure that it the appropiate permissions (as a executable) and install dependencies:

    sudo apt-get install libemail-outlook-message-perl libemail-sender-perl
    optionl: sudo apt-get install libemail-outlook-message-perl libemail-localdelivery-perl

Now you can

    ./msgconvert.pl <msg-file>

or you can convert many .msg files to one

    ./msgconvert.pl --mbox <one-eml-file> <msg-files>


[msgconvert]: https://github.com/mvz/msgconvert
