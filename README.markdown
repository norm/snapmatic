snapmatic
=========

A little python script to fetch all published "snapmatic" images from your
Rockstar [Social Club][sc] account. It needs to login as you to do this.

[sc]: http://socialclub.rockstargames.com

## Installation

    # install some python modules
    sudo pip install beautifulsoup4 requests

    # copy the script to your $PATH
    sudo cp snapmatic /usr/local/bin
    sudo chmod 755 /usr/local/bin/snapmatic


## Usage

    snapmatic [-d|--use-subdirs] [-l|--user <user>] [-m|--metadata]
              [-o|--directory <dir>] [-p|--password <pass>]
              [-t|--use-timestamp] [-v|--verbose]

* -d, --use-subdirs

    Create subdirectories from the timestamp of the picture,
    eg. `2015/08/21`

* -l *user*, --user *user*

    Login to Social Club as *user*. Can also be set in the environment
    variable `SOCIALCLUB_USER`. Command line overrides environment.

* -m, --metadata

    Save the JSON data of the picture in addition to the image.

* -o *dir*, --directory *dir*

    Save files to *dir* rather than the current directory.

* -p *pass*, --password *pass*

    Login to Social Club with the password *pass*. Can also be set in the
    environment variable `SOCIALCLUB_PASSWORD`. Command line overrides
    environment.

* -t, --use-timestamp

    Add the timestamp to the filename of created files. Without this, the
    pictures will be saved with the ID of the picture, eg
    `OfgJGAp_C0-JpY8E_0wpZQ.jpg`. With this, they will be saved as
    `2015-08-19-18.36.22.OfgJGAp_C0-JpY8E_0wpZQ.jpg`.

* -v, --verbose

    List the filenames of files created.


## Errors

If you see the error "Not JSON fetching photo data." then your account has
been flagged for logging in too frequently and you will need to login in
manually in a browser and fill out a [CAPTCHA].

To stop this occurring, run this script infrequently (only when you know there
are new images to download). If you run it automatically, don't do it more
than once a day.

[CAPTCHA]: https://en.wikipedia.org/wiki/CAPTCHA
