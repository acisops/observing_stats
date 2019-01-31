The files in this directory are intended to extract statistics on
the observing program from the obscat, and compute percentages of
time and proposals selected in various ways in the various instrument
configurations (ACIS-I, ACIS-S, HRC-I, HRC-S; and HETG, LETG, NONE).

Here's what you do:

[1] Copy the files in this directory into a new directory labeled with the
date. Edit the list of AO periods at the top (it's in there twice, in
ascending and descending order; edit both).

If you need to alter what cases are run, edit the cases.rdb file, and
the *text.html files to say what you did for each. Create new *text files
as needed, but be sure the lists in the foreach() statements and copies
at the end in the script cover if new ones are added.

[2] Run the script make_stats.csh. You will need to give your archive username
and password at the beginning.

[3] The script tars up the resulting web pages and copies them to
the ACIS temporary web space. If you expand them there, you can see
the pages in a path like this one:

http://cxc.harvard.edu/acis/tmp/observing_stats/

This script makes extensive use of the RDB tools provided by Diab Jerius.

There's a second script, make_drop_stats.csh, which makes a table of
chip-drop statistics.


