# Lab #1 (Text Analysis): Text Analysis in Python

<a href="http://creativecommons.org/licenses/by-nc/4.0/" rel="license"><img style="border-width: 0;" src="https://i.creativecommons.org/l/by-nc/4.0/88x31.png" alt="Creative Commons License" /></a>
This tutorial is licensed under a <a href="http://creativecommons.org/licenses/by-nc/4.0/" rel="license">Creative Commons Attribution-NonCommercial 4.0 International License</a>.

## Table of Contents

- [Bulk Downloads](#bulk-downloads)
- [Optical Character Recognition (OCR)](#optical-character-recognition-ocr)
- [Text Analysis in Python](#text-analysis-in-python)
- [Next Steps & Additional Resources](#next-steps--additional-resources)
- [Reflection Questions](#reflection-questions)

# Bulk Downloads

To undertake large-scale text analysis, we would need to be able to download source material in bulk and eventually convert that source material to plain-text formats for various kinds of analysis and visualization in a programming environment.

This section of the lab procedure includes Jupyter notebook (`.ipynb`) files with sample Python workflows for using text and data mining workflows with select collections of digitized material from the [University of Notre Dame Archives](http://archives.nd.edu/). Prof. Walden has built out Jupyter notebooks for bulk downloading PDFs for the following collections. Each Jupyter Notebook goes into more detail about the sample Python code presented.

*NOTE: Prof. Walden has already loaded PDFs for these publications into Google Drive ([link to folder](https://drive.google.com/drive/folders/17NxGLvJEmgF1RIKevCrcTGYdJSSKba7T?usp=drive_link)). If you want or need to download files to your personal computer, you can- but just know we're talking about gigabytes of material. My recommendation is for folks to make copies of the Jupyter Notebooks within Google Drive so you can run them through Google CoLab, mount the files in Google Drive, and not have to deal with storage and processing constraints/limitations on your personal computer.*

- [Alumnus](https://drive.google.com/file/d/1ZgGuymWQTX1IeTwWamr88RkPPuOeujS-/view?usp=sharing)
- [Bagby Glass Plate Negative Collection](https://drive.google.com/file/d/18Z19MYeu3iJzcjbItJQ97FPHWvSBVV4i/view?usp=sharing)
- [Annual Bulletings and Catalogs](https://drive.google.com/file/d/1D3_LhB3TcuNOiePnz8VubWpiP2Xl3rzn/view?usp=sharing)
- [Capstan](https://drive.google.com/file/d/1cH6qsO5F5kh6KBYhk-rsugraGjt3gs-Z/view?usp=sharing)
- [Commencement Programs](https://drive.google.com/file/d/1Cssj7PnOnb1XI0WuLKzQLDi5mWSna-E9/view?usp=sharing)
- [Daily](https://drive.google.com/file/d/1zwheUyZaZ9ut-ewYIx90ltFsaxXQgESS/view?usp=sharing)
- [Directories](https://drive.google.com/file/d/1Usoq-kxdywEnuUzp0F4GZKSjlI0YWx9V/view?usp=sharing)
- [Magazine](https://drive.google.com/file/d/19qTFmbhp7qJTdpCHcKTk-0GXvPc_N2-D/view?usp=sharing)
- [Observer](https://drive.google.com/file/d/1lCyuGKXQI4GrSGVOuz4l6bjscAd_-d2r/view?usp=sharing)
- [Scholastic](https://drive.google.com/file/d/1_rygfLHBoADkQqnfhTUd0xzUkF51n7Kp/view?usp=sharing)
- [Scholastic Football Review](https://drive.google.com/file/d/1oDtiH6hbeWhbAaAoZCU5-cSlojaDy88A/view?usp=sharing)
- [Voice](https://drive.google.com/file/d/1ydyMMAf43Aw7ltgB9CobTukR__MEO-P6/view?usp=sharing)

# Optical Character Recognition (OCR)

Prof. Walden has built out a Jupyter notebook that outlines a preliminary optical character recognition (OCR) workflow, using the Scholastic Football Review publications as an example.

The OCR workflow uses the following programs and Python modules:
- `tesseract`
- `pytesseract`
- `opencv`
- `pillow`
- `pdf2image`

The OCR workflow includes the following steps:
- Creates sub-directories for each `PDF`
- Converts each page in a `PDF` to a `PNG` file
- Saves the image files for a single `PDF` in a sub-directory
- Runs OCR on image files with sample code for `pytesseract` and `pytesseract`/`opencv` workflows
- Writes OCR output to a `txt` file in the main directory, with one `txt` file for each `PDF`

[Click here to access the Jupyter Notebook via Google CoLab](https://drive.google.com/file/d/1WbGTAvs1WCGrC5XZeADyhminFn8QMEHT/view?usp=sharing)

## Hacking Google CoLab

Given the scale of the processing jobs you may end up running, you will likely want to optimize Google CoLab's performance:
- Under `Runtime`, select `Change runtime type`
- Select `Python 3` for `Runtime type` and `GPU` for `Hardware accelerator`
  * Source: Matthew Mayo, "[3 Essential Google Colaboratory Tips and Tricks](https://www.kdnuggets.com/2018/02/essential-google-colaboratory-tips-tricks.html)" *KD Nuggets* (February 2018)

If folks need to go beyond what their personal computers or CoLab can handle, we do have access to high-performance computing (HPC) resources through Notre Dame's [Center for Research Computing](https://crc.nd.edu/). Contact Prof. Walden to learn more and discuss next steps.

[Click here](https://github.com/kwaldenphd/football-text-analysis/blob/main/python-ocr.md) for more details on the tools covered in the sample OCR workflow.

# Text Analysis in Python

Prof. Walden has built out a Jupyter notebook that outlines a preliminary text analysis workflow, using the Scholastic Football Review publications as an example.

The text analysis workflow is based on the back-end stack for Eric Lease Morgan's Distant Reader.
- Morgan, Eric Lease. (2020, April 10). Distant Reader (Version Alpha). Zenodo. https://doi.org/10.5281/zenodo.3747777.

The workflow uses the following Python modules:
- `wordcloud`
- `matplotlib`
- `spaCy`
- `nltk`
- `gensim`

The workflow includes sample code for the following steps or tasks:
- Generate a word cloud using `wordcloud` and `matplotlib`
- Analyze syntax using `spaCy`
- Part-of-speech tagging using `spaCy`
- Named entity extraction and visualization using `spaCy`
- Tokenizing text and tag tokens using `nltk`
- Named entity extraction using `nltk`
- Generate unique word list using `nltk`
- Plot term frequency and distribution using `nltk` and `matplotlib`
- Generate dictionary and corpus from text file using `gensim`
- Show word weights in corpus using `gensim`
- Create bag of words from single text file using `gensim`
- Create TD-IDF model and show TD-IDF weights using `gensim`

[Click here to access the Jupyter Notebook via Google CoLab](https://drive.google.com/file/d/1S2W6NQfLC_9kbcg7_RwYZ163yZ6R7n1K/view?usp=sharing)

## Next Steps & Additional Resources

[Click here](https://github.com/kwaldenphd/football-text-analysis/blob/main/python-next-steps.md) for more documentation and resources on some of the tools covered in this section of the lab.

## Reflection Questions

- What did you find engaging or interesting about the different aspects of these Python workflows?
- What challenges, frustrations, or limitations did you encounter while using and/or modifying these Python workflows?
- What words or features stood out in each component of the sample text analysis workflow?
- What types of historical research questions could a researcher have about a text or collection of texts?
- How did you understand the textual analysis differently based on how it was presented?
- What questions do you have about how the sample text analysis workflow and related Python libraries generated the analysis presented (or what can we tell about how the tool is calculating results/generating visualizations)?
- What remaining questions do you have about the source you focused on?
- How would you move forward with specific components of the sample Python text analysis workflow and related libraries as a tool for historical textual analysis?
  * To put that another way, what types of historical research questions could a researcher have about a text or collection of texts? How effectively might the different Python libraries and analysis methods highlighted be able to address those questions?
- Other questions/observations
