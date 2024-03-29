# Scraper
Python tool that searchs and downloads manga (command terminal)

Data source from: *http://w12.mangafreak.net*

## Virtual env
* Recommended even with python3/ pip3 commands (Windows/ Mac/ Linux)
1. cd to main folder 
2. `python3 -m pip install --user virtualenv`
3. `python3 -m venv env`
4. `source env/bin/activate`

## Install Dependencies
* `pip3 install selenium fpdf`
* Download chomedriver from *https://chromedriver.storage.googleapis.com/index.html?path=2.40/*
* Place the chromedriver file path `chromedriver` in the `const.py` file

  Inside const.py (Mac OS X 10.9+):   

        chromedriver = "/Users/Admin/Documents/chromedriver_mac64/chromedriver"

## Local
#### NOTE: 

* If a command is entered incorrectly the process for searching and downloading will reset
* New chrome windows is opened everytime as a new executable

#### Process:
1. Execute the script: `python3 app.py`

     * Google chrome will open and display `data:,` in the URL parameter if successful

2. Enter the name of a manga to search

     * After seaching the manga title the browser will redirect to a search page on *https://w13.mangafreak.net/*

3. Choose the index from the results 

     * Usually the index is 1 because it's the first search result

     * Browser will redirect to the chapter's page showing all chapters

     * Then display all chapters from terminal
4. Select the chapter or press zero for a range of chapters
5. Enter the chapter number you wish to download from start to end (ex. chapter 1 to 5)
6. Script will download the files
     * Makes a zip file, then extractes the contents to a folder, then compresses all images into a single PDF file
