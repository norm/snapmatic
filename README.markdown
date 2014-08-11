snapmatic
=========

A little perl script to fetch the latest snapmatic images from your Rockstar
Social Club account.

Installation
------------

    # install some perl modules
    brew install cpanminus
    sudo cpanm HTTP::CookieJar HTTP::Tiny IO::All JSON Modern::Perl

    # execution permissions
    sudo chmod +x snapmatic

    # copy the script to your $PATH
    sudo cp snapmatic /usr/local/bin

Usage
-----
    snapmatic [-m] [-o <dir>] [-d|-t] <account> [<platform>]

    -m  Download the metadata (in JSON format) in addition to photo

    -o <dir>
        Download files to <dir> rather than current directory

    -t  Use the time the photo was taken as the filename, not the ID.  eg
        "2014-08-11-22.00.42.jpg"

    -d  Use the time the photo was taken as the filename, not the ID.
        Creates subdirectories based on year, month, and day.  eg
        "2014/08/11/22.00.42.jpg".

        If both "-t" and "-d" are specified, "-d" takes precedence.

    <account>
        The slug of the Social Club account, normally the account name but
        lowercase.  You can confirm this by logging into Social Club and
        clicking the profile link in the top right. The URL will end with
        the slug.

        eg. My account is "InvaderNorm", so my slug should be `invadernorm`; 
        my profile is at http://socialclub.rockstargames.com/member/invadernorm
        confirming this.

    <platform>
        The platform ID: 1 for Xbox 360 (default), 2 for PS3.

[sc]: http://socialclub.rockstargames.com
