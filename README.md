createpreview
=============

Create an EPUB Preview file based on EPUB file (according to IDPF Previews standard: http://www.idpf.org/epub/previews/)

A preview EPUB is similar to original file but with only few chapters.
This utility essentially cut out several content file leaving only a given number of content files.

Version: 1.0
License: GPL v. 3

Usage: createpreview [options] <ebubfile> <num>

epubfile - the original file name
num - number of content files (chapters) to keep, note this number includes the cover.

Options:
-o <outputfile> - Set output file name (default overwrite original)
-a <acqlink> - Set acquisition link for original file
--catalog <catalog> - Set link to OPDS catalog containing the original file
-i <identifier> - Set new identifier for file
--identifier <identifier> - Same as -s

Written in perl, using the following non core CPAN modules:
* XML::Parse
* DateTime

It currently uses system() call for unzip and zip so unzip and zip must be installed on system.
This was written and tested on Linux system. It may not work on other OS.



