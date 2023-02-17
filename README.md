# plotdigitizer-binder
Python-based [PlotDigitizer](https://github.com/dilawar/PlotDigitizer) working 'headless' in sessions served via MyBInder.org

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/fomightez/plotdigitizer-binder/HEAD)

-----

To try click on the 'launch binder' badge above.  
When the session comes up, select an available notebook and open and run it.

Currently the `Testing_plotdigitizer.ipynb` notebook will step through the examples posted in [PlotDigitizer README](https://github.com/dilawar/PlotDigitizer#readme).


-------

### Option to go elsewhere to use a GUI for selecting points

Want to work with spawned windows via Qt to select points? Go to [plotdigitizer-binderDesktop](https://github.com/fomightez/plotdigitizer-binderDesktop), and press 'launch binder'. From there a Desktop interface will spin up where the necessary packages and dependencies for `plotdigitizer` to work are installed.  
There, click on the desktop icon to open Spyder.  
You can use the IPython console in the bottom left to run:

```python
!git clone https://github.com/dilawar/PlotDigitizer.git
%cd PlotDigitizer
```

And then to use the locator tool, run the following as advised at ['How to find coordinates of axes points' in the PlotDigitizer documentation](https://github.com/dilawar/PlotDigitizer/tree/master#how-to-find-coordinates-of-axes-points):

```python
!plotdigitizer-locate figures/trimmed
```

It will open a window as described where you can click and get the coordinates as big text on the image itself.  
You can also run commands like the typical one and leave off the coordinates, like this example below, to get a window spawned where you step through picking the coordinates:

```python
!plotdigitizer ./figures/trimmed.png -p 0,0 -p 40,0 -p 0,3
```

However, I found the interface to be too rough. It may be because it is running in a desktop in the browser; however, I'm not certain that is it as the locator tool works fine in the same situation.

Also, note that copying the URL of the session to a new window and removing the `desktop` and the end will let you access JupyterLab where you can add things and work in a notebook. (Sadly, the notebook cannot spawn Qt. Stay in Spyder in the desktop for that.) **Importantly**, the notebook(s) that work here will work there is placed inside the root of the cloned repo.

------------