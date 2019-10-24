## **yxhuang.github.io**
My personal webiste, built based on costomized themes in Alison's webiste (....)

### **1. Alison's webiste folder struture:**
#### 1.1 Basic required folders and files in the root directory: 

* **content:** 

  contents on each pages of the website, the sub-folders are the names of the pages and other contents, like "contact", "authors", "home", "talks", "publication"...
  
  貌似md文件里面的 都是widget, page_type = "talk", "publication", "post" "project" 对应的就是相应文件夹里的内容。然后Alison是用talks projects 等自己建的文件夹作为媒介文件调用上面真正储存各个publication, project的文内容。
  
  如果不用规定的post, talks 这些文件夹，用自己改名的文件夹，就不能在标题后面显示图片缩略图。查了发现是resource文件夹还有public文件夹下里自动generate的不同大小的同插图里，少了150*resize的这个小图，即使自己从/resource/image/post里找到复制过去这两个地方都也不能显示。应该是它widget的模板样式定死了文件夹名字.
  
  我的猜想貌似是对的：”Widget identifiers are set to their respective filenames, so a content/home/about.md widget can be linked from the navigation bar by setting the relevant URL as "#about" in config/_default/menu.toml.“ https://sourcethemes.com/academic/docs/page-builder/ 所以navigation bar里如果link到post，就自动调用了content/home下面的post名称的widget的格式。（不过Alison不是这个，她是link to section (other folders, not widget directly)

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

  It contain css and also all the pictures used in the website (I'm not sure if it is linked to website directly or just used as a storage folder).
  
  It seems, this folder will generate some pictures that used in the pages automatically based on the content folder.
  

#### 1.3 Menue item mapping:

* Research ==> /post

* Teaching ==> /talks

* CV ==> /projects

* About / Contact ==> contact

