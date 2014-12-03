Merge Errors
============

First try to google the error messages and see if any of the results help in your situation.

The .meteor directory usually gets messed up during a merge.  So what I do is look at the .meteor/package of the repo I am merging into my repo.
Then I add or remove whatever packages I need.  First I check what packages I have installed:
    meteor list

Then I add package:
    meteor add iron:router

Or remove packages I don't need:
    meteor remove iron:router@0.9.3

