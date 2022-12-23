---
sidebar_position: 3
sidebar_label: 'Sequence'
---

# Sequence Macro

When it is necessary for each label to include a reference to the total number of labels printed.  
Example: `1 of 2`, `2 of 2`  

To add a sequence macro, follow these steps:

1. Add a new **text** element to the label template.

1. Type `x of y` field into the text box.

1. Right click on the text box and click the **Select >** button.

1. Make note of the selected object **name**. Ex. `ITextObject1`

1. Click the **OK** button.

1. Click the **Save** button.

1. Go to the **folder** where you saved the label template.

1. Right click on the file select **Open With** and choose:
    - Windows: `Notepad`
    - MacOS: `TextEdit`  
      OR
    - Any text editor of your choosing

1. Find and Replace the object name noted above with `LABEL_NUMBER`.

1. **Save** the file.