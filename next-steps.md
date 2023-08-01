# Lab #1 (Text Analysis): Next Steps (aka, now it's your turn!)

<a href="http://creativecommons.org/licenses/by-nc/4.0/" rel="license"><img style="border-width: 0;" src="https://i.creativecommons.org/l/by-nc/4.0/88x31.png" alt="Creative Commons License" /></a>
This tutorial is licensed under a <a href="http://creativecommons.org/licenses/by-nc/4.0/" rel="license">Creative Commons Attribution-NonCommercial 4.0 International License</a>.

## Table of Contents

- [Next Steps (aka, now it's your turn!)](#next-steps-aka-now-its-your-turn)
  * [Collaborating Well](#collaborating-well)
  * [Where to Start: Articulating a Research Question or Topic](#where-to-start-articulating-a-research-question-or-topic)
  * [Building a Corpus](#building-a-corpus)
    * [Acrobat Adobe Pro](#acrobat-adobe-pro)
  * [Addressing Your Research Question](#addressing-your-research-question)
- [Lab Notebook Components](#lab-notebook-components)     


# Next Steps (aka, now it's your turn!)

By this point in the lab we've covered a number of different tools for (computational) text analysis, including some that run in a web browser, some that run are your local computer, and some that involve working within a programming language.

Now it's your turn to come up with a small-scale question, topic, etc. related to the period of ND football history we've been looking at (or some of the broader themes we've been talking about) that you could explore using some of the primary sources and analysis/research methods covered in this lab.

## Part I: Identify a research question (or topic)

Background or context for the research question or topic you're exploring
- At least 250  words (or 3 minutes audio/video) on how the question you're asking or topic you're exploring is grounded in the texts we've been reading and conversations we've been having about ND football history and cultural significance.
  * To put it another way, this is a "background" section.

## Part II: Build a corpus

Sources and research/analysis methods you'll be using
- At least 200 words (or 2 minutes audio/video) on how the specific sources you're engaging with and research/analysis methods you're using animate or connect to the question(s) you're asking or the topic(s) you're exploring.
  * To put it another way, this is a "methods" or "methodology" section

## Part III: Preliminary Findings

What you found through the exploration/analysis
- At least 250 words (or 3 minutes audio/video) on what you found through analyzing this source material using specific research/analysis methods. Folks are encouraged to include visualizations/screenshots/figures/etc in this section.
  * To put it another way, this is a "findings" section

## Part IV: Conclusions & Next Steps

Conclusions and next steps
- At least 250 words (or 2-3 minutes asudio/video) on how your findings relate to the broader context or background you outlined at the start of the report.
- Questions to address:
  * How can the work you did in this lab inform how we think about or understand ND football's history and cultural significance? How does it connect to the readings and conversations we've been having in class?
  * Where would you go next with this research? What questions emerged through doing this work? What questions were you not able to address? 
    * To put it another way, this is a hybrid "discussion" and "conclusion" section

## Part V: Individual Reflection

At least 200 words (or 2-3 minutes audio/video) from each member of the group, addressing the following questions:
- Your contribution to the lab report
- Challenges you faced in this lab and how you solved them
- What you learned about text analysis through this lab
- How you're thinking about text analysis (and ND football history/primary sources) differently after this lab
- Other comments/questions/observations

## Other Components
- Any PDF or TXT files you created or worked with (that aren't already in the Lab 1 Google Drive)
- Any Python scripts/Jupyter Notebooks (or RStudio/RMarkdown files) you created or used

# Collaborating Well

Collaboration is also your friend here- you don't have to come up with all the ideas or do all the work on your own. For example, folks with Python skills can focus on assembling a corpus of primary source materials as plain-text formats. Folks who are more comfortable with statistical analysis and/or data analysis/visualization can focus on those aspects of the project. Folks who are more comfortable with close reading approaches for analyzing primary sources can focus on the components of the lab that ask you to think about background/context/broader significance.

In short, leverage the group's strengths. And divide/conquer.

Folks are welcome to meet with me (individually or as a group) to ask questions and think about next steps for how to approach this lab.

# Where to Start: Articulating a Research Question or Topic

Our end-point for this class is an open-ended final project that takes up course topics/themes/etc. This lab is not a final project.

We'll have in-class work time on Thursday 9/23 to continue working on this lab, and folks should anticipate spending 5-7 hours (total) outside class time working on this lab.

Given the limited scope of this assignment, I encourage folks to drill down and narrow their focus for what you want to analyze or explore.
- This could be a particular player, team, or coach. 
- Or you could focus on a particular season or period of time. 
- It could be a specific publication or type of source material.

The final project is a space where you take up more advanced computational methods or engage in larger-scale, multi-faceted research questions- hanging out in the world of exploratory data analysis is absolutely fine for this lab.

For now, think about the questions you might be interested in asking or the topics you might be interested in exploring- we've already done some brainstorming in this direction with our in-class work.

# Building a Corpus

Then, thinking about the primary sources or materials that would be useful for exploring this question/topic.

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

Once you have access to Adobe Pro, you can use the expanded features to run an OCR workflow on a single PDF or multiple PDFs. 

Adobe Pro also allows you to export the contents of a single PDF or multiple PDFs to plain-text (`.txt`) files.

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

# Addressing Your Research Question

Any of the tools and methods covered in this lab are fair game. Folks are also welcome to branch out and/or go more deeply into any of these areas, keeping in mind the limited assignment scope.

But the tools you choose and the analysis methods you land on should be driven by your topic/question and what you want to know about it.

For example, are we wanting to show relationships, similarity, difference. Or change over time. Or comparison. 

The "Text Analysis Flow Guide" visual is a great place to start for thinking about your options.

<p align="center"><a href="https://github.com/kwaldenphd/football-text-analysis/blob/main/text-analysis-flow-guide.png?raw=true"><img class="aligncenter size-full wp-image-582" src="https://github.com/kwaldenphd/football-text-analysis/blob/main/text-analysis-flow-guide.png?raw=true" alt="" width="791" height="597" /></a></p>

Ferdio's [DataVizProject](https://datavizproject.com/) is another useful resource, although it focuses more on general data analysis/visualization and not specifically text sources.

Some questions from [the "Distant Reader" documentation](https://distantreader.org/getting-started) that might get you started:
- "The aforementioned process is a kin to the application of descriptive statistics and merely provides an overview of the results. For more in-depth analysis and understanding, you will want to do more than read frequencies. For example, you will want to identify documents containing interesting words or phrases (search). You will want to read in context where those words occur; employ a concordance. You may want to count & tabulate more specific things, like only the people in a set of given documents; refine the results. You may want to create a timeline or plot things on a map (geolocate). You might want to employ some machine learning techniques that can extract latent themes and plot those themes over time (topic model). You may want to characterize some or all of your carrel into set of nodes and edges, and then visualize the resulting network graph."

The thought experiments in Jennifer Guiliano's "Toward a Praxis of Critical Digital Sport History" might also be a starting point.
- Jennifer Guiliano, “Toward a Praxis of Critical Digital Sport History” *Journal of Sport History* 44:2 (2017): 146-159. [Link to online access via Hesburgh Libraries](https://onesearch.library.nd.edu/permalink/f/7uudnk/TN_cdi_crossref_primary_10_5406_jsporthistory_44_2_0146).

# Lab Notebook Components

[Link to Google Drive folder with lab materials and resources, including notebook template](https://drive.google.com/drive/folders/1ewsgmrPNeWJYzi5f8EXr05VjPnlRCATz?usp=sharing) (ND Users)

Lab notebook formats for non-ND users: 
- [Google Doc](https://docs.google.com/document/d/1mBiPpxjRfBlEZI9XIc8rzSpSuHfAlrfV6l5ivjih1Vo/copy)
- [Markdown](https://github.com/kwaldenphd/football-text-analysis/blob/main/lab-notebook-template.md)
- [PDF](https://github.com/kwaldenphd/football-text-analysis/blob/main/Text_Analysis_Lab_Notebook_Template.pdf)

Components:
- Reflections/observations from in-class work (Data Basic, Voyant Tools, AntConc)
- Report from your own textual analysis experiment (outline below)
- Any PDF or TXT files you worked with
- Any Python scripts/Jupyter Notebooks used in the lab

If you’re working in or using Google Drive, you can download the project folder as a compressed zip folder and submit to Canvas. You can also include a link to the Google Drive folder as part of the lab notebook. 
