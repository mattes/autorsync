autorsync
=========

Watch directories for changes and update remote directories with [rsync](http://www.samba.org/ftp/rsync/rsync.html). Directories are monitored with [fs.watch](http://nodejs.org/api/fs.html#fs_fs_watch_filename_options_listener) from [Node.js](http://nodejs.org).

rsync is a file transfer program for Unix systems. rsync uses the 'rsync algorithm' which provides a very fast method for bringing remote files into sync. rsync works unidirectional. If you are looking for a two-way-sync have a look at [unison](http://www.cis.upenn.edu/~bcpierce/unison/). autorsync could easily be ported to be used with unison. 

Prerequisites
-------------
 * Linux or Mac OS
 * [Node.js](http://nodejs.org)
 * [rsync](http://www.samba.org/ftp/rsync/rsync.html)

 Recommended: Update rsync to the latest version on Mac OS. [Tutorial](https://gist.github.com/3990176)

Usage
-----

    autorsync [option]... source user@host[:port] destination

    Options:
      --exclude=filepath    path to "exclude from sync file" relative to source or absolute
      --sync-delay=n        wait for sync to happen
      --sync-verbose=bool   print more details about sync
      --sync-simulate=bool  simulate sync and print details about sync

Example
-------

    ./autorsync --exclude=.rsync_ignore ~/watched_directory peter@example.com in_sync

License
-------
Copyright 2012 Matthias Kadenbach  
Released under the MIT license