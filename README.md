# irssi-prowl

[Irssi](http://www.irssi.org/) script for sending
[Prowl](http://www.prowlapp.com/) notifications.

## Features

* Notifications on all hilights when away
* Notifications on private messages when away
* Notifications on private actions (``/me``) when away
* Manual notifications using the ``/prowl`` command
* Customizable Prowl priority levels

## Installing

This script depends on
[WebService::Prowl](http://search.cpan.org/dist/WebService-Prowl/). To
install this dependency, run the following command in your terminal:

    cpan WebService::Prowl

Hint: You don't need root access to install perl modules, check out
[local::lib](http://search.cpan.org/dist/local-lib/)

Download
[prowl.pl](https://raw.github.com/henrikbrixandersen/irssi-prowl/master/prowl.pl)
and place it in ``~/.irssi/scripts/``.

## Usage

To activate the script, run the following commands in Irssi:

    /script load prowl
    /set prowl_apikey 0123456789abcdef0123456789abcdef01234567
    /save

Prowl notifications can be sent manually using the ``/prowl`` command:

    /help prowl
    /prowl Hello, world
    /prowl -url https://github.com/henrikbrixandersen/irssi-prowl -priority 2 Check out this cool irssi-prowl script!

To change the priority of the Prowl notifications for private
messages, hilights and the default priority for the ``/prowl`` command,
use the following settings:

    /set prowl_priority_msgs 1
    /set prowl_priority_hilight 0
    /set prowl_priority_cmd -2

To assist in debugging, turn on the following setting:

    /set prowl_debug on

## License

This script is licensed under the 2-clause BSD license. See the script
header for the license text.
