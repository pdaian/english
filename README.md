# A distributed approach to a Bitcoin wiki

This repository contains the collected knowledge about Bitcoin in a
wiki-style markup which are the sources to a beautiful site of all people
need to know about Bitcoin, the community and all the features and its
history.

This is currently a work-in-progress.

# How would this work?

A wiki is almost always centralized because people like editing in a web-browser
and committing to that central server.  
Using a wiki-engine called [ikiwiki](http://ikiwiki.info/) this same model
can still be used but instead of committing to a SQL database like for
instance wikipedia does, it commits to a git repository.

The idea is that people can edit the wiki on a website and push the changes
to github. This way everyone can clone the repository and set up their own
wiki site.  Using merge requests different sites can merge their users
work. This would also allow individuals more comfortable with different
editing tools from contributing like it were any open source project.

Distributed in this case means that no one person or group can succeed in
censoring content. If a certain place turns out to be too restrictive in
their policies, better content will appear on another one.


# How to actually see the pages?

Ikiwiki is a simple tool that you can apt-get install on ubuntu / debian,
other systems will likely package it as well.

The tool takes the this repository and uses <code>bitcoin.setup</code> file
to generate a new directory with all the html files.  The output is a
purely static site for browsing and it generates a cgi-bin executable that
when the webserver is configured to allow it to run it will enable logged
in users to edit pages. Just like any other wiki.

If you just want a mirror, for instance at home, you can just create a
website like this;

	cd wiki-en
	ikiwiki --setup bitcoin.setup

