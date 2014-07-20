snapmatic
=========

A little perl script to fetch the latest snapmatic images from your Rockstar
Social Club account.

Installation
------------

    # install some perl modules
    brew install cpanminus
    sudo cpanm HTTP::CookieJar HTTP::Tiny IO::All JSON

    # copy the script to your $PATH
    sudo cp snapmatic /usr/local/bin

Usage
-----

`snapmatic` takes two arguments:

1.  The slug of your social club account (normally your account name, 
    but lowercased). You can confirm this by logging into [social club][sc],
    and clicking the profile link in the top right. The URL will end 
    with the slug.

    eg. My account is "InvaderNorm", so my slug should be `invadernorm`; 
    my profile is at http://socialclub.rockstargames.com/member/invadernorm
    confirming this.

2.  The platform ID: 1 for Xbox 360 (default), 2 for PS3.

[sc]: http://socialclub.rockstargames.com

ie. running `snapmatic invadernorm 1` will save my most recent snapmatic
pictures to the current folder.
