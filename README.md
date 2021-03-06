# Lab #1: Text Analysis

<a href="http://creativecommons.org/licenses/by-nc/4.0/" rel="license"><img style="border-width: 0;" src="https://i.creativecommons.org/l/by-nc/4.0/88x31.png" alt="Creative Commons License" /></a>
This tutorial is licensed under a <a href="http://creativecommons.org/licenses/by-nc/4.0/" rel="license">Creative Commons Attribution-NonCommercial 4.0 International License</a>.

# Overview

This lab uses textual analysis methods to explore student newspaper coverage of Notre Dame football, covering computer vision methods (optical character recognition) and exploratory textual analysis/visualization (using coding and no-coding tools/methods) and focusing on methods for working with unstructured text.

[Click here](https://github.com/kwaldenphd/football-text-analysis/blob/main/acknowledgements.md) to view a full list of acknowledgements for this lab.

# Table of Contents

## Abbreviated Table of Contents

- [Background](#background)
- [University Archive Digital Collections](#university-archive-digital-collections)
- [Voyant Tools](#voyant-tools)
- [DataBasic](#databasic)
- [Distant Reader](#distant-reader)
- [AntConc](#antconc)
- [Python](#python)
  * [Optical Character Recognition](#optical-character-recognition)
  * [Text Analysis in Python](#text-analysis-in-python)
- [Next Steps (aka, now it's your turn!)](#next-steps-aka-now-its-your-turn)   

[Link to Google Drive folder with lab materials and resources, including notebook template](https://drive.google.com/drive/folders/1ewsgmrPNeWJYzi5f8EXr05VjPnlRCATz?usp=sharing) (ND Users)

FOR NON-ND USERS: 
- [Link to make a copy of the lab notebook template](https://docs.google.com/document/d/1mBiPpxjRfBlEZI9XIc8rzSpSuHfAlrfV6l5ivjih1Vo/copy) (Google Doc)
- [Lab notebook template as a plain-text `.md` file](https://github.com/kwaldenphd/football-text-analysis/blob/main/lab-notebook-template.md)
- [Lab notebook template as a PDF](https://github.com/kwaldenphd/football-text-analysis/blob/main/Text_Analysis_Lab_Notebook_Template.pdf)

# Background

To prepare for this lab, we read Kirsten Bussi??re's ???[Chapter 4- Text Analysis](https://carletonu.pressbooks.pub/digh5000/chapter/chapter-4-text-analysis/)??? in *Digital Humanities: A Primer* (Carleton University) and explored Alex Wermer-Colan's "[Computational Text Analysis](https://guides.temple.edu/corpusanalysis)" Temple University Library Guide.

Discussion Questions:
- What stood out to you from the resources we engaged with on computational text analysis?
- Questions you have about some of the research methods and approaches mentioned?
- Things you think would be interesting to explore related to Notre Dame Football using some of these methods?
- Other questions/observations

# University Archive Digital Collections

Head to the University Archives' "[Digital Collections](http://archives.nd.edu/digital/)" web page.

Browse the resources and materials listed, thinking about...
- Time period the resource covers
- Type of material/publication (student publication versus University publication, newspaper versus yearbook versus magazine, etc)

Focus on a specific text resource and select a PDF to download. For serialized publications, this may involve clicking through multiple pages to get to specific issues.
- If you're not sure where to get started or what resource to focus on, [the *Scholastic*](http://archives.nd.edu/Scholastic/) is a student publication from the period we've been discussing, and their annual football review has [its own digital collection](http://archives.nd.edu/Football/).

Looking at a specific document...
- What can we tell about who created this resource (specific authors as well as publisher)?
- What kinds of information are included in this resource (images, text, etc)?
- What topics are covered or addressed in this resource?
- What kinds of research questions or topics could you analyze/explore using this resource?

# Voyant Tools

We'll start by using a web-based textual analysis tool to engage with the resource you selected and explored in the previous section of the lab.

<a href="http://voyant-tools.org/">Voyant Tools</a> is an open-source web application developed by St??fan Sinclair and Geoffrey Rockwell in 2003, with later contributions added by Andrew MacDonald, Cyril Briquet, Lisa Goddard, and Mark Turcato. While Voyant is one of the leading robust web-based textual analysis interfaces, it grew out of existing text analysis tools like HyperPo, Tapoware, and TACT. Voyant also offers <a href="https://github.com/sgsinclair/Voyant">open-source code</a> that can be used to deploy the program on a server. Voyant users can upload text files from their computer, link to online text sources, or scrape the text off a webpage for analysis and visualization. Unlike more advanced, programming-oriented textual analysis programs like R and R Studio, Voyant gives users access to a range statistical analysis and visualization features without requiring significant technical knowledge.

[Click here](https://github.com/kwaldenphd/football-text-analysis/blob/main/voyant-tools.md) to open this section of the lab.

# DataBasic

Another web-based tool for text analysis that we'll explore is DataBasic.

According to [its website,](https://databasic.io) ???DataBasic is a suite of easy-to-use web tools for beginners that introduce concepts of working with data. These simple tools make it easy to work with data in fun ways, so you can learn how to find great stories to tell.??? DataBasic is developed and supported by MIT???s [Center for Civic Media](https://civic.mit.edu/) and Emerson College???s [Engagement Lab.](https://elab.emerson.edu/) 

[Click here](https://github.com/kwaldenphd/football-text-analysis/blob/main/data-basic.md) to open this section of the lab.

# Distant Reader

"The Distant Reader takes text as input, does analysis against it, and outputs sets of structured data called 'study carrels', which students, researchers, or scholars can use to do both close and distant reading...[it is] a tool intended to supplement the traditional reading process. Given a set of one or more texts acquired through a variety of means, the Reader: 1) applies different forms of text mining and natural language processing against the texts, 2) saves the results as a set of structured data amenable to computing, 3) summarizes everything in a set of interactive HTML reports, 4) compresses everything into a .zip file, and 5) provides the means for you to view the results online or download the whole thing to your computer. This resulting .zip file is affectionately called a 'study carrels."
- Morgan, Eric Lease. (2020, April 10). Distant Reader (Version Alpha). Zenodo. https://doi.org/10.5281/zenodo.3747777.

To learn more about Distant Reader:
- [About](https://distantreader.org/about)
- [Getting Started](https://distantreader.org/getting-started)

[Click here](https://github.com/kwaldenphd/football-text-analysis/blob/main/distant-reader.md) to open this section of the lab.

# AntConc

Developed by Laurence Anthony, <a href="http://www.laurenceanthony.net/software/antconc/">AntConc</a> is a free, closed-source program that runs on Windows, OS, and Linux. At the most basic level, AntConc is a concordancer, or a program that constructs a concordance based on terms in a text or collection of texts. AntConc also allows users to visualize concordance calculations and generate word and keyword lists based on terms present in the text. AntConc also supports cluster and collocation analysis and visualization. With Voyant, we explored a web-based graphical user interface option for conducting textual analysis, with a particular emphasis on visualization. AntConc is a software program (that runs on your own computer) that focuses more on corpus linguistics and statistical analysis methods.

[Click here](https://github.com/kwaldenphd/football-text-analysis/blob/main/antconc.md) to open this section of the lab.

# Python

To undertake large-scale text analysis, we would need to be able to download source material in bulk and eventually convert that source material to plain-text formats for various kinds of analysis and visualization in a programming environment.

This section of the lab procedure includes Jupyter notebook (`.ipynb`) files with sample Python workflows for using text and data mining workflows with select collections of digitized material from the [University of Notre Dame Archives](http://archives.nd.edu/).

Each Jupyter Notebook goes into more detail about the sample Python code presented.

# Bulk Download

Prof. Walden has built out Jupyter notebooks for bulk downloading PDFs for a variety of digital collections in the University Archive.

NOTE: Prof. Walden has already loaded PDFs for these publications into Google Drive. If you want or need to download files to your personal computer, you can- but just know we're talking about gigabytes of material. My recommendation is for folks to make copies of the Jupyter Notebooks within Google Drive so you can run them through Google CoLab, mount the files in Google Drive, and not have to deal with storage and processing constraints/limitations on your personal computer. 

[Link to this section of the lab](https://github.com/kwaldenphd/football-text-analysis/blob/main/python-bulk-download.md)

# Optical Character Recognition

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

Jupyter Notebook:
- [GitHub](https://github.com/kwaldenphd/football-text-analysis/blob/main/notebooks/ocr-roadmap.ipynb)
- [Jupyter nbviewer](https://nbviewer.jupyter.org/github/kwaldenphd/football-text-analysis/blob/main/notebooks/ocr-roadmap.ipynb)
- [Google CoLab](https://drive.google.com/file/d/1WbGTAvs1WCGrC5XZeADyhminFn8QMEHT/view?usp=sharing) *ND users*

[Click here](https://github.com/kwaldenphd/football-text-analysis/blob/main/python-ocr.md) to open this section of the lab.

## Text Analysis in Python

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

Jupyter Notebook:
- [GitHub](https://github.com/kwaldenphd/football-text-analysis/blob/main/notebooks/text-analysis-roadmap.ipynb)
- [Jupyter nbviewer](https://nbviewer.jupyter.org/github/kwaldenphd/football-text-analysis/blob/main/notebooks/text-analysis-roadmap.ipynb)
- [Google CoLab](https://drive.google.com/file/d/1S2W6NQfLC_9kbcg7_RwYZ163yZ6R7n1K/view?usp=sharing)

[Click here](https://github.com/kwaldenphd/football-text-analysis/blob/main/python-text-analysis.md) to open this section of the lab.

# Next Steps (aka, now it's your turn!)

By this point in the lab we've covered a number of different tools for (computational) text analysis, including some that run in a web browser, some that run are your local computer, and some that involve working within a programming language.

Now it's your turn to come up with a small-scale question, topic, etc. related to the period of ND football history we've been looking at (or some of the broader themes we've been talking about) that you could explore using some of the primary sources and analysis/research methods covered in this lab.

This section of the lab will resemble a more "traditional" lab report:
- Background or context for the research question or topic you're exploring
  * At least 500 words (or 5 minutes audio/video) on how the question you're asking or topic you're exploring is grounded in the texts we've been reading and conversations we've been having about ND football history and cultural significance.
  * To put it another way, this is a "background" section.
- Sources and research/analysis methods you'll be using
  * At least 200 words (or 2 minutes audio/video) on how the specific sources you're engaging with and research/analysis methods you're using animate or connect to the question(s) you're asking or the topic(s) you're exploring.
  * To put it another way, this is a "methods" or "methodology" section
- What you found through the exploration/analysis
  * At least 500 words (or 5 minutes audio/video) on what you found through analyzing this source material using specific research/analysis methods. Folks are encouraged to include visualizations/screenshots/figures/etc in this section.
  * To put it another way, this is a "findings" section
- Conclusions and next steps
  * At least 250 words (or 2-3 minutes asudio/video) on how your findings relate to the broader context or background you outlined at the start of the report. 
  * How can the work you did in this lab inform how we think about or understand ND football's history and cultural significance? How does it connect to the readings and conversations we've been having in class?
  * Where would you go next with this research? What questions emerged through doing this work? What questions were you not able to address? 
  * To put it another way, this is a hybrid "discussion" and "conclusion" section
- Any PDF or TXT files you created or worked with (that aren't already in the Lab 1 Google Drive)
- Any Python scripts/Jupyter Notebooks (or RStudio/RMarkdown files) used in the lab
- Individual reflections
  * At least 200 words (or 2-3 minutes audio/video) from each member of the group, addressing the following questions:
    * Your contribution to the lab report
    * Challenges you faced in this lab and how you solved them
    * What you learned about text analysis through this lab
    * How you're thinking about text analysis (and ND football history/primary sources) differently after this lab
    * Other comments/questions/observations

[Click here](https://github.com/kwaldenphd/football-text-analysis/blob/main/next-steps.md) to open this section of the lab.
