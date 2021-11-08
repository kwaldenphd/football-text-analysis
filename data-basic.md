# Lab #1 (Text Analysis): Data Basic

<a href="http://creativecommons.org/licenses/by-nc/4.0/" rel="license"><img style="border-width: 0;" src="https://i.creativecommons.org/l/by-nc/4.0/88x31.png" alt="Creative Commons License" /></a>
This tutorial is licensed under a <a href="http://creativecommons.org/licenses/by-nc/4.0/" rel="license">Creative Commons Attribution-NonCommercial 4.0 International License</a>.

## Table of Contents

- [DataBasic](#databasic)
  * [WordCounter](#wordcounter)
  * [SameDiff](#samediff)

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