Goal for this branch:

	The goal is to allow custom formatting of bar chart labels.  For example, adding % to a the label above each bar. Michael Rooney has achieved this on a previous version of Cairoplot but the changes where never merged with the master branch. This fork will attempt to incorporate the changes made by Michael Rooney.  Specifically this includes the changes in revision 47, 48, 49, and 50 of this branch: https://code.launchpad.net/~mrooney/cairoplot/label-formatters

About Cairoplot:

	CairoPlot is a Python based charting library created and maintained by Rodrigo Ara�jo (https://github.com/rodrigoaraujo01).  


Status:

As of May 2, 2013 all changes have been incorporated. 

As of May 23, 2013 the equivilent changes have been applied to horizontal bar charts.  

Light testing proved the improvements functional for vertical and horizontal bar charts!

HOWEVER, tests on some dot line plots and all scatter plots failed the tests.py script found in trunk. 
  * See test.py in trunk for details.
