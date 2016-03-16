ics_tools
=========

`ics_tools` is a small set of Perl scripts to try and
survive with `Mutt` in the modern world. 

`ics_process` accepts multi-part MIME emails, extracts iCal
invitations (RFC5546), and reply to them with an accept or
decline e-mail. Additionaly, it submits accepted meetings to
a CalDAV server.

This makes it essentially possible to work with invitations
and keep your calendar automatically synchronised, directly
from Mutt.

`ics_create` eases the creating ICS files to invite people.
Just attach the file to your e-mail.

`ics_put` imports an ICS file to Owncloud (which involves
splitting it into atomic events).

Configuration
-------------

Copy the example `ics_toolsrc` as `~/.ics_toolsrc`, and
fill it with your Owncloud URL and username. Install
`cadaver`. Create a `.netrc` file for `cadaver`:

        machine owncloud.example.net
        login john
        password j0hnp@ssw0rd

That should be enough!
