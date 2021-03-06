qdupe
=====

A command-line utility to quickly find duplicate files, written in Python and inspired by [FastDup](http://sourceforge.net/projects/fastdup/)

Installation
------------

    $ [sudo] pip install qdupe

Usage
-----

    $ qdupe path [path..]

How It Works
------------

Initially, qdupe scans all the files in the path(s) you specify and groups them by size. Then, for each file of a given size, the first 4kb are compared. This quickly excludes obvious non-matches. If the first 4kb of the files are equivalent, the remaining bytes of the files will then be compared. The size, MD5 hash, and paths will be reported for all duplicates found, followed by a summary.
