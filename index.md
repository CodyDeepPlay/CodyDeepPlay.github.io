
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




## Welcome to GitHub Pages

You can use the [editor on GitHub](https://github.com/CodyDeepPlay/CodyDeepPlay.github.io/edit/master/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/CodyDeepPlay/CodyDeepPlay.github.io/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
