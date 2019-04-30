# Scraper
Python crawler that searchs and downloads manga/Manga in the command terminal

Data source from: *http://www8.mangafreak.net*

## Virtual env
* Recommended for mac even with python3/ pip3 commands
1. cd to main folder 
2. `python3 -m pip install --user virtualenv`
3. `python3 -m venv env`
4. `source env/bin/activate`

## Install Dependencies
`pip3 install selenium fpdf`

Download chomedriver : https://chromedriver.storage.googleapis.com/index.html?path=2.40/
unzip and copy the location of chromedriver in it and assign it to `chromedriver` in `variable.py`

Inside variables.py (Mac OS X 10.9) + :   

        chromedriver = "/Users/default-user/Documents/chromedriver_mac64/chromedriver"

## Local
*NOTE:* If a command is entered incorrectly the process for searching and downloading will reset

New chrome window is opened everytime

1. Execute the script: `python3 go.py`

Google chrome will open and display `data:,` in the URL parameter if successful

3. Enter Manga name to be searched

After seaching the manga title the browser will redirect to a search page on *http://www8.mangafreak.net*

4. Choose the index from the results 

Usually the index is 1 because it's the first search result

Browser will redirect to the chapter's page showing all chapters

Then display all chapters from terminal

5. Select the chapter or press zero for a range of chapters

Enter the chapter number you with to download from start to end (ex. chapter 1 to 5)

6. Script will download the zip with the img files in them
