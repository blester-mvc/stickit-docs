---
sidebar_position: 6
---

# Fixed Sequence Macro

When it is necessary for each label to include a reference to the total number of labels printed and the sequence starts at a number other than 1 or a custom separator is desired.
Example: `3/5`, `4/5`, `5/5`  

To add a fixed sequence macro, follow these steps:

1. Add a new **text** element to the label template.

1. Type the desired start **number** into the text box.

1. Right click on the text box and click the **Select >** button.

1. Make note of the selected object **name**. Ex. `ITextObject1`

1. Click the **OK** button.

1. Add a new **text** element to the label template.

1. Type the desired **separator** into the text box.

1. Add a new **text** element to the label template.

1. Type the desired end **number** into the text box.

1. Right click on the text box and click the **Select >** button.

1. Make note of the selected object **name**. Ex. `ITextObject2`

1. Click the **OK** button.

1. Click the **Save** button.

1. Go to the **folder** where you saved the label template.

1. Right click on the file select **Open With** and choose:
    - Windows: `Notepad`
    - MacOS: `TextEdit`  
      OR
    - Any text editor of your choosing

1. Find and Replace the object names noted above with `START_POS` and `END_POS` respectively.

1. **Save** the file.
