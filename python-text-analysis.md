# Lab #1 (Text Analysis): Text Analysis in Python

<a href="http://creativecommons.org/licenses/by-nc/4.0/" rel="license"><img style="border-width: 0;" src="https://i.creativecommons.org/l/by-nc/4.0/88x31.png" alt="Creative Commons License" /></a>
This tutorial is licensed under a <a href="http://creativecommons.org/licenses/by-nc/4.0/" rel="license">Creative Commons Attribution-NonCommercial 4.0 International License</a>.

## Table of Contents

- [Text Analysis in Python](#text-analysis-in-python)
- [Python Text Analysis Next Steps and Additional Resources](#python-text-analysis-next-steps-and-additional-resources)
- [More documentation on the tools covered in this notebook](#more-documentation-on-the-tools-covered-in-this-notebook)
- [On-Campus Resources and Workshops](#on-campus-resources-and-workshops)
- [Other Tutorials, Packages, and Methods](#other-tutorials-packages-and-methods)

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

## Python Reflection Questions

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

## Python Text Analysis Next Steps and Additional Resources

### More documentation on tools covered in this notebook

**`wordcloud`**
- wordcloud, "[WordCloud for Python documentation](https://amueller.github.io/word_cloud/)"
- wordcloud, "[Gallery of Examples](https://amueller.github.io/word_cloud/auto_examples/index.html#example-gallery)"
- Duong Vu, "[Generating Word Clouds in Python](https://www.datacamp.com/community/tutorials/wordcloud-python)" *DataCamp* (8 November 2019)
- Zolzaya Luvsandorj, "[Simple Word Cloud in Python](https://towardsdatascience.com/simple-wordcloud-in-python-2ae54a9f58e5)" *Towards Data Science* (20 June 2020)

**`spaCy`**
- spaCy, "[spaCy 101: Everything you need to know](https://spacy.io/usage/spacy-101)"
- spaCy, "[Advanced NLP with spaCy](https://course.spacy.io/en/)"
- Ines Montani, "[spaCy Cheat Sheet: Advanced NLP in Python](https://www.datacamp.com/community/blog/spacy-cheatsheet)" *DataCamp* (14 July 2021)
- Conor Mc., "[A short introduction to NLP in Python with spaCy](https://towardsdatascience.com/a-short-introduction-to-nlp-in-python-with-spacy-d0aa819af3ad)" *Towards Data Science* (17 March 2017)

**`nltk`**
- Steven Bird, Ewan Klein, and Edward Loper, *[Natural Language Processing With Python: Analyzing Text with the Natural Language Toolkit](http://www.nltk.org/book/)* (O'Reilly, 2009).
  * Free online book includes chapters on processing tasks, categorizing/tagging words, classifying text, extracting information, analyzing sentence structure, and other tasks.
- Avinash Navlani, "[Text Analytics for Beginners using NLTK](https://www.datacamp.com/community/tutorials/text-analytics-beginners-nltk)" *DataCamp* (13 December 2019)
- Michelle Morales, "[How to Work with Language Data in Python 3 Using the Natural Language Toolkit (NLTK)](https://www.digitalocean.com/community/tutorials/how-to-work-with-language-data-in-python-3-using-the-natural-language-toolkit-nltk)" *Digital Ocean* (3 January 2017)
- Shaumik Daityari, "[How to Perform Sentiment Analysis in Python 3 using the Natural Langauge Toolkit (NLTK)](https://www.digitalocean.com/community/tutorials/how-to-perform-sentiment-analysis-in-python-3-using-the-natural-language-toolkit-nltk)" *Digital Ocean* (26 September 2019)
- Zoë Wilkinson Saldaña, "Sentiment Analysis for Exploratory Data Analysis," The Programming Historian 7 (2018), https://doi.org/10.46430/phen0079.
- François Dominic Laramée, "Introduction to stylometry with Python," The Programming Historian 7 (2018), https://doi.org/10.46430/phen0078.

### On-Campus Resources and Workshops

Eric Lease Morgan, the lead developer and project coordinator for Distant Reading is the Digital Initiatives Librarian here at ND, in the Navari Family Center for Digital Scholarship.
- [Eric's library profile](https://directory.library.nd.edu/directory/employees/emorgan)

He teaches a number of specialized workshops on text mining and data analysis, including many on the topics, tools, and methods covered in this lab. 

A list of his Fall 2021 workshops:
- [Introduction to Text Mining, Tuesday 9/21, 11am-12pm](https://library.nd.edu/event/introduction-to-text-mining-2021-09-21)
- [Using the Distant Reader, multiple dates/times](https://library.nd.edu/events/recurring/using-the-distant-reader-fall-2021)
- [Preparing Files for Text and Data Mining, Friday 9/24, 12:30-1:30pm](https://library.nd.edu/event/preparing-files-for-text-and-data-mining-2021-09-24)
- [Using Topic Modeling Against a Corpora, Wednesday 9/29, 12:30-1:30pm](https://library.nd.edu/event/using-topic-modeling-against-a-corpora-2021-09-29)
- [Extracting the Who, What, and When from a Text, Monday 10/4, 12:30-1:30pm](https://library.nd.edu/event/extracting-the-who-what-when-from-a-text-2021-10-04)
- [Using a Concordance with AntConc, Wednesday 10/6, 12:30-1:30pm](https://library.nd.edu/event/using-a-concordance-2021-10-06)
- [Introduction to Natural Language Processing With Python, Tuesday 10/12, 11am-12pm](https://library.nd.edu/event/introduction-to-natural-language-processing-with-python-2021-10-12)

I highly encourage to attend workshops that connect to tools/methods you want to explore in more detail, especially if you come back to these tools/methods for work you're doing in the final project.

We also have a deep bench of expertise in the [Navari Family Center for Digital Scholarship](https://cds.library.nd.edu/):
- [Eric Morgan Lease](https://directory.library.nd.edu/directory/employees/emorgan), Digital Initiatives Librarian
  * Eric specializes in text mining and large scale computational text analysis. 
- [Daniel Johnson](https://directory.library.nd.edu/directory/employees/djohns27), English Literature and Digital Humanities Librarian
  * Daniel specializes in many things, most germane to this class, digital methods for literary study and computational text analysis.

We'll come back to these on-campus resources when we start working on the final project.

### Other Tutorials, Packages, and Methods

For a more detailed overview of text analysis methods- START HERE before diving into a new method/tutorial:
- Heather Froelich, "[Text Analysis: An Introduction, Methods](https://guides.libraries.psu.edu/c.php?g=829065&p=5922906)" *PennState University Library Guide*
- Stéfan Sinclair & Geoffrey Rockwell, *[The Art of Literary Text Analysis](https://nbviewer.jupyter.org/github/sgsinclair/alta/blob/master/ipynb/ArtOfLiteraryTextAnalysis.ipynb)*, edited by Melissa Mony (last modified 12 January 2018)
  * Includes Jupyter notebooks with more resources on `nltk`, visualizing textual data, and a variety of analysis methods 

For a more detailed overview of various tools and tutorials (beyond those listed here):
- Alan Liu, "[Tutorials for DH Tools and Methods, Text Analysis](http://dhresourcesforprojectbuilding.pbworks.com/w/page/69244314/Tutorials%20for%20DH%20Tools%20and%20Methods#tutorials-text-analysis)" *digital humanities resources for project building* (2019)

**List of words and word frequency**
- William J. Turkel and Adam Crymble, "Normalizing Textual Data with Python," The Programming Historian 1 (2012), https://doi.org/10.46430/phen0014.
- William J. Turkel and Adam Crymble, "Counting Word Frequencies with Python," The Programming Historian 1 (2012), https://doi.org/10.46430/phen0003.
- William J. Turkel and Adam Crymble, "Keywords in Context (Using n-grams) with Python," The Programming Historian 1 (2012), https://doi.org/10.46430/phen0010.

**TF-IDF (term frequency, inverse document frequency)**
- Matthew J. Lavin, "Analyzing Documents with TF-IDF," The Programming Historian 8 (2019), https://doi.org/10.46430/phen0082.
- John R. Ladd, "Understanding and Using Common Similarity Measures for Text Analysis," The Programming Historian 9 (2020), https://doi.org/10.46430/phen0089.
  * Both of these tutorials use [`scikit-learn`'s tf-idf implementation](https://scikit-learn.org/stable/modules/generated/sklearn.feature_extraction.text.TfidfVectorizer.html)

**Topic Modeling (looking for patterns of words in text/corpus to build topics, builds on td-idf)**
- For more specifics on topic modeling as a methodology: 
  * Ted Underwood, "[Topic modeling made just simple enough](https://tedunderwood.com/2012/04/07/topic-modeling-made-just-simple-enough/) *blog* (7 April 2012)
  * Scott Weingart, "[Topic Modeling for Humanists: A Guided Tour](http://scottbot.net/topic-modeling-for-humanists-a-guided-tour/)" *blog* (25 July 2012)
- Shawn Graham, Scott Weingart, and Ian Milligan, "Getting Started with Topic Modeling and MALLET," The Programming Historian 1 (2012), https://doi.org/10.46430/phen0017.
- Shanshank Kapadia, "[Topic Modeling in Python: Latent Dirichlet Allocation (LDA)](https://towardsdatascience.com/end-to-end-topic-modeling-in-python-latent-dirichlet-allocation-lda-35ce4ed6b3e0)" *Towards Data Science* (14 April 2019)
- Susan Li, "[Topic Modelling in Python with NLTK and Gensim](https://towardsdatascience.com/topic-modelling-in-python-with-nltk-and-gensim-4ef03213cd21)" *Towards Data Science* (30 March 2018)

**Sentiment analysis (emotional intensity/weight for words and phrases in a text)**
- Zoë Wilkinson Saldaña, "Sentiment Analysis for Exploratory Data Analysis," The Programming Historian 7 (2018), https://doi.org/10.46430/phen0079.

**Stylometry (literary style, authorship attribution)**
- François Dominic Laramée, "Introduction to stylometry with Python," The Programming Historian 7 (2018), https://doi.org/10.46430/phen0078.

**Geoparsing (extracting and plotting location information)**
- Beatrice Alex, "Geoparsing English-Language Text with the Edinburgh Geoparser," The Programming Historian 6 (2017), https://doi.org/10.46430/phen0067.

**Working with other source material (other archives, APIs, etc)**
- Stephen Krewson, "Extracting Illustrated Pages from Digital Libraries with Python," The Programming Historian 8 (2019), https://doi.org/10.46430/phen0084.
  *  Tutorial covers workflows for getting digital image content from HathiTrust and Internet Archive, but could also get you started with an OCR workflow for texts in these collections.
- Resources for using the Library of Congress' "Chronicling America" collection (wide variety of national and local U.S. newspapers, 1777-1963)
  * Library of Congress, "[About the Site and API](https://chroniclingamerica.loc.gov/about/api/)" *Chronicling America: Historic American Newspapers*
  * Library of Congress, "[Available Tutorials](https://libraryofcongress.github.io/data-exploration/all-tutorials.html)" *loc.gov JSON API*
  * Hugo van Kemenade, "[chroniclingamerica.py: Python API to search Chronicling America newspaper pages](https://github.com/hugovk/chroniclingamerica.py)" *GitHub* (2016)
  * Jason Heppler, "[Working with the Chronicling America API](https://observablehq.com/@hepplerj/working-with-the-chronicling-america-api)" *Observable* (6 July 2020)

**Stanford Natural Language Processing Group**

From their "[Software](https://nlp.stanford.edu/software/)" page: "The Stanford NLP Group makes some of our Natural Language Processing software available to everyone! We provide statistical NLP, deep learning NLP, and rule-based NLP tools for major computational linguistics problems, which can be incorporated into applications with human language technology needs. These packages are widely used in industry, academia, and government...All our supported software distributions are written in Java."

**`scikit-learn`**
- `scikit-learn`, "[Working With Text Data](https://scikit-learn.org/stable/tutorial/text_analytics/working_with_text_data.html)": The `scikit-learn` machine-larning library includes a nubmer of modules and resources for natural language processing, including tasks like feature extraction and linear models for categorization.
