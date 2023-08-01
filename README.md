# Lab #1: Text Analysis

<a href="http://creativecommons.org/licenses/by-nc/4.0/" rel="license"><img style="border-width: 0;" src="https://i.creativecommons.org/l/by-nc/4.0/88x31.png" alt="Creative Commons License" /></a>
This tutorial is licensed under a <a href="http://creativecommons.org/licenses/by-nc/4.0/" rel="license">Creative Commons Attribution-NonCommercial 4.0 International License</a>.

# Overview

This lab uses textual analysis methods to explore student newspaper coverage of Notre Dame football, covering computer vision methods (optical character recognition) and exploratory textual analysis/visualization (using coding and no-coding tools/methods) and focusing on methods for working with unstructured text.

[Click here](https://github.com/kwaldenphd/football-text-analysis/blob/main/acknowledgements.md) to view a full list of acknowledgements for this lab.

# Table of Contents

- [Background](#background)
- [Introduction](#introduction)
  * [University Archive Digital Collections](#university-archive-digital-collections)
  * [From Document to Character](#from-document-to-character)
  * [Files & Resources](#files--resources)
- [Distant Reading with a Single Document: DataBasic](#distant-reading-with-a-single-document-databasic)
- [Distant Reading with a Corpus: Voyant Tools](#distant-reading-with-a-corpus-voyant-tools)
- [Distant Reading with a Concordancer: AntConc](#distant-reading-with-a-concordancer-antconc)
- [Oh, the Places You Could Go](#oh-the-places-you-could-go)
  * [NLTK and Python](#nltk-and-python)
  * [Distant Reader](#distant-reader)  
- [Next Steps (aka, now it's your turn!)](#next-steps-aka-now-its-your-turn) 
  * [Track #1: Additional Skill Building](#option-1-additional-skill-building)
  * [Track #2: Text Analysis Research Proposal](#text-analysis-research-proposal)
- [Lab Notebook Components](#lab-notebook-components)

[Link to Google Drive folder with lab materials and resources, including notebook template](https://drive.google.com/drive/folders/1ewsgmrPNeWJYzi5f8EXr05VjPnlRCATz?usp=sharing) (ND Users)

Lab notebook formats for non-ND users: 
- [Google Doc](https://docs.google.com/document/d/1mBiPpxjRfBlEZI9XIc8rzSpSuHfAlrfV6l5ivjih1Vo/copy)
- [Markdown](https://github.com/kwaldenphd/football-text-analysis/blob/main/lab-notebook-template.md)
- [PDF](https://github.com/kwaldenphd/football-text-analysis/blob/main/Text_Analysis_Lab_Notebook_Template.pdf)

# Background

To prepare for this lab, we read Kirsten Bussière's “[Chapter 4- Text Analysis](https://web.archive.org/web/20220831021739/https://carletonu.pressbooks.pub/digh5000/chapter/chapter-4-text-analysis/)” in *Digital Humanities: A Primer* (Carleton University) and explored Alex Wermer-Colan's "[Computational Text Analysis](https://guides.temple.edu/corpusanalysis)" Temple University Library Guide.

Discussion Questions:
- What stood out to you from the resources we engaged with on computational text analysis?
- Questions you have about some of the research methods and approaches mentioned?
- Things you think would be interesting to explore related to Notre Dame Football using some of these methods?
- Other questions/observations

# Introduction

## From Document to Character

SOMETHING ON METADATA, OCR

## University Archive Digital Collections

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

## Files & Resources

- [Google Drive folder](https://drive.google.com/drive/folders/1lvk2Vwah6ZZ69WC6TTbGZUIgXCqYSBi7?usp=drive_link) with sample files, Python notebooks, and lab notebook template
- [1929 Scholastic Football Review](https://docs.google.com/document/d/13-NlJ40DzzFBUs2qe1uOpET1ZKEGs3I2DZLzKzulnSU/edit?usp=drive_link)
- [1931 Scholastic Football Review](https://drive.google.com/file/d/1cPcY6mXNLcXUoL27v3BxlMgNkB4pS4rT/view?usp=drive_link)
- [Folder with Scholastic Football Reviews](https://drive.google.com/drive/folders/1zK99DK_Cd-w9tu2u2M5vlAOSidZYdVTd?usp=drive_link)

# Distant Reading with a Single Document: DataBasic

Something about computational methods, single document, what single document we're using, etc.

According to [its website,](https://databasic.io) “DataBasic is a suite of easy-to-use web tools for beginners that introduce concepts of working with data. These simple tools make it easy to work with data in fun ways, so you can learn how to find great stories to tell.” DataBasic is developed and supported by MIT’s [Center for Civic Media](https://civic.mit.edu/) and Emerson College’s [Engagement Lab.](https://elab.emerson.edu/) 

[Click here](https://github.com/kwaldenphd/football-text-analysis/blob/main/data-basic.md) to open this section of the lab.

# Distant Reading with a Corpus: Voyant Tools

In focusing on a single document, we're able to get a granular sense of how computational methods are interacting with text information. But what if we want to use these methods on a collection of documents?

<a href="http://voyant-tools.org/">Voyant Tools</a> is an open-source web application developed by Stéfan Sinclair and Geoffrey Rockwell in 2003, with later contributions added by Andrew MacDonald, Cyril Briquet, Lisa Goddard, and Mark Turcato. While Voyant is one of the leading robust web-based textual analysis interfaces, it grew out of existing text analysis tools like HyperPo, Tapoware, and TACT. Voyant also offers <a href="https://github.com/sgsinclair/Voyant">open-source code</a> that can be used to deploy the program on a server. Voyant users can upload text files from their computer, link to online text sources, or scrape the text off a webpage for analysis and visualization. Unlike more advanced, programming-oriented textual analysis programs like R and R Studio, Voyant gives users access to a range statistical analysis and visualization features without requiring significant technical knowledge.

[Click here](https://github.com/kwaldenphd/football-text-analysis/blob/main/voyant-tools.md) to open this section of the lab.

# Distant Reading with a Concordancer: AntConc

WHAT IS A CONCORDANCER

Developed by Laurence Anthony, <a href="http://www.laurenceanthony.net/software/antconc/">AntConc</a> is a free, closed-source program that runs on Windows, OS, and Linux. At the most basic level, AntConc is a concordancer, or a program that constructs a concordance based on terms in a text or collection of texts. AntConc also allows users to visualize concordance calculations and generate word and keyword lists based on terms present in the text. AntConc also supports cluster and collocation analysis and visualization. With Voyant, we explored a web-based graphical user interface option for conducting textual analysis, with a particular emphasis on visualization. AntConc is a software program (that runs on your own computer) that focuses more on corpus linguistics and statistical analysis methods.

[Click here](https://github.com/kwaldenphd/football-text-analysis/blob/main/antconc.md) to open this section of the lab.

# Oh, the Places You Could Go!

In addition to the graphical-user-interface (GUI) based tools covered in the previous sections of the lab, we can also apply these methods using programmatic workflows.

[Click here]() to open this section of the lab.

## NLTK and Python

To undertake large-scale text analysis, we would need to be able to download source material in bulk and eventually convert that source material to plain-text formats for various kinds of analysis and visualization in a programming environment. This section of the lab procedure includes Jupyter notebook (`.ipynb`) files with sample Python workflows for using text and data mining workflows with select collections of digitized material from the [University of Notre Dame Archives](http://archives.nd.edu/).

[Link to this section of the lab](https://github.com/kwaldenphd/football-text-analysis/blob/main/python-text-analysis.md)

## Natural Language Processing and Text Analysis in R

Taylor Arnold and Lauren Tilton (2015), [*Humanities Data in R: Exploring Networks, Geospatial Data, Images, and Text*](https://onesearch.library.nd.edu/permalink/f/1phik6l/ndu_aleph005141805). Springer.
- [Supplementary material](https://humanitiesdata.org/)

[CRAN Task View: Natural Language Processing](https://cran.r-project.org/web/views/NaturalLanguageProcessing.html)

*Programming Historian* tutorials:
- [Basic text processing](https://programminghistorian.org/en/lessons/basic-text-processing-in-r)
- [Sentiment analysis](https://programminghistorian.org/en/lessons/sentiment-analysis-syuzhet)

## Topic Modeling

*Programming Historian* [Topic Modeling & MALLET tutorial](https://programminghistorian.org/en/lessons/topic-modeling-and-mallet)

[Prof. Walden's tutorial](https://github.com/kwaldenphd/topicmodeling-tutorial)

[Link to download Stanford's Topic Modeling Tool](https://downloads.cs.stanford.edu/nlp/software/tmt/tmt-0.3)

## Named Entity Extraction 

[Prof. Walden's tutorial](https://github.com/kwaldenphd/NLP-NER-tutorial)

[Link to download Stanford's Named Entity Recognition tool](https://nlp.stanford.edu/software/CRF-NER.shtml)

## Distant Reader

"The Distant Reader takes text as input, does analysis against it, and outputs sets of structured data called 'study carrels', which students, researchers, or scholars can use to do both close and distant reading...[it is] a tool intended to supplement the traditional reading process. Given a set of one or more texts acquired through a variety of means, the Reader: 1) applies different forms of text mining and natural language processing against the texts, 2) saves the results as a set of structured data amenable to computing, 3) summarizes everything in a set of interactive HTML reports, 4) compresses everything into a .zip file, and 5) provides the means for you to view the results online or download the whole thing to your computer. This resulting .zip file is affectionately called a 'study carrels."
- Morgan, Eric Lease. (2020, April 10). Distant Reader (Version Alpha). Zenodo. https://doi.org/10.5281/zenodo.3747777.

To learn more about Distant Reader:
- [About](https://distantreader.org/)
- [Getting Started](https://reader-toolbox.readthedocs.io/en/latest/)

# Next Steps (aka, now it's your turn!)

By this point in the lab we've covered a number of different tools for (computational) text analysis. Now it's your turn to come up with a small-scale question, topic, etc. related to the period of ND football history we've been looking at (or some of the broader themes we've been talking about) that you could explore using some of the primary sources and analysis/research methods covered in this lab.

[Click here](https://github.com/kwaldenphd/football-text-analysis/blob/main/next-steps.md) to open this section of the lab.
