# Table of Contents
* [Set up a Folder Structure in an RMarkdown Project](set-up-a-folder-structure-in-an-rmarkdown-project)
* [How to Centralise Text or Image in the RMarkdown Report](how-to-centralise-text-or-image-in-the-rmarkdown-report)

***
# Set up a Folder Structure in an RMarkdown Project

Sometimes you would like to set up a folder structure in an R project for your RMarkdown report, so that files are well organised in their relevant folders. Here is an example of a folder structure:
* data (store any data files you want to import for the RMarkdown report, except those you want to publish on the ISD website)
* output (store the report produced by RMarkdown scripts. You can create subfolders under it)
  * datafile (store the data files such as Excel tables you want to publish on ISD website)
  * report (store the publication report produced by RMarkdown and any images of charts embedded into the report)
  * summary (store the publication summary produced by RMarkdown and any images of charts embedded into the summary)
* rmarkdown (store the RMarkdown scripts and style template)

To make the folder structure work properly, you need to add some scripts in .Rmd files and create some R scripts. You can find a real example of applying a folder structure in an RMarkdown project [here](https://github.com/NHS-NSS-transforming-publications/Folder-Structure-RMD).

# How to Centralise Text or Images in the RMarkdown Report

Sometimes you would like to centralise a line of text or an image in the RMarkdown report. Here are the steps to set it up:
* Go to the style template file (e.g. NATIONAL_STATS_REPORT_TEMPLATE.docx). Click on the small arrow under "Change Styles" to open up the Styles window. Click on "New Style" button, a window "Create New Style from Formatting" opens up.

![Example for centralising](https://github.com/NHS-NSS-transforming-publications/Images/blob/master/RMD-tip1.PNG)

* Give the new style a name (e.g. Style_Centre) and for Style based on choose "Normal". Click "Center" under Formatting. Then click OK. Now you can save the file and close it.

![Example for centralising](https://github.com/NHS-NSS-transforming-publications/Images/blob/master/RMD-tip2.PNG)

* In your RMarkdown script, whenever you want to centralise text or image, you just add some HTML code around the text/image.

```
<Div custom-style = "Style_Centre">Text/Image</Div>
```
For example:

```
<Div custom-style = "Style_Centre">![Uptake rate by NHS Board by three-year rolling period 2013-16.](Figure1_ggplot.png) \ </div>
```
Please note that for an image without a caption, you need to leave a space between ```\``` and ```</div>```. The text or image should be centralised after knitting.


