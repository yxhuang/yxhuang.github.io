## **yxhuang.github.io**
My personal webiste, built based on costomized themes in Alison's webiste (....)

### **1. Alison's webiste folder struture:**
#### 1.1 Basic required folders and files in the root directory: 

* **content:** 

  contents on each pages of the website, the sub-folders are the names of the pages and other contents, like "contact", "authors", "home", "talks", "publication"...

* **public:**

  This folder content all the files for publishing website (all conetents to be uploaded to the host)

* **static **

  This folder containts the images and files used in the webpages (header images, CV, working papers)

* **themes **
  
  The hugo theme used in the webiste (here it uses "hugo-academic")

* **config.toml**

  General config file for the website

#### 1.2 Other added folders and files:
* **archetypes**

  It seems to be used to overwrite the same folder under "themes/hugo-academic/archetypes". It contains only a markdown file you can specify image for your project. (not used by Alison)
  
* **assets**

  It contains a css file edited by Alison. It overwrites the same folder under "themes/hugo-academic/assets"
  
* **config**
  
  It contains, languages.toml, menus.toml, params.toml to overwrite the same folder under "themes/hugo-academic/exampleSite/config". You can change menu names, detailed setting options of the webpages.

  
* **data**

  It overwrites the same folder under "themes/hugo-academic/data". It specifies the font and themes setting
  
* **layouts**

  It overwrites some of the files in "themes/hugo-academic/layouts"

* **R**

  It has a R-script to run a single command: 
   
  > blogdown::build_dir('static')
 
* **resources**

  It contain css and also all the pictures used in the website (I'm not sure if it is linked to website directly or just used as a storage folder)
  

#### 1.3 Menue item mapping:

* Research ==> /post

* Teaching ==> /talks

* CV ==> /projects

* About / Contact ==> contact

