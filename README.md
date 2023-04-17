# Origin-Find-Missing-Labels
### This python script is uses yaml origin files to sort and move albums that have an original record label and/or cat number but not an edition record label and/or cat number

Once the albums are moved they can be researched to see if the original data is accurate for the edition and the origin file and site metadata can be updated. After finding moving the albums, it provides messaging and logs what it does so you can look up what it moved and any errors that happened.

It can handle albums with artwork folders or multiple disc folders in them. It can also handle specials characters. It has been tested and works in both Ubuntu Linux and Windows 10. 

This script is meant to work in conjunction with other scripts in order to manage a large music library when the source of the music has good metadata you want to use to organize it.  You can find an overview of the scripts and workflow at [Origin-Music-Management](https://github.com/spinfast319/Origin-Music-Management). 

## Dependencies
This project has a dependency on the gazelle-origin project created by x1ppy. gazelle-origin scrapes gazelle based sites and stores the related music metadata in a yaml file in the music albums folder. For this script to work you need to use a fork that has additional metadata including the tags and coverart. The fork that has the most additional metadata right now is: https://github.com/spinfast319/gazelle-origin

All your albums will need origin files origin files associated with them already for this script to work.


## Install and set up
1) Clone this script where you want to run it.

2) Edit the script where it says _Set your directories here_ to set up or specify three directories you will be using. Write them as absolute paths for:

    A. The directory where the albums you want to examine for missing tags are stored  
    B. The directory to store the log files the script creates  
    C. The directory where you want the albums with original label info and no edition label info to be moved to.  

3) Edit the script where it says _Set whether you are using nested folders_ to specify whether you are using nested folders or have all albums in one directory 

    A. If you have all your ablums in one music directory, ie. Music/Album then set this value to 1 (the default)  
    B. If you have all your albums nest in a Music/Artist/Album style of pattern set this value to 2

4) Use your terminal to navigate to the directory the script is in and run the script from the command line.  When it finishes it will output how many albums were moved for missing tags.

```
Origin-Find-Missing-Labels.py
```

_note: on linux and mac you will likely need to type "python3 Origin-Find-Missing-Labels.py"_  
_note 2: you can run the script from anywhere if you provide the full path to it_

The script will also create logs listing all the albums it moved and include the original path and the new path.  

