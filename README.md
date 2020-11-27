# Info
By Kyle Heffernan, Eoin Gallagher and Ryan Byrne
For Computer Science Infrastructure 4th year module Image Processing in TU Dublin.

# CardGameAssistant-ImageProcessing
This program reads in a hand of 5 cards and determines the value of each card.

* Idea
When learning poker many people have trouble understanding the poker hands and their ranks[1]. Our program aims at making this process easier for new players where they just take an image of their takes and the program will tell them what poker hand they have. 


# Requirements
    Tesseract OCR
    pytesseract

### These steps will give you a rundown of how to install the above packages

#### if you are using anaconda then these are the steps for installation

* first open anaconda
* once anaconda is running look for program titled `CMD.exe Prompt` it has a picture of the anaconda logo above
* once located click this program and enter the following commands
  * `conda install -c conda-forge pytesseract`
  * `conda install -c conda-forge/label/cf202003 pytesseract`
  * TesseractOCR needs to be downloaded from: [https://github.com/UB-Mannheim/tesseract/wiki] the steps for installation are below:
    * When selecting components to install you do not need to click anything extra you can leave them checked with the default ones, then click next.
    * The next step is to choose to install Location you should leave this as is.
   * This should have successfully installed the necessary libraries in order to run our project

#### If you are using python without anaconda you should be able to install with this

* Prerequisites before you install pytesseract:
  * `pip install pillow`
  * `pip install matplotlib`
  * `pip install opencv-python`
  * `pip install easygui`
  * TesseractOCR needs to be downloaded from: [https://github.com/UB-Mannheim/tesseract/wiki] the steps for installation are below:
    * When selecting components to install you do not need to click anything extra you can leave them checked with the default ones, then click next.
    * The next step is to choose to install Location you can leave this as is copy this location as it will be used later, then click next until the install is finished.
    * Once finished you then need to add tesseract to your enviroment variables this is done through the following steps:
      * go to your windows search bar and type in `edit the system environment variables` and hit enter.
      * then click the `environment variables` option.
      * then click on `PATH`.
      * then click on `Edit...`.
      * then when your in the edit environment variable screen click `New`.
      * In the highlighted area that appeared paste the path you copied earlier from the TessarctOCR install if you havent copied it the default location is `C:\Program Files\Tesseract-OCR\tesseract`.
      * to verify the install open CMD and type `tesseract`.
  * once the above steps have been taken you can proceed to install pytesseract using the following command:
    * `pip install pytesseract`

# Instructions
* With tesseract set up, run all cells in the notebook. 
* There will be a file open box allowing you to pick any of the sample card hands. 
* Select one of the files in the base project folder.
* The program will display the value of all the cards in the chosen image and output what poker hand the user has.

# Assumptions
* This program assumes the user will use an input image of five playing cards taken from above the cards.
* The background will be darker than the cards themselves.
* The image will be of high enough quality to decypher symbols.
* The image will be clear and not blurry.
* There are no other large object in the image other than the cards.

# Basic structure
* The program will take in the file then isolate each cards and warp it to match a vertical rectangle box
* It will then crop the sections it needs for detecting letter and symbol
* It will get the card type using the letter section
* It will get the card symbol using the symbol section
* It will use all the types and symbols to check what hand the user has


# Algorithm steps:
* This Program starts off by allowing to choose a picture card of their hand of 5 cards that they want analysis on
* It then calls the function `readCards()` takes in the user inputted image and performs all necessary operatioins on the image.
* The image is converted to greyscale and then to binary format.
* With this binary mask the contours are found and sorted by size
* the program then proceeds to call the function `warpPerspective()` and
* It then 
* Suit comparison takes in the cropped symbol image and compares it against the four sample suits. It returns the suit with the smallest difference.
* Next, 
* After this,
* It then 
* Next 
* Finally,


# Performance
* The algorithm takes a very small amount of time to run.
* The program is mostly accurate and is perfect for all the different poker hand images in the project folder, but accuracy depends on the image, so if the user wants to test an image from far away, with very bad lighting, or a bad background the accuracy may faulter. 
* The algorithm should work for a range of card brands if they are spaced out properly but this may vary greatly.
* An effort to increase performance has been made such as only having neccessary things within loops and breaking out of statements if the condition is met.


# Underlying concepts & Research:
* Thresholding: This selects certain parts of a grayscale image based on a threshold value allowing the user to separate objects.
* Masking: This selects certain parts of an image based on a binary mask.
* Contours: This finds continuous points on a shape and can be used for object detection.
* fillPoly: This fills in an area specified by the parameters.
* GaussianBlur: This blurs the pixels to make the images better fro detection and thresholding
* absDiff:
* Bitwise operations: This is used for editing and flipping the masks of images.
* WarpPerspective:
* pytesseract OCR: This used an image of text and returns a string of the characters in the image.
* Bounding rect:
* Resizing: 
* https://www.pyimagesearch.com/2014/08/04/opencv-python-color-detection/
^Color detection
OCR?: https://towardsdatascience.com/how-to-extract-text-from-images-with-python-db9b87fe432b


* Research
There are multiple methods of Optical Character Recognition in python.[2] OCR is basically for extracting text from an image. There were many libaries to choose from[3] but ultimately we ended up choosing pytesseract[4] as it is recommended for use with python.

NEED TO FIX CITATIONS:
[1] https://www.cardschat.com/poker-hands/
[2] https://docparser.com/blog/what-is-ocr/
[3] https://en.wikipedia.org/wiki/Comparison_of_optical_character_recognition_software
[4] https://github.com/UB-Mannheim/tesseract/wiki