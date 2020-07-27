
I am using anaconda to launch spyder.
Matplotlib not working, freeze figure, crash kernel if I am trying to close the figure.


Below are some figures to show the problem:

![figure freeze](https://github.com/CodyDeepPlay/CodyDeepPlay.github.io/blob/master/freeze_figure.PNG)

![close figure dialogue](https://github.com/CodyDeepPlay/CodyDeepPlay.github.io/blob/master/try_to_close_figure.PNG)


using matplotlib.get_backend() to view current backend being using by Matplotlib.
![view matplot backend](https://github.com/CodyDeepPlay/CodyDeepPlay.github.io/blob/master/face_recog_TKAGGPNG.PNG)

Then, I figured it out, using 'TkAgg' is not working, so need to change to backend 'Qt5Agg'. Don't know why. 
```
import matplotlib
matplotlib.use('Qt5Agg') # change back end
```

Make sure you installed PyQt5 module, otherwise you will have errors.
