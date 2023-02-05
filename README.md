![DKN4.Hackers](assets/dkn5.jpg)

# Remove background from Images using Python

You will need to install the [Python](python.org) packages using pip.

1. Open a Command Prompt and install rembg. Press Enter to start the process.

    `pip install rembg`

2. Install easygui using pip. Easygui provides a basic user interface for file open and save operations.

    `pip install easygui`

### Writing the Code
The code is essentially very simple, with just eight lines of Python we can remove the background from any image. The underlying modules, rembg and easygui will be doing all of the heavy lifting for us.

1. From the rembg module import the remove class. This is what we shall use to remove the background.

    `from rembg import remove`

2. From the Python Imaging Library (PIL), import Image. PIL is a powerful module that contains many different options for creating and working with images and image streams.

    `from PIL import Image`

3. Import the easygui module and create a reference to it as “eg”. Easygui is our GUI for basic file operations. Renaming it to “eg” makes it easier to work with.

    `import easygui as eg`

4. Create an object, input_path and use it to store the path and name of a file that we wish to remove the background from. Using easygui’s file open dialog box, we give the dialog a title, to explain what it is for. The chosen file and its path are stored to the input_path object.

    `input_path = eg.fileopenbox(title='Select image file')`

5. Create an object, output_path and use easygui’s file save dialog box to capture the file path and save it to the object.

    `output_path = eg.filesavebox(title='Save file to..')`

6. Create an object, input and use it to open and store the image via PIL’s Image.open function.

    `input = Image.open(input_path)`

7. Use rembg to remove the background from the image.

    `output = remove(input)`

8. Save the new image using the file path stored in output_path.

    `output.save(output_path)`




Hey Guys,

   I am pretty new to writing on Medium and would love to hear your feedback. If you like what I am writing about, don’t hesitate to put a thumb up or leave a tip. Please feel free to leave a comment if you have a question or recommendation. I read every message and try to answer as soon as I can.

[Abdellah Aarab](https://abdellahaarab.github.io/)
