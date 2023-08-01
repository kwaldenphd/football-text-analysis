# Lab #1 (Text Analysis): Optical Character Recognition in Python

<a href="http://creativecommons.org/licenses/by-nc/4.0/" rel="license"><img style="border-width: 0;" src="https://i.creativecommons.org/l/by-nc/4.0/88x31.png" alt="Creative Commons License" /></a>
This tutorial is licensed under a <a href="http://creativecommons.org/licenses/by-nc/4.0/" rel="license">Creative Commons Attribution-NonCommercial 4.0 International License</a>.

## OCR Next Steps and Additional Resources

There are a number of options and next steps for refining or further building out an OCR workflow.

**More documentation on tools covered in this notebook**:
- Tesseract
  * ["Tesseract documentation"](https://tesseract-ocr.github.io/tessdoc/)
    * ["Improving the quality of the output"](https://tesseract-ocr.github.io/tessdoc/ImproveQuality)
  * University of Illinois Scholarly Commons, "[Introduction to OCR and Searchable PDFs: Tesseract](https://guides.library.illinois.edu/c.php?g=347520&p=4116757)" *University of Illinois Library*
  * NYU Libraries Scholarly Communications and Information Policy Department, "[Tesseract OCR Software Tutorial](https://guides.nyu.edu/tesseract/home)" *New York University Libraries*
     * The NYU guide covers how to convert PDF or PNG files to TIFF high-resolution images, improving image quality using command-line tool ImageMagick, and optimizing the command-line version of Tesseract
   * Andrew Akhlaghi, "OCR and Machine Translation," The Programming Historian 10 (2021), https://doi.org/10.46430/phen0091.
     * Tutorial that covers ImagMagick to Tesseract workflow.
   * Moritz Mähr, "Working with batches of PDF files," The Programming Historian 9 (2020), https://doi.org/10.46430/phen0088.
     * Tutorial that covers using `poppler` to extract images from PDF and preliminary topic modeling
- OpenCV
  * ["OpenCV documentation"](https://opencv.org/)
    * `OpenCV` has a number of more advanced features and functions, including rotation/deskewing, removing shadows, object detection, etc. OpenCV's [Python Tutorials](https://docs.opencv.org/4.5.3/d6/d00/tutorial_py_root.html) are a good place to start.

**Other tools/packages that can get you started with more advanced work**:
- [Leptonica](http://www.leptonica.org/): variety of resources related to image processing/analysis (affine transformations, binary/grayscale morphology, pixelwise masking/blending, etc)
- [ImageMagick](https://imagemagick.org/index.php): program that uses multi-threaded processing for large-scale image processing workflows (color management, image features, morphology, noise reduction, etc)
- [ScanTailor](https://github.com/4lex4/scantailor-advanced): designed for post-processing scanned pages (before OCR) to improve OCR results (margins, picture zones, dewarping, etc)
- [unpaper](https://github.com/unpaper/unpaper): another tool designed for post-processing scanned material (before OCR) to improve OCR results (dark edges, margins, deskewing, etc)
- [PRLib](https://github.com/leha-bot/PRLib): pre-recognition library (before OCR) designed to improve OCR results (binarization, deskew, noise, etc)

### Acrobat Adobe Pro

But, depending on the number of documents you're working with as well as the quality of OCR output needed for your project, Adobe Acrobat Pro will likely get you where you need to go.
- NOTE: This is a different program than the Adobe Acrobat Reader DC free program you may have on your computer.

Notre Dame students have access to the Adobe Pro software title through the Adobe Creative Cloud Desktop Application, available free through OIT.
- NOTE: The full Adobe Creative Cloud suite is available on any [OIT lab computer](https://nd.service-now.com/kb_view.do?sysparm_article=KB0013524) and can be accessed through the OIT general purpose [Virtual Computer Lab](https://inside.nd.edu/task/all/virtual-computer-lab)

Once you have access to Adobe Pro, you can use the expanded features to run an OCR workflow on a single PDF or multiple PDFs. 

Adobe Pro also allows you to export the contents of a single PDF or multiple PDFs to plain-text (`.txt`) files.

To run OCR within Adobe Pro:
- University of Illinois Scholarly Commons, "[Introduction to OCR and Searchable PDFs: Adobe Acrobat Pro](https://guides.library.illinois.edu/c.php?g=347520&p=4116755)" *University of Illinois Library*
- Rowan University Library Digital Scholarship Center, "[Acrobat Pro: Optical Character Recognition for Research, Learning, and Accessibility](https://youtu.be/HxSYtQdaAp0)" *YouTube video* (20 August 2020)
- Pixascene, "[Perform an OCR on a PDF document using Adobe Acrobat Pro](https://youtu.be/zZT34zmc0kw)" *YouTube video* (15 June 2020)
- Tulane University Libraries, "[Digitize Your Sources: OCR and Adobe Acrobat Pro](https://libguides.tulane.edu/diy_digital/acrobat)" *Tulane University Library Guide*

To export a single PDF as TXT from Adobe Pro (using "Export"):
- Adobe Acrobat User Guide, "[Convert or export PDFs to other file formats](https://helpx.adobe.com/acrobat/using/exporting-pdfs-file-formats.html)" *Adobe* (26 August 2021)
 
To export multiple PDFs as TXT files from Adobe Pro (using "Action Wizard"):
1. `View -> Tools -> Action Wizard -> Create New Action`
2. `Choose 'Save & Export' -> Save -> add to right-hand pane`
3. At `right-hand pane -> choose folder` and click `Specify Settings` to change export format to `TXT`
- Source: StackOverflow, "[How to convert batch pdf files to text using Adobe Acrobat Pro?](https://stackoverflow.com/questions/25212228/how-to-convert-batch-i-e-huge-pdf-files-to-text-using-adobe-acrobat-pro)" *StackOverflow* (2015)
- For more on Action Wizard: Adobe Acrobat User Guide, "[Action Wizard (Acrobat Pro)](https://helpx.adobe.com/acrobat/using/action-wizard-acrobat-pro.html#about_action_wizards)" *Adobe* (2 June 2020)
