## documentation
https://matplotlib.org/stable/index.html
Usage Guide:https://matplotlib.org/stable/tutorials/introductory/usage.html
matplotlib.pyplot.plot: https://matplotlib.org/stable/api/_as_gen/matplotlib.pyplot.plot.html
API reference: https://matplotlib.org/stable/api/index.html

## OOP
https://matplotlib.org/stable/api/_as_gen/matplotlib.axes.Axes.plot.html
https://matplotlib.org/stable/api/axes_api.html

## NumPY
https://numpy.org/


## import
import matplotlib.pyplot as plt

## Line Graph plotting
plt.plot(x, y) --> matlab plotting

fig, as = plt.subplots()
ax.plot(x_axis, y_axis)


## Bar Graph: Vertical and horizontal
### Vertical
#### Matlab
plt.bar(x, y)
https://matplotlib.org/stable/api/_as_gen/matplotlib.pyplot.bar.html

#### Object Oriented
fig,ax = plt.subplots()
ax.bar(x, y)
https://matplotlib.org/stable/api/_as_gen/matplotlib.axes.Axes.bar.html

### Horizontal
#### MAtlab
 plt.barh(x,y, markers=".", linewidth=2, color='red')
 to switch axis, use plt.gca().invert_xaxis()

 https://matplotlib.org/stable/api/_as_gen/matplotlib.pyplot.barh.html#matplotlib.pyplot.barh
#### Object Oriented
fig,ax = plt.subplots()
ax.barh(x, y)
https://matplotlib.org/stable/gallery/lines_bars_and_markers/barh.html#sphx-glr-gallery-lines-bars-and-markers-barh-py

## Scatter Plots
### MatLab
either plt.plot(x, y, 'o') or plt.scatter()
https://matplotlib.org/stable/api/_as_gen/matplotlib.pyplot.scatter.html#matplotlib.pyplot.scatter
https://matplotlib.org/stable/gallery/shapes_and_collections/scatter.html#sphx-glr-gallery-shapes-and-collections-scatter-py

## Pie Charts
### Mat Lab
plt.pie(ValueAkaSizeOfEachPiece, label=LabelOfPieces, autopct"%1.1f%%")
add percent by using autopct="%1.1f%%"
can have one piece 'explode out using the 'explode' option
https://matplotlib.org/stable/api/_as_gen/matplotlib.pyplot.pie.html#matplotlib.pyplot.scatter

### Object Oriented Interface
fig, ax = plt.subplots(figsize=(8,8))
explode_values = (0, 0, 0.2, 0, 0, 0, 0.2, 0, 0, 0, 0, 0)
ax.pie(y_axis,
       labels=x_axis,
       colors=colors,
      autopct="%.1f%%",
      explode=explode_values,
      startangle=90,
      shadow=True)

plt.gca().invert_xaxis()

https://matplotlib.org/stable/api/_as_gen/matplotlib.axes.Axes.pie.html

###  Object oriented
fit, ax = plt.subplots()
ax.scatter(x, y)
ax.plot(x,y,'o')
https://matplotlib.org/stable/api/_as_gen/matplotlib.axes.Axes.scatter.html
https://matplotlib.org/stable/gallery/lines_bars_and_markers/scatter_with_legend.html#sphx-glr-gallery-lines-bars-and-markers-scatter-with-legend-py


## Error Bars
plt.errorbar(x,y, yerr = <value>, capsize=3, xerr=<value>
requires matplotlib.pyplot and import statistics

ax.errorbar(x_axis, y_axis, yerr=stdev, capsize=3)
https://matplotlib.org/3.1.1/api/_as_gen/matplotlib.pyplot.errorbar.html
https://matplotlib.org/3.1.1/api/_as_gen/matplotlib.axes.Axes.errorbar.html

https://matplotlib.org/stable/api/_as_gen/matplotlib.pyplot.bar.html
https://matplotlib.org/3.1.1/api/_as_gen/matplotlib.axes.Axes.bar.html




## Showing data
plt.show()
should be the last line of code as it will show the data

## Invert Axis
plt.gca().invert_yaxis()


## Label chart
plt.xlabel("x axis label")
plt.ylabel("y axis label")
plt.title("Chart title")
plt.legend()
plt.ylim(a,b): set the y axis
plt.xlim(a,b): set the x axis

## show charts in line with Jupyter
%matplotlib inline

# Matplotlib Functions	& Feature: MATLAB
plt.figure(figsize=(w, h)):	Change the size of the figure in pixels. Added on the first line of the script.
plt.plot(x, y, label='line'):	Add a label that will be added to the legend.
plt.xlim(min, max):	Set the min and max range of the x-axis.
plt.ylim(min, max):	Set the min and max range of the y-axis.
plt.xlabel('x label'):	Add a label to the x-axis.
plt.ylabel('y label'):	Add a label to the y-axis.
plt.title("Title"):	Add a title.
plt.legend():	Add a legend.
plt.grid():	Add a grid to the chart.
plt.savefig("add a path and figure extension"):	Save the figure with the given extension. Added at the end of the script.

# Matplotlib Functions	& Feature: OBJECT ORIENTED METHOD

fig, ax = plt.subplots(figsize=(w, h)):	Change the size of the figure in pixels. Add this in the subplots() function.
ax.plot(x, y, label='line'):	Add a label that will be added to the legend.
ax.set_ylim(min, max):	Sets the min and max range of the y-axis.
ax.set_xlim(min, max):	Sets the min and max range of the x-axis.
ax.set_xlabel('x label'):	Add a label to the x-axis.
ax.set_ylabel('y label'):	Add a label to the y-axis.
ax.set_title("Title"):	Add a title.
ax.legend():	Add a legend.
ax.grid():	Add a grid to the chart.
** plt.savefig("add a path and figure extension"):	Saves the figure with the given extension. Added at the end of your script.

## Add Ticks
### Major
ax.set_xticks, or ax.xasix.set_ticks()
ax.set_yticks, or ax.yaxis.set_ticks()

### Minor
set_minor_locator: ax.xaxis.set_minor_locator(MultipleLocator(<how often we want minor ticks>))


## Box & Whisker plots
ax.boxplot()
      must have the fix, ax = plt.subplots() before
 https://matplotlib.org/2.0.2/examples/statistics/boxplot_demo.html     


## change all the font types
import matplotlib as mpl
rcParams['font.size']=14
https://matplotlib.org/stable/tutorials/introductory/customizing.html

## magic commands, use with %matplotlib 
'inline'
'GTK3Agg'
'GTK3Cairo'
'MacOSX'
'nbAgg'
'Qt4Agg'
'Qt4Cairo'
'Qt5Agg'
'Qt5Cairo'
'TkAgg'
'TkCairo'
'WebAgg'
'WX'
'WXAgg'
'WXCairo'
'Agg'
'Cairo'
'Pdf'
'Pgf'
'Ps'
'Svg'
'template'