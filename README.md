# CardGameAssistant-ImageProcessing
This program reads in a hand of 5 cards and determines the value of each card.

## Requirements

    Tesseract OCR #Only neccessary if not using anaconda 
    pytesseract

### These steps will give you a rundown of how to install the above packages

#### if you are using anaconda then these are the steps for installation

* first open anaconda
* once anaconda is running look for program titled `CMD.exe Prompt` it has a picture of the anaconda logo above
* once located click this program and enter the following commands
  * `conda install -c conda-forge pytesseract`
  * `conda install -c conda-forge/label/cf202003 pytesseract`
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

#### Instructions
With tesseract set up, run all cells in the notebook. There will be a file open box allowing you to pick any of the sample card hands. The program will display the value of all the cards in the chosen image.

#### Assumptions
This program assumes the user will use an input image of five playing cards taken from above the cards.

#### Algorithm steps:
* This Program starts off by
* It then
* Once the
* With this 
* If 
* It then 
* It now 
* Next, 
* After this,
* It then 
* Next 
* Finally,


#### Performance
The algorithm takes a very small amount of time to run, looking almost instant to the user. The program is mostly accurate, but accuracy depends on the image, so if the user wants to test an image from far away or with very bad lighting, accuracy may faulter.

#### Underlying concepts:
* Thresholding: This selects certain parts of a grayscale image based on a threshold value allowing the user to separate objects.
* Masking: This selects certain parts of an image based on a binary mask.
* Contours: This finds continuous points on a shape and can be used for object detection.
* fillPoly: This fills in an area specified by the parameters.
* GaussianBlur: 
* pytesseract:
* absDiff: 


