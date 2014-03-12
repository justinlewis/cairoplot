Instalation:
	Copy cairoplot.py and series.py to <YourPythonRoot>/Lib


Goal for this branch:

	The goal is to allow custom formatting of bar chart labels.  For example, adding % to a the label 
	above each bar. Michael Rooney has achieved this on a previous version of Cairoplot but the changes 
	where never merged with the master branch. This fork will attempt to incorporate the changes made by 
	Michael Rooney.  Specifically this includes the changes in revision 47, 48, 49, and 50 of this 
	branch: https://code.launchpad.net/~mrooney/cairoplot/label-formatters
	
	The more I use CairoPlot the more I seem to make modifications to the library.  This branch has had
	numersous small modifications to it.  Please review the revision history if needed.

About Cairoplot:

	CairoPlot is a Python based charting library created and maintained by Rodrigo Araujo 
	(https://github.com/rodrigoaraujo01).  

Important Notes:

	Support for Python >= 2.7 OrderedDict() data type was added requiring the collections module to be 
	imported. Add "from collections import OrderedDict" to your script.
		* This is useful if you want to maintain the same color for each wedge in a pie plot while
		inputing a dictionary for many output files. The order of the dictionary elements is important
		to maintain consistency in wedge color accross different output charts.
		
	Added support for negative values on vertical bar plots (warning: hackish and probably buggy):


![alt tag](/examples/neg_value_vertical_bar_example.png)


Status:

As of May 2, 2013 all changes have been incorporated. 

As of May 23, 2013 the equivilent changes have been applied to horizontal bar charts.  

Light testing proved the improvements functional for vertical and horizontal bar charts!

HOWEVER, tests on some dot line plots and all scatter plots failed the tests.py script found in trunk. 
  * See test.py in trunk for details.
  

  

