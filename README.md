# Lab #1: Text Analysis

<a href="http://creativecommons.org/licenses/by-nc/4.0/" rel="license"><img style="border-width: 0;" src="https://i.creativecommons.org/l/by-nc/4.0/88x31.png" alt="Creative Commons License" /></a>
This tutorial is licensed under a <a href="http://creativecommons.org/licenses/by-nc/4.0/" rel="license">Creative Commons Attribution-NonCommercial 4.0 International License</a>.

# Overview

This lab uses textual analysis methods to explore student newspaper coverage of Notre Dame football, covering computer vision methods (optical character recognition) and exploratory textual analysis/visualization (using coding and no-coding tools/methods) and focusing on methods for working with unstructured text.

# Acknowledgements

## Text Analysis With Voyant Tools

This tutorial was originally written by Katherine Walden, when she was working as a Digital Liberal Arts Specialist at Grinnell College. Tutorial instructions were co-authored by Sarah Purcell (L.F. Parker Professor of History, Grinnell College) and Papa Ampim-Darko, a student research assistant at Grinnell College.

This tutorial was reviewed by <a href="https://www.grinnell.edu/users/donovang">Gina Donovan</a> (Instructional Technologist, Grinnell College).

This tutorial is adapted from <a href="http://history2016.doingdh.org/voyant-tutorial/">Doing Digital History’s Voyant tutorial</a>.

<a href="http://creativecommons.org/licenses/by-nc/4.0/" rel="license"><img style="border-width: 0;" src="https://i.creativecommons.org/l/by-nc/4.0/88x31.png" alt="Creative Commons License" /></a>
Introduction to Textual Analysis (Voyant Tools) is licensed under a <a href="http://creativecommons.org/licenses/by-nc/4.0/" rel="license">Creative Commons Attribution-NonCommercial 4.0 International License</a>.

## Text Analysis With AntConc

This tutorial was originally written by Katherine Walden, when she was working as a Digital Liberal Arts Specialist at Grinnell College. The tutorial framework was created by Sarah Purcell (L.F. Parker Professor of History, Grinnell College) and Papa Ampim-Darko, a student research assistant at Grinnell College

This tutorial was reviewed by <a href="https://www.grinnell.edu/users/donovang">Gina Donovan</a> (Instructional Technologist. Grinnell College).

This tutorial is adapted from the Programming Historian’s <a href="https://programminghistorian.org/en/lessons/corpus-analysis-with-antconc">Corpus Analysis with AntConc tutorial</a>.

<a href="http://creativecommons.org/licenses/by-nc/4.0/" rel="license"><img style="border-width: 0;" src="https://i.creativecommons.org/l/by-nc/4.0/88x31.png" alt="Creative Commons License" /></a>
Text Analysis in AntConc is licensed under a <a href="http://creativecommons.org/licenses/by-nc/4.0/" rel="license">Creative Commons Attribution-NonCommercial 4.0 International License</a>.

# Table of Contents

