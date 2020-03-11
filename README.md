# Jupyter Notebook for the Busy Scientist

A quick demonstration. Some curious scientific programmers wait a long-time before trying a modern IDE. Here are some reasons to take a look at Jupyter, a linearly executed IDE, with come caveats.

## Preliminaries

**First**, it's good to know there's two distinct products associated with Jupyter. The earliest and first product developed by the Jupyter team is called [Jupyter Notebook](https://jupyter-notebook-beginner-guide.readthedocs.io/en/latest/what_is_jupyter.html). This is the one you will see discussed and screenshoted the most when surfing the web. The second and latest product developed by the Jupyter team and the one we'll discuss in further detail below is [JupyterLab](https://jupyterlab.readthedocs.io/en/latest/). 

![](https://jupyterlab.readthedocs.io/en/stable/_images/interface_jupyterlab.png)

So let's get started with JupyterLab, oh and I'll just say at the top that I do not think JupyterLab can currently replace a more engineering focused IDE application like Atom, VSCode or PyCharm but it is heading in that direction with its extensions and it does presently make a very good light-weight, browser-based analytical tool for teaching, data wrangling, modeling, scripting, cloud computing and various other analytic needs outside of engineering.

1. First let's [install JupyterLab](https://jupyterlab.readthedocs.io/en/latest/getting_started/installation.html). The latest version is 2.0.1 and that's important because some of the add-ons and extensions may not work with this or other versions.
2. By default JupyterLab installs python but to install all the other cools stuff* you'll need:
   - A linter such as [flake8](https://github.com/mlshapiro/jupyterlab-flake8) 
   - A [debugger](https://github.com/jupyterlab/debugger)
   - [Github integration](https://github.com/jupyterlab/jupyterlab-git)
   - The [variable inspector](https://github.com/lckr/jupyterlab-variableInspector)
   - And for those that use R as well there's an [R kernel](https://richpauloo.github.io/2018-05-16-Installing-the-R-kernel-in-Jupyter-Lab/) so you can run R in JupyterLab. That's nice.


   *Caveat here - some of these extensions/add-on are not as frequently updated as the core JupyterLab product and may not be available with the latest version of JupyterLab so be mindful when installing them. 

## Shortcuts for Mac

* ⌘ is the Command () key.
* ⌃ is the Control key.
* ⌥ is the Option (alt) key.
* ⇧ is the Shift key.
* ⇪ is the Caps Lock key.

## 1. Keyboard Shortcuts 

### Jupyterlab 

The shortcuts I use most when operating in Jupyterlab are the following:

* Shift + Return - will run the cell selected
* Return - will allow you to enter into the cell to edit the code
* Esc - while escape will take you out of the cell while keeping it selected. You can then use the arrow keys to navigate down to another cell or..
* A - hitting `A` after hitting Esc so you are no longer in a cell will create a new cell above where you are now
* B - `B`  will create a cell below the one you are in now and..
* DD - hitting `D` twice will delete the cell selected
* M - hitting `M` when a cell is selected will turn that cell from a code to a markdown cell
* Y - `Y` will turn the markdown cell back into a coded one
* R - `R` will turn the cell into a raw format

It also auto-saves checkpoints so I don't worry too much about saving but use ⌘+S for good measures every now and again. Jupyterlab also has a text editor which has keyboard maps to popular text editors like vim, emacs or Sublime Text which you can select and edit under Settings. And if you just need a cheat sheet [BOOM!](https://blog.ja-ke.tech/assets/jupyterlab-shortcuts/Shortcuts.png)

![](https://miro.medium.com/max/2640/1*O20XGvUOTLoFKQ9o20usIA.png)

## 2. Preview your README.md

Jupyterlab offers live rendering of your markdown. To set it up, locate the markdown file you want to edit in Jupyter's file browser; right-click on the markdown file and select Open With > Markdown Preview. This will open up the file as a rendered markdown. You can then double-click on the same file again in the explorer and it'll open in Jupyter's Text Editor at which point you can grab and move/split the tabs to your preference for live editing of markdown.

## 3. Run Script or Only Part of Script With ~~⌃⌥N~~

~~You can run a segment of a script by selecting the part you care about and hitting [⌃⌥N]. The results show up in the OUTPUT table.~~ Take the segment of code you want to run and drop it into a new cell and Shift+Return. Seems manual but this ability to take parts of code and iterate and interact with them by dropping them into a new cell to run is what some find beatiful about Jupyter. It is like an inline console which speaking of if you want to create a new console just select File > New and you can create a new console, or a new notebook (in either a python, R, Julia or other kernel), a terminal instance, a new text file, or a markdown.

## 4. Problems and Their Quick Fixes

Linters help you find problems quickly and [this guy](https://github.com/mlshapiro/jupyterlab-flake8) built a good one based on the flake8 python library for linting. The only problem is that currently it doesn't work with JupyterLab 2.0 yet that doesn't mean it won't in the future ; )

![](https://raw.githubusercontent.com/mlshapiro/jupyterlab-flake8/master/img/example.png)
![](https://github.com/mlshapiro/jupyterlab-flake8/raw/master/img/editor-example.png)

## 5. Debugging

So having a debugger in your IDE that you can insert breakpoints, step in, cycle thru your lines, and step out is nice. Once again we have a [great extension here](https://github.com/jupyterlab/debugger) that provides that in Jupyterlab. Unfortunately, after many attempts at getting the debugger switch to show up in the UI and then trying to get it to operate I had to give up on it but in version 1 it worked as a good debugger should so hopefully this will be operating smoothly in Jupyterlab 2.0 soon.

![](https://github.com/jupyterlab/debugger/blob/master/screencast.gif)

## 6. Work on a Specific Unit Test

No cool unit testing integration or UI here folks :( but there is an extension that allows [cell-by-cell testing](https://github.com/timkpaine/jupyterlab_celltests) if you want to roll that into your testing setup.

## 7. ~~Peak Function is~~ Some Serious Magic Beans

Ok, so the "magic beans" here with Jupyterlab is that you have a very light and functional, once all the extensions are updated to play nicely with Jupyterlab 2.0, web-based IDE which outside of hard core engineering can be of use to you especially with the rise of cloud-computing and oh it has a dark theme now Settings > JupyterLab Theme.

![](https://github.com/telamonian/theme-darcula/blob/master/darcula_preview.png)

## 8. Git extension for JupyterLab

"There's an extension for that"[...seriously!](https://github.com/jupyterlab/jupyterlab-git) Yet, it's not as nice as the github integration for VSCode or PyCharm but then again JupyterLab is new and the extensions I believe are community-driven so they haven't had the time or resources to flush it out like the others may have. There's also one specifically for [diffing and merging of notebooks](https://github.com/jupyter/nbdime).

![](https://github.com/jupyterlab/jupyterlab-github/blob/master/gitception.png)

## 9. Settings

You can set system and all your user-specific settings by going to Settings > Advance Setting Editor.

### 10. the .ipynb file

This IS the ipython notebook file or your JupyterLab file with code and markdown in it and note you can only access these from the directory you execute `jupyterlab` in so either `pwd` to make sure or have a set location of where you save the files because you'll only be able to open .ipynb files in either the start-up directory or it's sub-folders. 

## Conclusions

Jupyterlab built upon the success of Jupyter notebook as a light-weight, browser based linearly executed IDE, but now has an updated front-end making it seem more similar to RStudio and Spyder. It comes with a much quicker backend running in your browser than Jupyter notebook and with the help of some extensions which you can theoretically load by enabling the Extension Manager in Settings you can add linting, debugging, version control and many more [(fasta render anyone?)](https://github.com/jupyterlab/jupyter-renderers).

![](https://camo.githubusercontent.com/6aa00b126595f41bc5bee84a6696234b63036fda/687474703a2f2f672e7265636f726469742e636f2f74656d697a6a616539582e676966)

The downside though is that version 2 was a major release for them and they are now at 2.0.1 which was released in March 6, 2020 so the project is very new which means the extensions which add a lot of features to flush out the product also need to stay update-to-date with the current code base but that can create problems. There's guides for that, ["JupyterLab 1.x to 2.x Extension Migration Guide"](https://jupyterlab.readthedocs.io/en/stable/developer/extension_migration.html), but it'll be great when everything is playing nice and you have a powerful browser-based, light-weight IDE at your finger tips.

Let's hope the synergy of the versioning of the core product and the community of extensions improves. Until then there's nothing stopping a python or R user from doing all their engineering in Atom, PyCharm, RStudio, or VSCode and then the rest of their coding/management in Jupyterlab since it _is_ browser-based. Hopefully, this tutorial has heightened your interest.
