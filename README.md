CairoPlot Install (windows - python 2.7 32bit):

	The official install docs:  http://cairoplot.sourceforge.net/tutorials.html
	
	What I needed to do:
	
		Copy cairoplot.py and series.py to <YourPythonRoot>/Lib
	
Dependancies (windows - python 2.7 32bit):
	
	zlib 
		1. dowonload zlib http://www.gtk.org/download/win32.php 
		2. copy the zlib directory to <YourPythonRoot>/Lib
		3. rename the directory to 'zlib'
		4. test the module in the python console with 'import zlib'
	
	Cairo (the easy way)
		1. download the PyGTK All in One installer and run it:  http://ftp.gnome.org/pub/GNOME/binaries/win32/pygtk/2.24/
	

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
  

  

