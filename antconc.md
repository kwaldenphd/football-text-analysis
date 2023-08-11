# Lab #1 (Text Analysis): AntConc

<a href="http://creativecommons.org/licenses/by-nc/4.0/" rel="license"><img style="border-width: 0;" src="https://i.creativecommons.org/l/by-nc/4.0/88x31.png" alt="Creative Commons License" /></a>
This tutorial is licensed under a <a href="http://creativecommons.org/licenses/by-nc/4.0/" rel="license">Creative Commons Attribution-NonCommercial 4.0 International License</a>.

## Table of Contents

- [Files](#files)
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

# Files

- [Folder with Scholastic Football Reviews](https://drive.google.com/drive/folders/1zK99DK_Cd-w9tu2u2M5vlAOSidZYdVTd?usp=drive_link)

# AntConc

Developed by Laurence Anthony, <a href="http://www.laurenceanthony.net/software/antconc/">AntConc</a> is a free, closed-source program that runs on Windows, OS, and Linux. At the most basic level, AntConc is a concordancer, or a program that constructs a concordance based on terms in a text or collection of texts. AntConc also allows users to visualize concordance calculations and generate word and keyword lists based on terms present in the text. AntConc also supports cluster and collocation analysis and visualization. With Voyant, we explored a web-based graphical user interface option for conducting textual analysis, with a particular emphasis on visualization. AntConc is a software program (that runs on your own computer) that focuses more on corpus linguistics and statistical analysis methods.

## Data

1- Download the zip folder that includes Scholastic football reviews from 1901-1931 ([link to access this corpus via Google Drive](https://drive.google.com/drive/folders/1zK99DK_Cd-w9tu2u2M5vlAOSidZYdVTd?usp=drive_link)). Extract the folder contents on your computer.
- PC users- open File Explorer (folder icon), right click on the zip folder (likely in Downloads), and click "Extract"
- Mac users- click on the zip folder

## Downloading AntConc and Loading Data

2-To download AntConc on your own computer, navigate to [the project website](http://www.laurenceanthony.net/software/antconc/), select the appropriate version for your operating system, and follow the installation instructions.
- NOTE: If at all possible, try to have AntConc installed on your computer for class Thursday 9/16. 

<p align="center"><a href="https://github.com/kwaldenphd/AntConc-tutorial/blob/master/screenshots/Capture_1.PNG?raw=true"><img class="aligncenter size-full wp-image-583" src="https://github.com/kwaldenphd/AntConc-tutorial/blob/master/screenshots/Capture_1.PNG?raw=true" alt="" width="790" height="592" /></a></p>

3-You can launch AntConc by double clicking on the Desktop icon or searching for the program in the Start menu.

4-AntConc allows you to open <strong>single files</strong>, as well as open an entire <strong>file directory</strong>. For this tutorial, we will be working with a large number of text files, so opening the directory makes more sense than loading these files individually.

5-[Link to Google Drive folder where you can download plain-text files](https://drive.google.com/drive/folders/1zK99DK_Cd-w9tu2u2M5vlAOSidZYdVTd?usp=sharing).

*Note: Images and screenshots included in this tutorial are from a sample corpus and do not reflect what you will see working with different texts*

<p align="center"><a href="https://github.com/kwaldenphd/AntConc-tutorial/blob/master/screenshots/Capture_2.PNG?raw=true"><img class="aligncenter size-full wp-image-584" src="https://github.com/kwaldenphd/AntConc-tutorial/blob/master/screenshots/Capture_2.PNG?raw=true" alt="" width="790" height="594" /></a></p>

6-To load the directory (or folder) of Scholastic football review files into AntConc:
  * Click the "File" menu option
  * Select "Open Dir"
  * In the pop-up window, navigate to the folder where you downloaded and extracted the Scholastic football review files
  * Click "OK"

7-The loaded files will be listed on the left-hand window in AntConc, and the total number of files will display at the bottom of that window.

## AntConc’s Functionality

<p align="center"><a href="https://github.com/kwaldenphd/AntConc-tutorial/blob/master/screenshots/Capture_3.PNG?raw=true"><img class="aligncenter size-full wp-image-585" src="https://github.com/kwaldenphd/AntConc-tutorial/blob/master/screenshots/Capture_3.PNG?raw=true" alt="" width="551" height="35" /></a></p>

8-The main AntConc screen gives you access to seven different textual analysis tools.

- **Concordance** searches for and displays keywords in context (KWIC).
- **Concordance Plot** presents a preliminary, basic visualization of a KWIC search.
- **File View** is like the Reader panel in Voyant—it shows you a full file view to see a search result in the larger context of a text.
- **Clusters** highlights terms that appear together frequently in the text.
- **Collocates** calculates the statistical likelihood of terms appearing together in the text. 
  * Clusters looks for term patterns as they are represented in the text. Collocates looks at the likelihood of terms appearing together in the text.
- **Word List** calculates how frequency words appear in your text.
- **Keyword List** compares keywords from two text sources (a reference text and an analysis text).

### Searching Keywords in Context

9-AntConc (and other computing tools) excel at identifying patterns in language that are not always detected by the average reader. 

10-For example, function words like *a, an, the, he, she, I* (often called stopwords in textual analysis) don’t frequently catch our attention as readers. 

11-A computational tool focuses on analyzing the words as term objects, rather than interpreting them based on meaning, context, or function.

<p align="center"><a href="https://github.com/kwaldenphd/AntConc-tutorial/blob/master/screenshots/Capture_4.PNG?raw=true"><img class="aligncenter size-full wp-image-586" src="https://github.com/kwaldenphd/AntConc-tutorial/blob/master/screenshots/Capture_4.PNG?raw=true" alt="" width="789" height="593" /></a></p>

12-Type "the" in the Search Term box at the bottom of the Concordance window and click "Start."

13-The Concordance shows key words in context (KWIC), with the search term highlighted.

14-The KWIC Sort options allow you to change how AntConc displays or sorts the context for your search term. 
- `1R` includes the term immediately to the right of your search term, `2R` includes the second term to the right from your search term, etc.
- `1L` includes the term immediately to the left of your search term, `2L` includes the second term to the left from your search term, etc.

15-Experiment with different KWIC Sort options, and click the "Sort" icon to see updated results.

16-Reflection questions:
- How did your search results change? 
- What happens if you continue to customize or edit the Kwic Sort options? 
- How do you understand a key word differently based on how you tell the program to calculate context?

### Visualizing Keywords in Context

<p align="center"><a href="https://github.com/kwaldenphd/AntConc-tutorial/blob/master/screenshots/Capture_5.PNG?raw=true"><img class="aligncenter size-full wp-image-576" src="https://github.com/kwaldenphd/AntConc-tutorial/blob/master/screenshots/Capture_5.PNG?raw=true" alt="" width="790" height="595" /></a></p>

17-Search for a "ball" in the Concordance Tab.

18-Once your search has loaded, click on the "Concordance Plot" tab to visualize your search results.

19-Each instance of the keyword is represented as a vertical black line. AntConc visualizes how keyword appearances are distributed across each file in the Corpus Files.

<p align="center"><a href="https://github.com/kwaldenphd/AntConc-tutorial/blob/master/screenshots/Capture_6.PNG?raw=true"><img class="aligncenter size-full wp-image-577" src="https://github.com/kwaldenphd/AntConc-tutorial/blob/master/screenshots/Capture_6.PNG?raw=true" alt="" width="791" height="598" /></a></p>

20-Clicking on a specific line takes you to that passage of the text in "File View."

21-Reflection questions:
- How useful do you find these preliminary visualizations? 
- How do they compare to the types of visualizations generated on Voyant? 
- How do these visualizations impact your understanding of the text? 
- What questions do you have based on these visualizations?

### Search Operators

22-If you’re familiar with Boolean searching or Regular Expressions, you know symbols can be used in a search to customize or focus your search results. AntConc uses a series of wildcard operators to allow you to further customize your search.

<p align="center"><a href="https://github.com/kwaldenphd/AntConc-tutorial/blob/master/screenshots/Capture_7.PNG?raw=true"><img class="aligncenter size-full wp-image-578" src="https://github.com/kwaldenphd/AntConc-tutorial/blob/master/screenshots/Capture_7.PNG?raw=true" alt="" width="788" height="579" /></a></p>

23-Go to the "Global Settings" menu option, and select "Wildcard Settings" to view or edit the full list of available wildcard operators.

24-Search for `m?n` and `wom?n` and compare your results.

25-A few notes on operators:
- The `*` operator is often used in Boolean searching.
- The `?` operator is more specific because it stands in for only one character. 
- For example, searching `m*n` will bring back results that include `men`, `mean`, `mellon`, etc. 
- Searching `m?n`  will return `men`, `man`, and `min`. 
- Similarly, `wom?n` will return `woman` and `women`.

### Clusters and N-Grams

<p align="center"><a href="https://github.com/kwaldenphd/AntConc-tutorial/blob/master/screenshots/Capture_8.PNG?raw=true"><img class="aligncenter size-full wp-image-579" src="https://github.com/kwaldenphd/AntConc-tutorial/blob/master/screenshots/Capture_8.PNG?raw=true" alt="" width="791" height="597" /></a></p>

26-Click on the Clusters/N-Grams tab and search for "sport."

27-AntConc ranks your search results, calculates frequency, and range (number of files in which the cluster appears), while also displaying the text in the cluster.

<p align="center"><a href="https://github.com/kwaldenphd/AntConc-tutorial/blob/master/screenshots/Capture_9.PNG?raw=true"><img class="aligncenter size-full wp-image-580" src="https://github.com/kwaldenphd/AntConc-tutorial/blob/master/screenshots/Capture_9.PNG?raw=true" alt="" width="790" height="595" /></a></p>

28-The default Search Term Position places the search term on the left side of the cluster. Change the Search Term Position selection to "On Right" and click "Start" to re-run the search. How do your search results change?

29-Cluster Size determines the range for the number of terms AntConc searches and displays. How are your search results different when you change this range?

## Exporting in AntConc

30-After you are satisfied with a search result, click the "File" menu option and then "Save Output" to save the search result as a plain-text (`.txt`) file.

31-Save the file as `SEARCHTERM_cluster_search` or another descriptive name.

32-Conduct another Cluster search for a keyword of your choosing. Customize your results, and export the results as a text (`.txt`) file.

33-Open the exported file in a text editor (Notepad or Notepad++ for PC users and Text Edit for Mac users) to explore the exported results.

## Collocates and Word Lists

34-As mentioned earlier in the tutorial, Clusters analyzes what words appear most frequently alongside your search term.

35-Collocates calculates what terms are statistically probable to appear near your search term. 
- **Freq** calculates overall frequency
- **Freq(L)** looks at frequency for terms to the left of your search term
- **Freq(R)** calculates frequency for terms to the right of your search term
- **Stat** uses the Mutual Information (MI) and T-score calculations outlined in Michael Stubbs's 1995 article "On inference theories and code theories: Corpus evidnece for semantic schemas" to calculate the statistical probability of term collocation.
  * Michael Stubbs, "[On inference theories and code theories: Corpus evidnece for semantic schemas](http://people.cs.pitt.edu/~wiebe/courses/CS3730/Spring05/stubbs01.pdf)" *Text* 21:3 (1995): 437-465.

<p align="center"><a href="https://github.com/kwaldenphd/AntConc-tutorial/blob/master/screenshots/Capture_11.PNG?raw=true"><img class="aligncenter size-full wp-image-582" src="https://github.com/kwaldenphd/AntConc-tutorial/blob/master/screenshots/Capture_11.PNG?raw=true" alt="" width="791" height="597" /></a></p>

36-Use the name of a historic campus figure or building as your search term.
- "Rockne" is a good place to start.

37-AntConc will display a pop-up window message about needing to generate a Word List. Click "OK" to have AntConc generate that list automatically.

38-Reflection questions:
- What terms are statistically likely to appear in proximity to your search term?
- What happens when you change the Window Span (number of words to the right and left of your search term AntConc will include in the analysis)?

## AntConc Reflection Questions

- What do you notice is similar about Data Basic, Voyant Tools, and AntConc as digital tools for textual analysis? What are the differences?
- Which did you prefer working with (and how/why)?
- How was your understanding of the text impacted by the analysis we did in AntConc? What questions do you still have?
- What would be some of your next steps for conducting textual analysis related to Notre Dame football, using Voyant or AntConc?
- What types of historical research questions can you see textual analysis being useful to answer or respond to (especially related to the conversations we've been having about college football/ND football)?
