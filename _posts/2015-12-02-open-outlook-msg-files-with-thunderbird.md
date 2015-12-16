---
layout: post
title:  "How to open Outlook saved email (.msg) files with Thunderbird"
date:   2015-12-02 16:54:00 +0300
categories: outlook thunderbird ubuntu
---

Unfortunately Outlook .msg file can not be opened directly by Thunderbird, but we can convert it to .eml (MIME RFC 822) format. Which Thunderbird understands very well.

For this purpose download the project [MSGConvert][msgconvert]. We will need only the `msgconvert.pl` file located in [`script`][msgconvert-script] directory. Before running this script ensure that it has the appropiate permissions (as a executable) and install the dependencies:

    sudo apt-get install libemail-outlook-message-perl libemail-sender-perl

Now you can

    ./msgconvert.pl <msg-file>

or you can convert many .msg files to a single .eml

    ./msgconvert.pl --mbox <one-eml-file> <msg-files>

Other similar HOWTOs:

1. [HOWTO: Read Microsoft Outlook .MSG files in Linux][HOWTO:_Read_Microsoft_Outlook_.MSG_files_in_Linux]
1. [MSGConvert: A .MSG to mbox converter][msgconv]

[msgconvert]: https://github.com/mvz/msgconvert
[msgconvert-script]: https://github.com/mvz/msgconvert/tree/master/script
[HOWTO:_Read_Microsoft_Outlook_.MSG_files_in_Linux]: https://wiki.sabayon.org/index.php?title=HOWTO:_Read_Microsoft_Outlook_.MSG_files_in_Linux
[msgconv]: http://www.matijs.net/software/msgconv/

