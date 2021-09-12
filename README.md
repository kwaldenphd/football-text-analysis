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

## Text and Data Mining for ND Archive Materials

Any text and data mining endeavor is supported by heroic and ongoing work that happens at the nexus of digital infrastructure, archives/special collections, metadata, digital preservation. The workflows outlined in this project would not be possible without significant past, present, and ongoing work from colleagues in the University of Notre Dame Libraries, specifically (but not exclusively)...
- [University Archives](http://archives.nd.edu/) (Patrick Milhoan, Scott Kirycki, Joseph Smith, and Matthew Wilken)
- [Rare Books and Special Collections](https://rarebooks.library.nd.edu/) (Rachel Bohlmann, Tracy Bergstrom, Sara Weber)
- [Navari Family Center for Digital Scholarship](https://cds.library.nd.edu/) (Daniel Johnson, Eric Lease Morgan, Matthew Sisk)
- [Metadata Services](https://cds.library.nd.edu/expertise/Digitization.shtml) (Peggy Griesinger)
- [Digital Services](https://directory.library.nd.edu/directory/departments/1195) (Mikala Narlock)

# Table of Contents

## Abbreviated Table of Contents

- [Background](#background)
- [University Archive Digital Collections](#university-archive-digital-collections)
- [Voyant Tools](#voyant-tools)
  * [Uploading Data](#uploading-data)
  * [Voyant Interface](#voyant-interface)
  * [Voyant's Tools](#voyants-tools)
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
- [Python](#python)
  * [Bulk Download](#bulk-download)
  * [Optical Character Recognition](#optical-character-recognition)
  * [Text Analysis in Python](#text-analysis-in-python)
- [Next Steps](next-steps)
- [Lab Notebook Components](#lab-notebook-components)     

[Link to Google Drive folder with lab materials and resources, including notebook template](https://drive.google.com/drive/folders/1ewsgmrPNeWJYzi5f8EXr05VjPnlRCATz?usp=sharing) (ND Users)

## Expanded Table of Contents

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
    * [Exporting in AntConc ](#exporting-in-antconc)
    * [Collocates and Word Lists](#collocates-and-word-lists)
    * [Reflection Questions](#antconc-reflection-questions)
- [Python](#python)
  * [Bulk Download](#bulk-download)
    * [Alumnus](#alumnus)
    * [Bagby Glass Plate Negatives](#bagby-glass-plate-negative-collection)
    * [Annual Bulletins and Catalogs](#annual-bulletins-and-catalogs)
    * [Capstan](#capstan)
    * [Commencement Programs](#commencement-programs)
    * [Daily](#daily)
    * [Directories](#directories)
    * [Magazine](#magazine)
    * [Observer](#observer)
    * [Scholastic](#scholastic)
    * [Scholastic Football Review](#scholastic-football-review)
    * [Voice](#voice)
  * [Optical Character Recognition](#optical-character-recognition)
    * [OCR Next Steps and Additional Resources](#ocr-next-steps-and-additional-resources) 
      * [Acrobat Adobe Pro](#acrobat-adobe-pro)
  * [Text Analysis in Python](#text-analysis-in-python)
    * [Python Text Analysis Next Steps and Additional Resources](#python-text-analysis-next-steps-and-additional-resources)
      * [More documentation on the tools covered in this notebook](#more-documentation-on-the-tools-covered-in-this-notebook)
      * [Other Tutorials, Packages, and Methods](#other-tutorials-packages-and-methods)
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

To undertake large-scale text analysis, we would need to be able to download source material in bulk and eventually convert that source material to plain-text formats for various kinds of analysis and visualization in a programming environment.

This section of the lab procedure includes Jupyter notebook (`.ipynb`) files with sample Python workflows for using text and data mining workflows with select collections of digitized material from the [University of Notre Dame Archives](http://archives.nd.edu/).

Each Jupyter Notebook goes into more detail about the sample Python code presented.

# Bulk Download

Prof. Walden has built out Jupyter notebooks for bulk downloading PDFs for the following collections.

## Alumnus

From the [University Archives](http://archives.nd.edu/digital/):
- "The Alumnus, published by the Alumni Association from January of 1923 until December of 1971, provided news and feature articles of interest to Notre Dame graduates. Notre Dame Magazine replaced it starting in 1972."
- [Alumnus Digital Collection](http://archives.nd.edu/Alumnus/)

Jupyter Notebook:
- [GitHub](https://github.com/kwaldenphd/football-text-analysis/blob/main/notebooks/alumnus.ipynb)
- [Jupyter nbviewer](https://nbviewer.jupyter.org/github/kwaldenphd/football-text-analysis/blob/main/notebooks/alumnus.ipynb)
- [Google CoLab](https://drive.google.com/file/d/1ZgGuymWQTX1IeTwWamr88RkPPuOeujS-/view?usp=sharing) *ND users*

## Bagby Glass Plate Negative Collection

From the [University Archives](http://archives.nd.edu/digital/):
- "The Bagby company, a South Bend photographic studio, took pictures of athletes for Notre Dame. The digitized Glass Plate Negative Collection is part of a [larger Bagby collection](http://archives.nd.edu/findaids/ead/xml/bby.xml)."
- [Bagby Glass Plate Negative Collection (Notre Dame Sports), 1920s-1930s](http://archives.nd.edu/Bagby/index.htm/)

Jupyter Notebook:
- [GitHub](https://github.com/kwaldenphd/football-text-analysis/blob/main/notebooks/bagby_negatives.ipynb)
- [Jupyter nbviewer](https://nbviewer.jupyter.org/github/kwaldenphd/football-text-analysis/blob/main/notebooks/bagby_negatives.ipynb)
- [Google CoLab](https://drive.google.com/file/d/1D3_LhB3TcuNOiePnz8VubWpiP2Xl3rzn/view?usp=sharing) *ND users*

## Annual Bulletins and Catalogs

From the [University Archives](http://archives.nd.edu/digital/):
- "Notre Dame's catalogues or bulletins included descriptions of courses, programs, curricula, facilities, and faculty. They generally [listed students](http://archives.nd.edu/bulletin/stdnts.htm) and provided information on [graduation ceremonies](http://archives.nd.edu/bulletin/cmmncmts.htm), degree recipients, and academic prizes won by students."
- [Notre Dame Annual Catalogues or Bulletins, 1850 - 1914](http://archives.nd.edu/bulletin/)

Jupyter Notebook:
- [GitHub](https://github.com/kwaldenphd/football-text-analysis/blob/main/notebooks/bulletins_catalogs.ipynb)
- [Jupyter nbviewer](https://nbviewer.jupyter.org/github/kwaldenphd/football-text-analysis/blob/main/notebooks/bulletins_catalogs.ipynb)
- [Google CoLab](https://drive.google.com/file/d/1cH6qsO5F5kh6KBYhk-rsugraGjt3gs-Z/view?usp=sharing) *ND users*

## Capstan

From the [University Archives](http://archives.nd.edu/digital/):
- "During World War II, the United States Navy trained many officers at Notre Dame. The naval program published its own yearbook, called Capstan."
- [Capstan, 1943-1945, Digital Collection](http://archives.nd.edu/Capstan/)

Jupyter Notebook:
- [GitHub](https://github.com/kwaldenphd/football-text-analysis/blob/main/notebooks/capstan.ipynb)
- [Jupyter nbviewer](https://nbviewer.jupyter.org/github/kwaldenphd/football-text-analysis/blob/main/notebooks/capstan.ipynb)
- [Google CoLab](https://drive.google.com/file/d/1Cssj7PnOnb1XI0WuLKzQLDi5mWSna-E9/view?usp=sharing) *ND users*

## Commencement Programs

From the [University Archives](http://archives.nd.edu/digital/):
- "Programs for graduations at the University of Notre Dame. The number of commencements per year varies. The content of programs also varies, but they generally provide information about graduating students, speakers, related events and ceremonies."
- [Notre Dame Commencement Programs, 1845 - 2018](http://archives.nd.edu/Commencement/)

Jupyter Notebook:
- [GitHub](https://github.com/kwaldenphd/football-text-analysis/blob/main/notebooks/commencement_programs.ipynb)
- [Jupyter nbviewer](https://nbviewer.jupyter.org/github/kwaldenphd/football-text-analysis/blob/main/notebooks/commencement_programs.ipynb)
- [Google CoLab](https://drive.google.com/file/d/1Cssj7PnOnb1XI0WuLKzQLDi5mWSna-E9/view?usp=sharing) *ND users*

## Daily

From the [University Archives](http://archives.nd.edu/digital/):
- "The Notre Dame Daily first appeared on the twentieth of May, 1923. It published thirteen issue in its first volume, concluding at the end of the academic year on the sixth of June. Its second and final volume covered the 1923-1924 academic year in 128 issues beginning on the twenty-third of September and ending on the fifteenth of June."
- [Notre Dame Daily (student newspaper), 1923 - 1924](http://archives.nd.edu/Daily/)

Jupyter Notebook:
- [GitHub](https://github.com/kwaldenphd/football-text-analysis/blob/main/notebooks/daily.ipynb)
- [Jupyter nbviewer](https://nbviewer.jupyter.org/github/kwaldenphd/football-text-analysis/blob/main/notebooks/daily.ipynb)
- [Google CoLab](https://drive.google.com/file/d/19qTFmbhp7qJTdpCHcKTk-0GXvPc_N2-D/view?usp=sharing) *ND users*

## Directories

From the [University Archives](http://archives.nd.edu/digital/):
- "Lists of Notre Dame officers, administrators, rectors, prefects, faculty, post-doctoral research fellows, and students. The alphabetical list of faculty generally indicates academic department, campus address and home address. The alphabetical list of students gives major subject or academic program, dorm or local address, and home address."
- [Notre Dame Directories, 1922 - 1974](http://archives.nd.edu/dir/)

Jupyter Notebook:
- [GitHub](https://github.com/kwaldenphd/football-text-analysis/blob/main/notebooks/directories.ipynb)
- [Jupyter nbviewer](https://nbviewer.jupyter.org/github/kwaldenphd/football-text-analysis/blob/main/notebooks/directories.ipynb)
- [Google CoLab](https://drive.google.com/file/d/19qTFmbhp7qJTdpCHcKTk-0GXvPc_N2-D/view?usp=sharing) *ND users*

## Magazine

From the [University Archives](http://archives.nd.edu/digital/):
- "The Notre Dame Foundation published this quarterly magazine, which includes much of general interest to anyone studying Notre Dame in the middle of the twentieth century."
- [Notre Dame: A Magazine, 1948-1965](http://archives.nd.edu/ndm/)

Jupyter Notebook:
- [GitHub](https://github.com/kwaldenphd/football-text-analysis/blob/main/notebooks/magazine.ipynb)
- [Jupyter nbviewer](https://nbviewer.jupyter.org/github/kwaldenphd/football-text-analysis/blob/main/notebooks/magazine.ipynb)
- [Google CoLab](https://drive.google.com/file/d/19qTFmbhp7qJTdpCHcKTk-0GXvPc_N2-D/view?usp=sharing) *ND users*

## Observer

From the [University Archives](http://archives.nd.edu/digital/):
- "The Observer started providing news for the University of Notre Dame and Saint Mary's College starting in the fall of 1966, first as a weekly, then bi-weekly, and soon as a daily newspaper. Starting with the issue of October 10, 2009, the Notre Dame / Saint Mary's Observer appeared online (http://ndsmcobserver.com/)."
- [The Observer (student newspaper), 1966 - 2015](http://archives.nd.edu/Observer/)

Jupyter Notebook:
- [GitHub](https://github.com/kwaldenphd/football-text-analysis/blob/main/notebooks/observer.ipynb)
- [Jupyter nbviewer](https://nbviewer.jupyter.org/github/kwaldenphd/football-text-analysis/blob/main/notebooks/observer.ipynb)
- [Google CoLab](https://drive.google.com/file/d/1lCyuGKXQI4GrSGVOuz4l6bjscAd_-d2r/view?usp=sharing) *ND users*

## Scholastic

From the [University Archives](http://archives.nd.edu/digital/):
- "The Scholastic, a student weekly, began in 1867 as The Scholastic Year. For most of its history it provided news about Notre Dame as well as feature articles, literary works, essays, and alumni notes."
- [Notre Dame Scholastic (student magazine), 1867 - 2011](http://archives.nd.edu/Scholastic/)

Jupyter Notebook:
- [GitHub](https://github.com/kwaldenphd/football-text-analysis/blob/main/notebooks/scholastic.ipynb)
- [Jupyter nbviewer](https://nbviewer.jupyter.org/github/kwaldenphd/football-text-analysis/blob/main/notebooks/scholastic.ipynb)
- [Google CoLab](https://drive.google.com/file/d/1_rygfLHBoADkQqnfhTUd0xzUkF51n7Kp/view?usp=sharing) *ND users*

## Scholastic Football Review

From the [University Archives](http://archives.nd.edu/digital/):
- "The Notre Dame Scholastic published reviews of the football season starting in 1901. In 1910 a separate publication covered the "Gridiron Season" and from 1919 to 1921 a Football Review provided competition for the Scholastic. From 1924 to 1932 the Football Review prevailed as the Scholastic provided little or no commentary. In later years the Scholastic generally published its own special issue on the football season, though Irish Eye took over for a time in the 1980s."
- [Notre Dame Football Review, 1901 - 2010](http://archives.nd.edu/Football/)

Jupyter Notebook:
- [GitHub](https://github.com/kwaldenphd/football-text-analysis/blob/main/notebooks/scholastic_football_review.ipynb)
- [Jupyter nbviewer](https://nbviewer.jupyter.org/github/kwaldenphd/football-text-analysis/blob/main/notebooks/scholastic_football_review.ipynb)
- [Google CoLab](https://drive.google.com/file/d/1oDtiH6hbeWhbAaAoZCU5-cSlojaDy88A/view?usp=sharing) *ND users*

## Voice

From the [University Archives](http://archives.nd.edu/digital/):
- "The Voice of Notre Dame, predecessor of the more familiar daily Observer, appeared somewhat irregularly every week or so between 1963 and 1966, though issues were sometimes printed as little as two days apart."
- [Notre Dame Voice (student newspaper), 1963 - 1966](http://archives.nd.edu/Voice/)

Jupyter Notebook:
- [GitHub](https://github.com/kwaldenphd/football-text-analysis/blob/main/notebooks/voice.ipynb)
- [Jupyter nbviewer](https://nbviewer.jupyter.org/github/kwaldenphd/football-text-analysis/blob/main/notebooks/voice.ipynb)
- [Google CoLab](https://drive.google.com/file/d/1ydyMMAf43Aw7ltgB9CobTukR__MEO-P6/view?usp=sharing) *ND users*

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

To get Adobe Pro on your own computer:
- Download the program: [OIT, Adobe Creative Cloud Desktop Application](https://oit.nd.edu/services/software/software-downloads/adobe-creative-cloud-desktop-application/)
- Request a license: OIT, "[Request a license for Adobe Creative Cloud](https://nd.service-now.com/kb_view.do?sysparm_article=KB0017960)," *ND Service Now*

Once you have Adobe Pro on your own computer, you can use the expanded features to run an OCR workflow on a single PDF or multiple PDFs. 

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
- [GitHub](https://github.com/kwaldenphd/nd-digital-archives/blob/main/text-analysis-roadmap.ipynb)
- [Google CoLab]

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

# Next Steps

For more background and context on the various University Archive publications and collections, users are encouraged to consult Thomas E. Blantz's *[The University of Notre Dame: A History](https://undpress.nd.edu/9780268108212/the-university-of-notre-dame/)* (University of Notre Dame Press, 2020).
- [Link to online access via Hesburgh Libraries (ND users)](https://onesearch.library.nd.edu/permalink/f/7uudnk/TN_cdi_askewsholts_vlebooks_9780268108243)

The text analysis tools and resources covered in this lab will work best (and in many cases require) plain-text files as the starting point for analysis. 

We can extract plain-text from scanned documents using a process called "optical character recognition" or OCR. 

For folks with Python proficiency, the Python portions of the lab include a sample OCR workflow that converts digitized PDFs to image files, then takes the image files as binary data and extracts text. The notebooks provided in that section of the lab also include a number of resources for refining or further developing/customizing an OCR workflow.

## Acrobat Adobe Pro

But, depending on the number of documents you're working with as well as the quality of OCR output needed for your project, Adobe Acrobat Pro will likely get you where you need to go.
- NOTE: This is a different program than the Adobe Acrobat Reader DC free program you may have on your computer.

Notre Dame students have access to the Adobe Pro software title through the Adobe Creative Cloud Desktop Application, available free through OIT.
- NOTE: The full Adobe Creative Cloud suite is available on any [OIT lab computer](https://nd.service-now.com/kb_view.do?sysparm_article=KB0013524) and can be accessed through the OIT general purpose [Virtual Computer Lab](https://inside.nd.edu/task/all/virtual-computer-lab)

To get Adobe Pro on your own computer:
- Download the program: [OIT, Adobe Creative Cloud Desktop Application](https://oit.nd.edu/services/software/software-downloads/adobe-creative-cloud-desktop-application/)
- Request a license: OIT, "[Request a license for Adobe Creative Cloud](https://nd.service-now.com/kb_view.do?sysparm_article=KB0017960)," *ND Service Now*

Once you have Adobe Pro on your own computer, you can use the expanded features to run an OCR workflow on a single PDF or multiple PDFs. 

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

# Lab Notebook Components

PLACEHOLDER TEXT
