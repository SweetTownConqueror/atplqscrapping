I INTRO

Suite à de nombreuses indisponibilités d'un site de révision atpl liées à des piratages info
J'ai décidé de mettre en place un scrapper pour pouvoir avoir au moins une partie des questions en offline

Ce programme aspirera les questions des differents uv de latpl sur le site en question, les enregistrera dans un fichier excel
1 colonne contiendra la question 4 autres colonnes les réponses la derniere colonne la solution(A-B-C-D)

-------------------

Following many indisponibilities of an ATPL revision website, mainly because of a cyber hack; I decided
to set up a scrapper to have at least a part of questions on my possession even if their website is down.

II Prepare the script

1) open main.py
2) set the 4 firths variables:
URL="https://yourbebsite/path_to_your_corrected_test" ->enter the url of a corrected test you want to scrap data from
EXEL_SHEETNAME='sheetname_of_where_you_want_to_save_data' ->open the excel file and add the sheet you want the data to be saved on
NUMBER_OF_QUESTION_TO_SCRAP=3 ->enter the number you want
COOKIE_PATH = '../cookie.json' -> connect to the website and export the cookies in JSON (thanks to cookie editor on chrome for instance)
Then copy the json content to the file 'cookie.json'

III execute the script:

command: 

python ../main.py

-----------------------




IV DESCRIPTION
This script use python 3.11
It uses SELENIUM, a virtual web browser using chromium search-engine, which is a programmatically commandded webbrowser
It use the cookie session of the user to access his website account and get the data he needs to.
It browse questions of corrected test and save it in an excel sheet
If the script doesnt work, it may be because of selenium's need of 'chromedriver.exe' eventhough it seems to work without it on my configuration
Google it to know how to download it and specify its path in the script.