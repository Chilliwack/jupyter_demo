# Jupyter Notebook for the Busy Scientist

A quick demonstration. Some curious scientific programmers
wait a long-time before trying a modern IDE.
Here are some reasons to take a look at Jupyter.

## Preliminaries

**First**, it's good to know there's two distinct and different products associated with Jupyter. The earliest and first product developed by the Jupyter team is called [Jupyter Notebook](https://jupyter-notebook-beginner-guide.readthedocs.io/en/latest/what_is_jupyter.html). This is the one you will see discussed the most when surfing the web. The second and latest product developed by the Jupyter team and the one we'll discuss in further detail below is [JupyterLab](https://jupyterlab.readthedocs.io/en/latest/). So let's get started with JupyterLab!

1. [Install JupyterLab](https://jupyterlab.readthedocs.io/en/latest/getting_started/installation.html) 
2. Be default JupyterLab installs python but to install all the other cools stuff you'll need to:
   - Linter such as [flake8](https://github.com/mlshapiro/jupyterlab-flake8) 
   - [R kernel](https://richpauloo.github.io/2018-05-16-Installing-the-R-kernel-in-Jupyter-Lab/) so you can run R in Jupyter Lab
   

## Shortcuts for Mac

* ⌘ is the Command () key.
* ⌃ is the Control key.
* ⌥ is the Option (alt) key.
* ⇧ is the Shift key.
* ⇪ is the Caps Lock key.

## 1. Keyboard Shortcuts Aren't just for Emacs

### Select Panes with ⌘1,⌘2, ... #n

If n is greater than the number of open panes, this will create a new pane.

### Select Tabs within Panes with ⌃1,⌃2, ... ⌃n

Get to the 2nd tab in the leftmost pane [⌘1], then [⌃2].

### Select Explorer Pane with ⌘0

Once you are in the explorer you can use up and down keys to select files.

### Reveal File Paths Instantly

Click on the file panel Use the keyboard shortcut [⌥⌘C], and bam!, the full path is copied to your clipboard (e.g., `/Users/kmayerbl/active/demo_vsc/README.md`)

### Reveal Paths with Clicks

Instantly get to where your code lives on your machine. Save time by right-clicking on a folder or file, and select [Reveal in Finder] or [Open in Terminal]. Need the path just click [Copy Path].

### Save one or Save all by Group

Take a look at the icon on the browser panel. You can, with one-click, save all the files or all the files in a group.

## 2. Preview your README.md

VSC offers a live rendering of your markdown. To view it, right-click on your markdown file and select [Open Preview].

## 3. Run Script or Only Part of Script With ⌃⌥N

You can run a segment of a script by selecting the part you care about and hitting [⌃⌥N]. The results show up in the OUTPUT table.

## 4. Problems and Quick Their Quick Fixes

Linters help you find problems quickly. These are reported in the Problems tab of the  Here are two examples. 

* No-trailing-spaces (see one line above)
* No-bare URLs (see in the first block)

Get to the problems quickly with this shortcut [⇧⌘ M].

![Problems and Their Fixes](https://user-images.githubusercontent.com/46639063/75186808-8c5f6c80-56fd-11ea-91c3-1d09b401b734.png)

Here you can see tests that are failing, and "lint" that's piling up in your code. One of the things, I like about VSCode is that
you can auto-correct simple problems like those above without even having to search through the code.

## 5. Debugging

When we run python hi.py we see an error. Suppose we want to see where that error emerges.

```bash
Traceback (most recent call last):
  File "greetings/hi.py", line 51, in <module>
    assert sentance_case_to_be_degbugged("Camel") == "Camel"
AssertionError
```

* Breakpoints fn + F9, or using the mouse by clicking in the left margin in the editor.
* Click the Bug with the play icon
* We can start at the source of the error and move inwards

The breakpoint is placed on line 51 at the source of the error:

![error1](https://user-images.githubusercontent.com/46639063/75187868-d9444280-56ff-11ea-9893-e2a2fa064875.png)

"Step Into" the error (that is, go to the function being called) by clicking on the downward blue arrow.
Then, step line by line through the problematic function and check whether state of all variables meet your expectations.

![error2 1](https://user-images.githubusercontent.com/46639063/75188401-edd50a80-5700-11ea-9836-9d400300510d.png)

* More: <https://code.visualstudio.com/docs/python/debugging>

## 6. Work on a Specific Unit Test

A great thing about VSCode is how it organizes your test. You can even run them one by one.

![tests](https://user-images.githubusercontent.com/46639063/75184229-ea3d8580-56f8-11ea-83d3-1ee87fec849c.png)

Also here is an easter egg if you like doctests:

```bash
pytest --doctest-modules -v
```

## 7. Peak Function is Some Serious Magic Beans

 Sometimes you don't want to search for where a variable or function is defined. VSCode has a peak function that let's examine externally referenced objects, and even edit them, directly from where an object is referenced. Let's look at what the French hello should be:

![peak](https://user-images.githubusercontent.com/46639063/75184186-d98d0f80-56f8-11ea-8e67-cd76626992f0.png)

## 8. Look at a Merge Conflict

Let's look at resolving a merge conflict. A merge conflict often arises when two users commit changes to the same file. For instance, on GitHub, I wrote:

```bash
I think we should think global!
```

But on my laptop, I wrote:

```bash
I think we should start local!
```

When I tried to, push the second commit, my push was rejected:

![Fail to Push](https://user-images.githubusercontent.com/46639063/75186423-b5333200-56fc-11ea-93e8-1aae785bc57c.png)

So I pulled the version on GitHub that was one commit ahead, revealing a conflict without an auto-resolution. Git cannot merge two versions of the same file, if they have different content on the same line! How would git know which was correct?

![Merge Conlict](https://user-images.githubusercontent.com/46639063/75185762-810b4180-56fb-11ea-810d-2560939496be.png)

Fortunately, VSCode makes it easy to review the confict and pick the winner (or keep both, by appending a version as new lines of code).

![Resolve Merge Conflict](https://user-images.githubusercontent.com/46639063/75185767-82d50500-56fb-11ea-8da1-4d32fddabe7c.png)

After resolving the conflict, remember to commit and push the resolution.

## 9. settings.json

JSON file with all your user-specific settings. How to get to it? (see the common settings wheel at the lower left)

![where is settngs dot json](https://user-images.githubusercontent.com/46639063/75194760-9ab58480-570d-11ea-95ed-d44fd5805197.png)
≈

### the .code-workspace file

These apply to your specific workspace (project specific)?

## 10. Switch effortlessly between environments


## Conclusions

I am sure there are a ton of other great stuff one can do with Visual Studio Code.
Hopefully, this tutorial has heightened your interest.