- [Background](#background)
- [University Archive Digital Collections](#university-archive-digital-collections)
- [Voyant Tools](#voyant-tools)
  * [Uploading Data](#uploading-data)
  * [Voyant Interface](#voyant-interface)
  * [Voyant's Tools](#voyants-tools)
    * [Cirrus](#cirrus)
    * [Reader](#reader)
    * [Trends](#trends)
    * [Summary](#summary)
    * [Contexts](#contexts)
  * [Interacting With Voyant Tools](#interacting-with-voyant-tools)
  * [Exporting in Voyant](#exporting-in-voyant)
  * [Final Voyant Reflection Questions](#final-voyant-reflection-questions)
- [DataBasic](#databasic)
  * [WordCounter](#wordcounter)
  * [SameDiff](#samediff)
- [Distant Reader](#on-your-own-distant-reader)
   * [Reflection Questions](#distant-reader-reflection-questions)
   * [For More on Distant Reader](#for-more-on-distant-reader-including-more-advanced-on-campus-workshops)
- [AntConc](#antconc)
  * [Data](#data)
  * [Downloading AntConc and Loading Data](#downloading-antconc-and-loading-data)
  * [AntConc's Functionality](#antconcs-functionality)
    * [Searching Key Words in Context](#searching-key-words-in-context)
    * [Visualizing Key Words in Context](#visualizing-key-words-in-context)
    * [Search Operators](#search-operators)
    * [Clusters and N-Grams](#clusters-and-n-grams)
    * [Exporting in AntConc ]#exporting-in-antconc)
    * [Collocates and Word Lists](#collocates-and-word-lists)
    * [Reflection Questions](#antconc-reflection-questions)
- [Python](#python)
- [Next Steps](next-steps)
- [Lab Notebook Components](#lab-notebook-components)     

[Link to Google Drive folder with lab materials and resources, including notebook template](https://drive.google.com/drive/folders/1ewsgmrPNeWJYzi5f8EXr05VjPnlRCATz?usp=sharing) (ND Users)

# Background

To prepare for this lab, we read Kirsten Bussière's “[Chapter 4- Text Analysis](https://carletonu.pressbooks.pub/digh5000/chapter/chapter-4-text-analysis/)” in *Digital Humanities: A Primer* (Carleton University) and explored Alex Wermer-Colan's "[Computational Text Analysis](https://guides.temple.edu/corpusanalysis)" Temple University Library Guide.

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

<a href="http://voyant-tools.org/">Voyant Tools</a> is an open-source web application developed by Stéfan Sinclair and Geoffrey Rockwell in 2003, with later contributions added by Andrew MacDonald, Cyril Briquet, Lisa Goddard, and Mark Turcato. While Voyant is one of the leading robust web-based textual analysis interfaces, it grew out of existing text analysis tools like HyperPo, Tapoware, and TACT. Voyant also offers <a href="https://github.com/sgsinclair/Voyant">open-source code</a> that can be used to deploy the program on a server. Voyant users can upload text files from their computer, link to online text sources, or scrape the text off a webpage for analysis and visualization. Unlike more advanced, programming-oriented textual analysis programs like R and R Studio, Voyant gives users access to a range statistical analysis and visualization features without requiring significant technical knowledge.

## Uploading Data

1-*Note: Images and screenshots included in this tutorial are from a sample corpus and do not reflect what you will see working with different texts.*

2-Open a web browser (preferably Firefox or Chrome) and navigate to the <a href="http://voyant-tools.org/">Voyant Tools homepage</a>.

<p align="center"><a href="https://github.com/kwaldenphd/Voyant-tutorial/blob/master/screenshots/Capture_1.PNG?raw=true"><img class="aligncenter size-large wp-image-549" src="https://github.com/kwaldenphd/Voyant-tutorial/blob/master/screenshots/Capture_1.PNG?raw=true" alt="" width="676" height="523" /></a></p>

3-Upload the PDF you explored in the previous section of the lab and click Reveal.
  * If you want to work with a collection of texts, download the zip folder included in this repository and upload that to Voyant. The zip folder includes Scholastic football review issues from 1901-1931. [Link to access this corpus via Google Drive](https://drive.google.com/drive/folders/1zK99DK_Cd-w9tu2u2M5vlAOSidZYdVTd?usp=sharing)

<p align="center"><a href="https://github.com/kwaldenphd/Voyant-tutorial/blob/master/screenshots/Capture_2.PNG?raw=true"><img class="aligncenter size-large wp-image-550" src="https://github.com/kwaldenphd/Voyant-tutorial/blob/master/screenshots/Capture_2.PNG?raw=true" alt="" width="676" height="355" /></a></p>

4-Once a text or corpus has been uploaded, Voyant moves into its ‘default skin,’ or primary editing environment.

5-Without clicking on any of the page elements, scan the page.

**Reflection questions:**
- What do you immediately notice after uploading a text to Voyant?
- What stands out, or catches your attention?
- What types of information are contained in this page?
- What do you have questions about, or what is confusing and not immediately clear?
- Based on your initial scan, what function do you think these various components serve?

## Voyant Interface

6-In the default editing environment, Voyant displays five panels: Cirrus, Reader, Trends, Summary, and Contexts.

7-Each panel is a tool, and all the panel tools interact with each other. Modifying or interacting with one tool will update the others.

<p align="center"><a href="https://github.com/kwaldenphd/Voyant-tutorial/blob/master/screenshots/Capture_3.PNG?raw=true"><img class="aligncenter wp-image-551" src="https://github.com/kwaldenphd/Voyant-tutorial/blob/master/screenshots/Capture_3.PNG?raw=true" alt="" width="154" height="43" /></a></p>

8-Each panel tool offers additional display and export options, which can be accessed by placing your cursor over the ? symbol. From left to right:
- Export—opens a pop-up window with export and sharing options.
- Choose another tool—opens a dropdown with other tools that be displayed in the panel space.
- Options—opens a pop-up window with additional options for a specific tool.
- Additional information—provides a description of the tool’s functionality and possible uses.

9-Most tool panels in Voyant also include a search bar.

## Voyant’s Tools

Reflection questions to consider as you explore the different tools and panels:
- What differences do you notice across the tools/panels- how are they similar, how are they different?
- What words or features stood out in each representation of the textual analysis?
- How did you understand the textual analysis differently based on how it was presented? 
- What questions do you have about how this tool calculated these results (or what can we tell about how the tool is calculating results/generating visualizations)? 
- What questions do you have about the textual data after exploring this tool?

### Cirrus

<p align="center"><a href="https://github.com/kwaldenphd/Voyant-tutorial/blob/master/screenshots/Capture_4.PNG?raw=true"><img class="aligncenter size-full wp-image-552" src="https://github.com/kwaldenphd/Voyant-tutorial/blob/master/screenshots/Capture_4.PNG?raw=true" alt="" width="635" height="543" /></a></p>

10-Cirrus (top left-hand corner of the page): Cirrus visualizes a word cloud of words contained in the uploaded text. Words that are larger in size and closer to the center of the visualization appear with greater frequency in the text.

<p align="center"><a href="https://github.com/kwaldenphd/Voyant-tutorial/blob/master/screenshots/Capture_9.PNG?raw=true"><img class="aligncenter size-full wp-image-557" src="https://github.com/kwaldenphd/Voyant-tutorial/blob/master/screenshots/Capture_9.PNG?raw=true" alt="" width="647" height="546" /></a></p>

11-The default Cirrus view displays a visualization of word count calculation. 

12- Clicking on the table icon labeled Terms switches from the word cloud to a table view of word counts and frequency trends.

<p align="center"><a href="https://github.com/kwaldenphd/Voyant-tutorial/blob/master/screenshots/Capture_10.PNG?raw=true">><img class="aligncenter size-full wp-image-558" src="https://github.com/kwaldenphd/Voyant-tutorial/blob/master/screenshots/Capture_10.PNG?raw=true" alt="" width="630" height="544" /></a></p>

13- The Links icon visualizes relationships between words by presenting a network visualization of connected terms, or words that appear in relation or proximity to each other.

### Reader

<p align="center"><a href="https://github.com/kwaldenphd/Voyant-tutorial/blob/master/screenshots/Capture_5.PNG?raw=true"><img class="aligncenter size-full wp-image-553" src="https://github.com/kwaldenphd/Voyant-tutorial/blob/master/screenshots/Capture_5.PNG?raw=true" alt="" width="652" height="520" /></a></p>

14-Reader (top middle of the page): Reader is a text reader that displays the original text. Moving the mouse over a word in the reader will highlight the word and display its frequency count.

<p align="center"><a href="https://github.com/kwaldenphd/Voyant-tutorial/blob/master/screenshots/Capture_11.PNG?raw=true"><img class="aligncenter size-full wp-image-559" src="https://github.com/kwaldenphd/Voyant-tutorial/blob/master/screenshots/Capture_11.PNG?raw=true" alt="" width="645" height="551" /></a></p>

15-Like with Cirrus, Reader offers additional panel views. 

16- Clicking on the circle icon labeled TermsBerry switches the panel to a visualization of term frequency and proximity. Hovering over a bubble with highlight the term, calculate the number of times it appears in the text, and indicate what terms most frequently appear to the right and left of the selected term in the  text.

### Trends

<p align="center"><a href="https://github.com/kwaldenphd/Voyant-tutorial/blob/master/screenshots/Capture_6.PNG?raw=true"><img class="aligncenter size-full wp-image-554" src="https://github.com/kwaldenphd/Voyant-tutorial/blob/master/screenshots/Capture_6.PNG?raw=true" alt="" width="642" height="504" /></a></p>

17-Trends uses a line graph visualization to show the distribution of terms and relative term frequency across the text. The legend will define the most frequently-appearing terms in the text, and the graph illustrates where and how frequently they appear in the text. Hovering over a graph point highlights a term, displays its relative frequency calculation, as well as the source text for that calculation.

<p align="center"><a href="https://github.com/kwaldenphd/Voyant-tutorial/blob/master/screenshots/Capture_13.PNG?raw=true"><img class="aligncenter size-full wp-image-561" src="https://github.com/kwaldenphd/Voyant-tutorial/blob/master/screenshots/Capture_13.PNG?raw=true" alt="" width="963" height="368" /></a></p>

18-Clicking on the table icon labeled Document Terms shows the frequency and proportion counts as a data table.

### Summary

<p align="center"><a href="https://github.com/kwaldenphd/Voyant-tutorial/blob/master/screenshots/Capture_7.PNG?raw=true"><img class="aligncenter size-full wp-image-555" src="https://github.com/kwaldenphd/Voyant-tutorial/blob/master/screenshots/Capture_7.PNG?raw=true" alt="" width="962" height="365" /></a></p>

19-Summary provides information about the corpus, including the number of documents, words, and unique terms. 

20-Summary also calculates document length, vocabulary density, average words per sentence, and most frequently-occurring terms.

<p align="center"><a href="https://github.com/kwaldenphd/Voyant-tutorial/blob/master/screenshots/Capture_13.PNG?raw=true"><img class="aligncenter size-full wp-image-561" src="https://github.com/kwaldenphd/Voyant-tutorial/blob/master/screenshots/Capture_13.PNG?raw=true" alt="" width="963" height="368" /></a></p>

21-Clicking on the table icon labeled Documents shows the word count, unique term, word count ratio, and words per sentence calculated data in tabular form.

<p align="center"><a href="https://github.com/kwaldenphd/Voyant-tutorial/blob/master/screenshots/Capture_14.PNG?raw=true"><img class="aligncenter size-full wp-image-562" src="https://github.com/kwaldenphd/Voyant-tutorial/blob/master/screenshots/Capture_14.PNG?raw=true" alt="" width="966" height="369" /></a></p>

22-Clicking on the table icon labeled Phrases shows the number of times a particular phrase appears in the text, as well as the phrase length and document location.

### Contexts

<a href="https://github.com/kwaldenphd/Voyant-tutorial/blob/master/screenshots/Capture_8.PNG?raw=true"><img class="aligncenter size-full wp-image-556" src="https://github.com/kwaldenphd/Voyant-tutorial/blob/master/screenshots/Capture_8.PNG?raw=true" alt="" width="959" height="370" /></a>

23-Contexts identifies the most frequently-occurring terms and shows the text that appears to the left and right of the term in the text.

24-Clicking on the table icon labeled Correlations shows how frequently a specific term appear next to or near another term by calculating correlation and significance measures.

## Interacting with Voyant Tools

25-Up to this point, we have been interacting with each panel tool individually. Now we will explore how the panel tools interact.

26-Select a panel tool, and click on a term, data point, or other interactive element within the panel tool. 

27-What changes in that panel after you click? What changes happen in the other panels? How does the analysis in each tool change based on how you interact with the data analysis and visualization?

28-Refresh the browser page, and select another panel tool. Use the search function to look for a term in the text. What changes in that panel after you search? What changes happen in the other panels? How does the analysis in each tool change based on how you interact with the search function?

29-What do you find useful about the interactive analysis and visualization tools? What do you find frustrating, unclear, or confusing? How does interacting with a tool change or impact your understanding of the text? What additional questions do you have about the text (or tool)?

## Exporting in Voyant

30-We briefly mentioned export options when introducing you to the editing interface. Voyant gives you the option to share an entire editing interface view. Move your cursor over the question mark icon in the top-right hand corner of the page to explore this option.

31-Voyant also gives you the option to export or share the data or visualization created in a specific panel tool. Again, move your cursor over the question mark icon in the top right-hand corner of a specific panel to explore this option.

## Final Voyant Reflection Questions

- What did you find engaging or interesting about Voyant Tools?
- What types of historical research questions could a researcher have about a text or collection of texts?
- How effectively might Voyant be able to address those questions?
- What challenges, frustrations, or limitations did you encounter while using Voyant?
- What remaining questions do you have about the source you focused on?
- How would you move forward with Voyant as a tool for historical textual analysis?

# DataBasic

Another web-based tool for text analysis that we'll explore is DataBasic.

According to [its website,](https://databasic.io) “DataBasic is a suite of easy-to-use web tools for beginners that introduce concepts of working with data. These simple tools make it easy to work with data in fun ways, so you can learn how to find great stories to tell.” DataBasic is developed and supported by MIT’s [Center for Civic Media](https://civic.mit.edu/) and Emerson College’s [Engagement Lab.](https://elab.emerson.edu/) 

*Note: Images and screenshots included in this tutorial are from a sample corpus and do not reflect what you will see working with different texts*

<p align="center"><img class=" size-full wp-image-53 aligncenter" src="https://github.com/kwaldenphd/DataBasic-tutorial/blob/master/screenshots/Capture_1.jpg?raw=true" alt="Capture" /></p>

32-Navigate to https://databasic.io/ in a web browser (preferably Chrome). 

## WordCounter

<p align="center"><img class=" size-full wp-image-53 aligncenter" src="https://github.com/kwaldenphd/DataBasic-tutorial/blob/master/screenshots/Capture_4.jpg?raw=true" alt="Capture" /></p>

33-Click on the WordCounter icon to open the WordCounter tool. 

34-As described on the page, “WordCounter analyzes your text and tells you the most common words and phrases. This tool helps you count words, bigrams, and trigrams in plain text. This is often the first step in quantitative text analysis.”

35-Bigrams are two-word phrases or expressions. Trigrams are three-word phrases or expressions.

36-WordCounter gives you the option to use a sample text, paste in your own text, upload a file, or load text from a URL.

<p align="center"><img class=" size-full wp-image-53 aligncenter" src="https://github.com/kwaldenphd/DataBasic-tutorial/blob/master/screenshots/Capture_5.jpg?raw=true" alt="Capture" /></p>

37-Download a plain-text file for one of the Scholastic football reviews. [Link to Google Drive folder with sample files](https://drive.google.com/drive/folders/1zK99DK_Cd-w9tu2u2M5vlAOSidZYdVTd?usp=sharing).

<p align="center"><img class=" size-full wp-image-53 aligncenter" src="https://github.com/kwaldenphd/DataBasic-tutorial/blob/master/screenshots/Capture_6.jpg?raw=true" alt="Capture" /></p>

38-The default options selected in WordCounter will analyze the text without considering capitalization and stopwords.

39-Stopwords are commonly used words. English-language examples include “and,” “the”, and “this.”

40-Leave both options selected and click the Count icon.

<p align="center"><img class=" size-full wp-image-53 aligncenter" src="https://github.com/kwaldenphd/DataBasic-tutorial/blob/master/screenshots/Capture_7.jpg?raw=true" alt="Capture" /></p>

41-The first visualization generated by WordCount is a word cloud of the most frequently occurring terms in the document you uploaded. Hover over specific words with your cursor to see how many times they appear in the document.

42-<p align="center"><img class=" size-full wp-image-53 aligncenter" src="https://github.com/kwaldenphd/DataBasic-tutorial/blob/master/screenshots/Capture_8.jpg?raw=true" alt="Capture" /></p>

43-The tables below the word cloud on the results page include a list of words that appear most frequently in the document. WordCount has also generated a table with a list of bigrams and trigrams, as well as how many times they appear in the document.

<p align="center"><img class=" size-full wp-image-53 aligncenter" src="https://github.com/kwaldenphd/DataBasic-tutorial/blob/master/screenshots/Capture_8a.jpg?raw=true" alt="Capture" /></p>

44-You can click on the arrow icon next to any of the table titles to download a CSV (comma-separate value) file with the data contained in that table. This file can be opened in a spreadsheet program like Microsoft Excel.

<blockquote> What is a CSV? 

A comma-separated value file (CSV) is a structured tabular data format in which column values are separated by a comma. Computer programs like Microsoft Excel parse those values and display the underlying data in a spreadsheet format. Saving tabular data as a CSV file type avoids much of the additional formatting added by programs like Microsoft Excel. </blockquote>

<p align="center"><img class=" size-full wp-image-53 aligncenter" src="https://github.com/kwaldenphd/DataBasic-tutorial/blob/master/screenshots/Capture_8c.jpg?raw=true" alt="Capture" /></p>

<p align="center"><img class=" size-full wp-image-53 aligncenter" src="https://github.com/kwaldenphd/DataBasic-tutorial/blob/master/screenshots/Capture_8b.jpg?raw=true" alt="Capture" /></p>

45-You can also click on the arrow icon next to the page title to get a link to your WordCounter results. Your results are available via that link for 60 days.

### Reflection Questions
- What do you notice about the text through the results displayed in WordCounter?
- How does WordCounter’s results shape your understanding of the text?
- What additional questions do you have about the text? Where would you go next using this tool?
- Other comments/questions/observations

## SameDiff

<p align="center"><img class=" size-full wp-image-53 aligncenter" src="https://github.com/kwaldenphd/DataBasic-tutorial/blob/master/screenshots/Capture_1.jpg?raw=true" alt="Capture" /></p>

46-Navigate back to the [DataBasic home page.](https://databasic.io)

<p align="center"><img class=" size-full wp-image-53 aligncenter" src="https://github.com/kwaldenphd/DataBasic-tutorial/blob/master/screenshots/Capture_9.PNG?raw=true" alt="Capture" /></p>

47-Click on the SameDiff icon to open the SameDiff tool.

48-As described on the page, “SameDiff compares two or more text files and tells you how similar or different they are. SameDiff compares one...text to another….to show you similarities and differences. It uses a cosine similarity algorithm to rate whether the documents are really similar or totally different.”

49-SameDiff gives you the option to use provided sample texts or upload your own documents.

50-We can use the tool to compare texts that represented different time periods or themes. We can also use this tool to compare a single text with a larger group of texts (or a corpus).

<p align="center"><img class=" size-full wp-image-53 aligncenter" src="https://github.com/kwaldenphd/DataBasic-tutorial/blob/master/screenshots/Capture_10.PNG?raw=true" alt="Capture" /></p>

51-Take the single text file you used in the previous section of the lab, and compare it with the combined Scholastic football reviews from 1901-1931 (file name `Scholastic-Combined.txt`, [Link to download from Google Drive](https://drive.google.com/file/d/1Law1fb8c1xZOdwLyNCO-p3opI020kovn/view?usp=sharing)).

52-Click the Compare icon. 

<p align="center"><img class=" size-full wp-image-53 aligncenter" src="https://github.com/kwaldenphd/DataBasic-tutorial/blob/master/screenshots/Capture_11.PNG?raw=true" alt="Capture" /></p>

53-The SameDiff report page summarizes the relative similarity of the documents you are comparing and provides a cosine similarity score.

54-The Cosine Similarity Score uses an algorithm to calculate the similarity of two documents based on the number of times words across the documents.

55-The three columns show what terms the two documents have in common, as well as what words are unique to each document. 

<p align="center"><img class=" size-full wp-image-53 aligncenter" src="https://github.com/kwaldenphd/DataBasic-tutorial/blob/master/screenshots/Capture_12a.png?raw=true" alt="Capture" /></p>

56-You can click on the circle arrow icon to download a CSV file with your SameDiff results. The square arrow icon will give you a link to share your results (which will be saved for 60 days).

<p align="center"><img class=" size-full wp-image-53 aligncenter" src="https://github.com/kwaldenphd/DataBasic-tutorial/blob/master/screenshots/Capture_12.PNG?raw=true" alt="Capture" /></p>

### Reflection Questions

- What do you notice about the individual text and the combined texts through the results displayed in SameDiff?
- How do the SameDiff results shape your understanding of the individual text and combined text?
- What additional questions do you have about these resources? Where would you go next using this tool? 
- Other comments/questions/observations

# ON YOUR OWN: Distant Reader

"The Distant Reader takes text as input, does analysis against it, and outputs sets of structured data called 'study carrels', which students, researchers, or scholars can use to do both close and distant reading...[it is] a tool intended to supplement the traditional reading process. Given a set of one or more texts acquired through a variety of means, the Reader: 1) applies different forms of text mining and natural language processing against the texts, 2) saves the results as a set of structured data amenable to computing, 3) summarizes everything in a set of interactive HTML reports, 4) compresses everything into a .zip file, and 5) provides the means for you to view the results online or download the whole thing to your computer. This resulting .zip file is affectionately called a 'study carrels."
- Morgan, Eric Lease. (2020, April 10). Distant Reader (Version Alpha). Zenodo. https://doi.org/10.5281/zenodo.3747777.

To learn more about Distant Reader:
- [About](https://distantreader.org/about)
- [Getting Started](https://distantreader.org/getting-started)

57-You will need to have or create an ORCID to use Distant Reader.
- [Link to register](https://orcid.org/register)

58-Once you have an ORCID, log in to Distant Reader.

59-Let's create a carrel for the scholastic football review materials:
- Click on the "Create Carrels" menu item on the top of the page.
- Select the option to create a "New Carrel."
- Select the "Zip file" option
- Give your carrel a name
- Upload the `zip` folder of scholastic football reviews from 1901-1931 ([Link to download from Google Drive](https://drive.google.com/drive/folders/1zK99DK_Cd-w9tu2u2M5vlAOSidZYdVTd?usp=sharing)
- Click the "Create" button

60-The process of creating a carrel will take some time. Give it a few hours, come back, and you should see the new carrel under "Browse Carrels" and "Browse Your Carrels."

61-Once the carrel has been processed, you can click the "View" option to see Distant Reader's analysis of your text.

62-Spend some time exploring the carrel analysis and visualization.

## Distant Reader Reflection Questions

- What did you find engaging or interesting about Distant Reader?
- What types of historical research questions could a researcher have about a text or collection of texts?
- How effectively might Distant Reader be able to address those questions?
- What challenges, frustrations, or limitations did you encounter while using Distant Reader?
- What words or features stood out in each representation of the textual analysis?
- How did you understand the textual analysis differently based on how it was presented? 
- What questions do you have about how this tool calculated these results (or what can we tell about how the tool is calculating results/generating visualizations)? 
- What remaining questions do you have about the source you focused on?
- How would you move forward with Distant Reader as a tool for historical textual analysis?
- Other questions/observations

## For More on Distant Reader (including more advanced on-campus workshops)

Eric Lease Morgan, the lead developer and project coordinator for Distant Reading is the Digital Initiatives Librarian here at ND, in the Navari Family Center for Digital Scholarship.
- [Eric's library profile](https://directory.library.nd.edu/directory/employees/emorgan)

He teaches a number of specialized workshops on text mining and data analysis, including some that go into greater depth with Distant Reader.

A list of his Fall 2021 workshops:
- [Introduction to Text Mining, Tuesday 9/21, 11am-12pm](https://library.nd.edu/event/introduction-to-text-mining-2021-09-21)
- [Using the Distant Reader, multiple dates/times](https://library.nd.edu/events/recurring/using-the-distant-reader-fall-2021)
- [Preparing Files for Text and Data Mining, Friday 9/24, 12:30-1:30pm](https://library.nd.edu/event/preparing-files-for-text-and-data-mining-2021-09-24)
- [Using Topic Modeling Against a Corpora, Wednesday 9/29, 12:30-1:30pm](https://library.nd.edu/event/using-topic-modeling-against-a-corpora-2021-09-29)
- [Extracting the Who, What, and When from a Text, Monday 10/4, 12:30-1:30pm](https://library.nd.edu/event/extracting-the-who-what-when-from-a-text-2021-10-04)
- [Using a Concordance with AntConc, Wednesday 10/6, 12:30-1:30pm](https://library.nd.edu/event/using-a-concordance-2021-10-06)
- [Introduction to Natural Language Processing With Python, Tuesday 10/12, 11am-12pm](https://library.nd.edu/event/introduction-to-natural-language-processing-with-python-2021-10-12)

# AntConc

Developed by Laurence Anthony, <a href="http://www.laurenceanthony.net/software/antconc/">AntConc</a> is a free, closed-source program that runs on Windows, OS, and Linux. At the most basic level, AntConc is a concordancer, or a program that constructs a concordance based on terms in a text or collection of texts. AntConc also allows users to visualize concordance calculations and generate word and keyword lists based on terms present in the text. AntConc also supports cluster and collocation analysis and visualization. With Voyant, we explored a web-based graphical user interface option for conducting textual analysis, with a particular emphasis on visualization. AntConc is a software program (that runs on your own computer) that focuses more on corpus linguistics and statistical analysis methods.

## Data

64- Download the zip folder that includes Scholastic football reviews from 1901-1931 ([link to access this corpus via Google Drive](https://drive.google.com/drive/folders/1zK99DK_Cd-w9tu2u2M5vlAOSidZYdVTd?usp=sharing)). Extract the folder contents on your computer.
- PC users- open File Explorer (folder icon), right click on the zip folder (likely in Downloads), and click "Extract"
- Mac users- click on the zip folder

## Downloading AntConc and Loading Data

65-To download AntConc on your own computer, navigate to [the project website](http://www.laurenceanthony.net/software/antconc/), select the appropriate version for your operating system, and follow the installation instructions.
- NOTE: If at all possible, try to have AntConc installed on your computer for class Thursday 9/16. 

<p align="center"><a href="https://github.com/kwaldenphd/AntConc-tutorial/blob/master/screenshots/Capture_1.PNG?raw=true"><img class="aligncenter size-full wp-image-583" src="https://github.com/kwaldenphd/AntConc-tutorial/blob/master/screenshots/Capture_1.PNG?raw=true" alt="" width="790" height="592" /></a></p>

66-You can launch AntConc by double clicking on the Desktop icon or searching for the program in the Start menu.

67-AntConc allows you to open <strong>single files</strong>, as well as open an entire <strong>file directory</strong>. For this tutorial, we will be working with a large number of text files, so opening the directory makes more sense than loading these files individually.

68-[Link to Google Drive folder where you can download plain-text files](https://drive.google.com/drive/folders/1zK99DK_Cd-w9tu2u2M5vlAOSidZYdVTd?usp=sharing).

*Note: Images and screenshots included in this tutorial are from a sample corpus and do not reflect what you will see working with different texts*

<p align="center"><a href="https://github.com/kwaldenphd/AntConc-tutorial/blob/master/screenshots/Capture_2.PNG?raw=true"><img class="aligncenter size-full wp-image-584" src="https://github.com/kwaldenphd/AntConc-tutorial/blob/master/screenshots/Capture_2.PNG?raw=true" alt="" width="790" height="594" /></a></p>

69-To load the directory (or folder) of Scholastic football review files into AntConc:
  * Click the "File" menu option
  * Select "Open Dir"
  * In the pop-up window, navigate to the folder where you downloaded and extracted the Scholastic football review files
  * Click "OK"

70-The loaded files will be listed on the left-hand window in AntConc, and the total number of files will display at the bottom of that window.

## AntConc’s Functionality

<p align="center"><a href="https://github.com/kwaldenphd/AntConc-tutorial/blob/master/screenshots/Capture_3.PNG?raw=true"><img class="aligncenter size-full wp-image-585" src="https://github.com/kwaldenphd/AntConc-tutorial/blob/master/screenshots/Capture_3.PNG?raw=true" alt="" width="551" height="35" /></a></p>

71-The main AntConc screen gives you access to seven different textual analysis tools.

- **Concordance** searches for and displays keywords in context (KWIC).
- **Concordance Plot** presents a preliminary, basic visualization of a KWIC search.
- **File View** is like the Reader panel in Voyant—it shows you a full file view to see a search result in the larger context of a text.
- **Clusters** highlights terms that appear together frequently in the text.
- **Collocates** calculates the statistical likelihood of terms appearing together in the text. 
  * Clusters looks for term patterns as they are represented in the text. Collocates looks at the likelihood of terms appearing together in the text.
- **Word List** calculates how frequency words appear in your text.
- **Keyword List** compares keywords from two text sources (a reference text and an analysis text).

### Searching Keywords in Context

72-AntConc (and other computing tools) excel at identifying patterns in language that are not always detected by the average reader. 

73-For example, function words like *a, an, the, he, she, I* (often called stopwords in textual analysis) don’t frequently catch our attention as readers. 

74-A computational tool focuses on analyzing the words as term objects, rather than interpreting them based on meaning, context, or function.

<p align="center"><a href="https://github.com/kwaldenphd/AntConc-tutorial/blob/master/screenshots/Capture_4.PNG?raw=true"><img class="aligncenter size-full wp-image-586" src="https://github.com/kwaldenphd/AntConc-tutorial/blob/master/screenshots/Capture_4.PNG?raw=true" alt="" width="789" height="593" /></a></p>

75-Type "the" in the Search Term box at the bottom of the Concordance window and click "Start."

76-The Concordance shows key words in context (KWIC), with the search term highlighted.

77-The KWIC Sort options allow you to change how AntConc displays or sorts the context for your search term. 
- `1R` includes the term immediately to the right of your search term, `2R` includes the second term to the right from your search term, etc.
- `1L` includes the term immediately to the left of your search term, `2L` includes the second term to the left from your search term, etc.

78-Experiment with different KWIC Sort options, and click the "Sort" icon to see updated results.

79-Reflection questions:
- How did your search results change? 
- What happens if you continue to customize or edit the Kwic Sort options? 
- How do you understand a key word differently based on how you tell the program to calculate context?

### Visualizing Keywords in Context

<p align="center"><a href="https://github.com/kwaldenphd/AntConc-tutorial/blob/master/screenshots/Capture_5.PNG?raw=true"><img class="aligncenter size-full wp-image-576" src="https://github.com/kwaldenphd/AntConc-tutorial/blob/master/screenshots/Capture_5.PNG?raw=true" alt="" width="790" height="595" /></a></p>

80-Search for a "ball" in the Concordance Tab.

81-Once your search has loaded, click on the "Concordance Plot" tab to visualize your search results.

82-Each instance of the keyword is represented as a vertical black line. AntConc visualizes how keyword appearances are distributed across each file in the Corpus Files.

<p align="center"><a href="https://github.com/kwaldenphd/AntConc-tutorial/blob/master/screenshots/Capture_6.PNG?raw=true"><img class="aligncenter size-full wp-image-577" src="https://github.com/kwaldenphd/AntConc-tutorial/blob/master/screenshots/Capture_6.PNG?raw=true" alt="" width="791" height="598" /></a></p>

83-Clicking on a specific line takes you to that passage of the text in "File View."

84-Reflection questions:
- How useful do you find these preliminary visualizations? 
- How do they compare to the types of visualizations generated on Voyant? 
- How do these visualizations impact your understanding of the text? 
- What questions do you have based on these visualizations?

### Search Operators

85-If you’re familiar with Boolean searching or Regular Expressions, you know symbols can be used in a search to customize or focus your search results. AntConc uses a series of wildcard operators to allow you to further customize your search.

<p align="center"><a href="https://github.com/kwaldenphd/AntConc-tutorial/blob/master/screenshots/Capture_7.PNG?raw=true"><img class="aligncenter size-full wp-image-578" src="https://github.com/kwaldenphd/AntConc-tutorial/blob/master/screenshots/Capture_7.PNG?raw=true" alt="" width="788" height="579" /></a></p>

86-Go to the "Global Settings" menu option, and select "Wildcard Settings" to view or edit the full list of available wildcard operators.

87-Search for `m?n` and `wom?n` and compare your results.

88-A few notes on operators:
- The `*` operator is often used in Boolean searching.
- The `?` operator is more specific because it stands in for only one character. 
- For example, searching `m*n` will bring back results that include `men`, `mean`, `mellon`, etc. 
- Searching `m?n`  will return `men`, `man`, and `min`. 
- Similarly, `wom?n` will return `woman` and `women`.

### Clusters and N-Grams

<p align="center"><a href="https://github.com/kwaldenphd/AntConc-tutorial/blob/master/screenshots/Capture_8.PNG?raw=true"><img class="aligncenter size-full wp-image-579" src="https://github.com/kwaldenphd/AntConc-tutorial/blob/master/screenshots/Capture_8.PNG?raw=true" alt="" width="791" height="597" /></a></p>

89-Click on the Clusters/N-Grams tab and search for "sport."

90-AntConc ranks your search results, calculates frequency, and range (number of files in which the cluster appears), while also displaying the text in the cluster.

<p align="center"><a href="https://github.com/kwaldenphd/AntConc-tutorial/blob/master/screenshots/Capture_9.PNG?raw=true"><img class="aligncenter size-full wp-image-580" src="https://github.com/kwaldenphd/AntConc-tutorial/blob/master/screenshots/Capture_9.PNG?raw=true" alt="" width="790" height="595" /></a></p>

91-The default Search Term Position places the search term on the left side of the cluster. Change the Search Term Position selection to "On Right" and click "Start" to re-run the search. How do your search results change?

92-Cluster Size determines the range for the number of terms AntConc searches and displays. How are your search results different when you change this range?

## Exporting in AntConc

93-After you are satisfied with a search result, click the "File" menu option and then "Save Output" to save the search result as a plain-text (`.txt`) file.

94-Save the file as `SEARCHTERM_cluster_search` or another descriptive name.

95-Conduct another Cluster search for a keyword of your choosing. Customize your results, and export the results as a text (`.txt`) file.

96-Open the exported file in a text editor (Notepad or Notepad++ for PC users and Text Edit for Mac users) to explore the exported results.

## Collocates and Word Lists

97-As mentioned earlier in the tutorial, Clusters analyzes what words appear most frequently alongside your search term.

98-Collocates calculates what terms are statistically probable to appear near your search term. 
- **Freq** calculates overall frequency
- **Freq(L)** looks at frequency for terms to the left of your search term
- **Freq(R)** calculates frequency for terms to the right of your search term
- **Stat** uses the Mutual Information (MI) and T-score calculations outlined in Michael Stubbs's 1995 article "On inference theories and code theories: Corpus evidnece for semantic schemas" to calculate the statistical probability of term collocation.
  * Michael Stubbs, "[On inference theories and code theories: Corpus evidnece for semantic schemas](http://people.cs.pitt.edu/~wiebe/courses/CS3730/Spring05/stubbs01.pdf)" *Text* 21:3 (1995): 437-465.

<p align="center"><a href="https://github.com/kwaldenphd/AntConc-tutorial/blob/master/screenshots/Capture_11.PNG?raw=true"><img class="aligncenter size-full wp-image-582" src="https://github.com/kwaldenphd/AntConc-tutorial/blob/master/screenshots/Capture_11.PNG?raw=true" alt="" width="791" height="597" /></a></p>

99-Use the name of a historic campus figure or building as your search term.
- "Rockne" is a good place to start.

100-AntConc will display a pop-up window message about needing to generate a Word List. Click "OK" to have AntConc generate that list automatically.

101-Reflection questions:
- What terms are statistically likely to appear in proximity to your search term?
- What happens when you change the Window Span (number of words to the right and left of your search term AntConc will include in the analysis)?

## AntConc Reflection Questions

- What do you notice is similar about Voyant Tools and AntConc as digital tools for textual analysis? What are the differences?
- Which did you prefer working with (and how/why)?
- How was your understanding of the text impacted by the analysis we did in AntConc? What questions do you still have?
- What would be some of your next steps for conducting textual analysis related to Notre Dame football, using Voyant or AntConc?
- What types of historical research questions can you see textual analysis being useful to answer or respond to (especially related to the conversations we've been having about college football/ND football)?

# Python

PLACEHOLDER TEXT

# Next Steps

PLACEHOLDER TEXT

# Lab Notebook Components

PLACEHOLDER TEXT
