dshng-loginhooks - Login/Logout Hooks
=====================================

.. contents::

.. toctree::
   :maxdepth: 1

.. comment: split here
.. |copy|   unicode:: U+000A9 .. COPYRIGHT SIGN

Status and License
------------------

dshng-loginhooks was written by Rob Moggach, for `Dashing Collective Inc. <http://dashing.tv>`_
It is licensed under an `MIT-style permissive license <https://github.com/dshng/python-dirtt/raw/master/LICENSE.txt>`_.

|copy| 2011 Dashing Collective Inc. and contributors.

Licensed under the MIT license: http://www.opensource.org/licenses/mit-license.php


What It Does
------------

``dshng-loginhooks`` is a set of shell scripts that are run when a user logs in
or logs out of a network account (without a local home folder).

It is based on a few different solutions that didn't solve all of our issues.

`NHR <http://tools.mconserv.net/NHR.html>`_:
	Network Home Redirector - this one is pretty solid and forms the basis of this.
	I just didn't want it in a package and also wanted to combine a bit of everything
	he does along with the next one.
	
`Enterprise Mac Administrator's Guide <http://www.apress.com/apple-mac/mac-os-x/9781430224433>`_:
	really great concepts in here too but I wanted a bit of both so I borrowed what was
	useful.

The general problem being tackled is one of slow network speed for network home
directories caused by constant file access of things like internet or mail caches
and software that requires large files locally.

For now it is mac specific but there's no reason why these scripts couldn't be tailored
to linux use. Once installed to the path that matches the code repository it's necessary
to set a system preference from the command line as follows:

	``defaults write /private/var/root/Library/Preferences/com.apple.loginwindow LoginHook /etc/login.hook``

	``defaults write /private/var/root/Library/Preferences/com.apple.loginwindow LogoutHook /etc/logout.hook``


Contributing
------------

All kinds of contributions are welcome - code, tests, documentation, bug reports, ideas, etc.

Currently we need to implement the following:

-reverse rsync (back to the server)
-better documentation
-linux

Forking through Github
~~~~~~~~~~~~~~~~~~~~~~

First of all, you need to fork from the official repository, which is 
`https://github.com/dshng/dshng-loginhooks <https://github.com/dshng/dshng-loginhooks>`_.

Log in to Github, go to the dshng-loginhooks repository page, follow the fork link, 
wait for Github to copy the repository and then clone your fork, like:

	``git clone https://github.com/YOUR_USER_NAME/dshng-loginhooks``

Now you can change whatever you want, commit, push to your fork and when 
your contribution is done, follow the pull request link and send us a 
request explaining what you did and why.


Links
-----

Here's the links:

`Github <https://github.com/dshng/dshng-loginhooks>`_

`Dashing Opensource <http://opensource.dashing.tv/dshng-loginhooks>`_
