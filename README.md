# ipyfilechooser

A simple Python file chooser widget for use in Jupyter/IPython in conjunction with ipywidgets. The selected path and file are available via `.selected_path` and `.selected_filename` respectvely or as a single combined filepath via `selected`. The dialog can be reset to its default path and filename by using `.reset()`. 

If a filename is typed in the filename text field that matches a file entry in the current folder the entry will be highlighted. To highlight the risk of overwriting existing files, the selected filepath will be green if the file does not exist and orange if it does.

## Usage

```
from ipyfilechooser import FileChooser

# Create and display a FileChooser widget
fc = FileChooser('/Users/crahan/Projects/Jupyter/ipywidgets')
display(fc)

# Print the selected path, filename, or both
print(fc.selected_path)
print(fc.selected_filename)
print(fc.selected)

# Change defaults and reset
fc.default_path = '/Users/crahan/Projects'
fc.default_filename = 'output.txt'
fc.reset()

# Shorthand reset
fc.reset(path='/Users/crahan/Projects', filename='output.txt')
```

## Functions and variables

```
fc.reset()
fc.default
fc.default_path
fc.default_filepath
fc.selected
fc.selected_path
fc.selected_filename
```

## Screenshots

![Screenshot 1](screenshots/FileChooser_screenshot_1.png)
*Fig. 1: FileChooser default view*

![Screenshot 2](screenshots/FileChooser_screenshot_2.png)
*Fig. 2: FileChooser open view*

![Screenshot 3](screenshots/FileChooser_screenshot_3.png)
*Fig. 3: Entering a filename for an existing file*

![Screenshot 4](screenshots/FileChooser_screenshot_4.png)
*Fig. 4: Existing file selected*

![Screenshot 5](screenshots/FileChooser_screenshot_5.png)
*Fig. 4: Entering a filename for a new file*

![Screenshot 6](screenshots/FileChooser_screenshot_6.png)
*Fig. 5: New file selected*

![Screenshot 7](screenshots/FileChooser_screenshot_7.png)
*Fig. 5: Quick navigation dropdown*