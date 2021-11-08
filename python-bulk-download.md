# Lab #1 (Text Analysis): Bulk Downloading Files With Python

<a href="http://creativecommons.org/licenses/by-nc/4.0/" rel="license"><img style="border-width: 0;" src="https://i.creativecommons.org/l/by-nc/4.0/88x31.png" alt="Creative Commons License" /></a>
This tutorial is licensed under a <a href="http://creativecommons.org/licenses/by-nc/4.0/" rel="license">Creative Commons Attribution-NonCommercial 4.0 International License</a>.

## Table of Contents

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

# Python

To undertake large-scale text analysis, we would need to be able to download source material in bulk and eventually convert that source material to plain-text formats for various kinds of analysis and visualization in a programming environment.

This section of the lab procedure includes Jupyter notebook (`.ipynb`) files with sample Python workflows for using text and data mining workflows with select collections of digitized material from the [University of Notre Dame Archives](http://archives.nd.edu/).

Each Jupyter Notebook goes into more detail about the sample Python code presented.

# Bulk Download

Prof. Walden has built out Jupyter notebooks for bulk downloading PDFs for the following collections.

NOTE: Prof. Walden has already loaded PDFs for these publications into Google Drive. If you want or need to download files to your personal computer, you can- but just know we're talking about gigabytes of material. My recommendation is for folks to make copies of the Jupyter Notebooks within Google Drive so you can run them through Google CoLab, mount the files in Google Drive, and not have to deal with storage and processing constraints/limitations on your personal computer. 

To mount Google Drive files within CoLab:
- [Google Colab, "External Data: Local Files, Drive, Sheets, and Cloud Storage"](https://colab.research.google.com/notebooks/io.ipynb#scrollTo=XDg9OBaYqRMd)
- Mdkaish Ansari, "[How to Connect Google Colab with Google Drive](https://www.marktechpost.com/2019/06/07/how-to-connect-google-colab-with-google-drive/)" *Markettechpost* (7 June 2019)

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
- [Google CoLab](https://drive.google.com/file/d/18Z19MYeu3iJzcjbItJQ97FPHWvSBVV4i/view?usp=sharing) *ND users*

## Annual Bulletins and Catalogs

From the [University Archives](http://archives.nd.edu/digital/):
- "Notre Dame's catalogues or bulletins included descriptions of courses, programs, curricula, facilities, and faculty. They generally [listed students](http://archives.nd.edu/bulletin/stdnts.htm) and provided information on [graduation ceremonies](http://archives.nd.edu/bulletin/cmmncmts.htm), degree recipients, and academic prizes won by students."
- [Notre Dame Annual Catalogues or Bulletins, 1850 - 1914](http://archives.nd.edu/bulletin/)

Jupyter Notebook:
- [GitHub](https://github.com/kwaldenphd/football-text-analysis/blob/main/notebooks/bulletins_catalogs.ipynb)
- [Jupyter nbviewer](https://nbviewer.jupyter.org/github/kwaldenphd/football-text-analysis/blob/main/notebooks/bulletins_catalogs.ipynb)
- [Google CoLab](https://drive.google.com/file/d/1D3_LhB3TcuNOiePnz8VubWpiP2Xl3rzn/view?usp=sharing) *ND users*

## Capstan

From the [University Archives](http://archives.nd.edu/digital/):
- "During World War II, the United States Navy trained many officers at Notre Dame. The naval program published its own yearbook, called Capstan."
- [Capstan, 1943-1945, Digital Collection](http://archives.nd.edu/Capstan/)

Jupyter Notebook:
- [GitHub](https://github.com/kwaldenphd/football-text-analysis/blob/main/notebooks/capstan.ipynb)
- [Jupyter nbviewer](https://nbviewer.jupyter.org/github/kwaldenphd/football-text-analysis/blob/main/notebooks/capstan.ipynb)
- [Google CoLab](https://drive.google.com/file/d/1cH6qsO5F5kh6KBYhk-rsugraGjt3gs-Z/view?usp=sharing) *ND users*

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
- [Google CoLab](https://drive.google.com/file/d/1zwheUyZaZ9ut-ewYIx90ltFsaxXQgESS/view?usp=sharing) *ND users*

## Directories

From the [University Archives](http://archives.nd.edu/digital/):
- "Lists of Notre Dame officers, administrators, rectors, prefects, faculty, post-doctoral research fellows, and students. The alphabetical list of faculty generally indicates academic department, campus address and home address. The alphabetical list of students gives major subject or academic program, dorm or local address, and home address."
- [Notre Dame Directories, 1922 - 1974](http://archives.nd.edu/dir/)

Jupyter Notebook:
- [GitHub](https://github.com/kwaldenphd/football-text-analysis/blob/main/notebooks/directories.ipynb)
- [Jupyter nbviewer](https://nbviewer.jupyter.org/github/kwaldenphd/football-text-analysis/blob/main/notebooks/directories.ipynb)
- [Google CoLab](https://drive.google.com/file/d/1Usoq-kxdywEnuUzp0F4GZKSjlI0YWx9V/view?usp=sharing) *ND users*

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
