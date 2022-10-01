# Contribution Guide

The first step in adding your game to the Mocs Arcade is to contact us on the CompUTC [Discord Server](https://discord.gg/CcbAhtdAtn). If you're not a student, contact us through our club email: computc.utc.edu. Once we've responded, we will create a repository for you and add you as an owner over it. 

Read our [Development Guide]() to learn how to make games that will work with the Mocs Arcade. 

# The Listing.toml File

This file holds all relevant information for the launcher to display and launch your game. An example looks like this:

```toml
[metadata]
name = "BananaBomber"
authors = [
    "Andrew Goodenough",
    "Connor McPherson"
]
creation_date = "September 14th, 2014"

[config]
img_path = "example.png"
exec_path = "game.exe"
scores_path = "scores.csv" # [Optional]
volume = 100 # 0 - 255 [Optional]
```

Your listing.toml shoud be added at the root of the repository. 

Your game can have multiple authors, separated by commas. Use the square brackets even if there is only 1 author. 

Be sure to add your cover image, a 320x456 png, to the location and name specified by img_path. 
Also add the path to the executable with exec_path. 

scores_path and volume are optional. If your game does not use highscores, do not include a scores.csv file or put it in the toml. 

all paths are relative to the root of your github repository. 

# Configuring Github

In the repository that has been created for you, upload your project.

Next, click "create a new release" on the right-hand side of the screen under the `Releases` tab. 

Create a tag for your release under the `tag` dropdown.  We recommend `1.0.0`. Click "Generate Release Notes", github will document the release automatically. In the bottom of this screen, there is a dropbox with the text "Attach Binaries by Dropping Them Here or Selecting Them". You'll need to compress your project file into a .zip file and upload it there. 

Click "Publish Release" to finalize. 

The Launcher will automatically pull the latest release in your repository.  It will use the .zip file you uploaded. 

The Mocs Arcade will only load new games once it is restarted. Your game will not appear on the machine right away. 

# Data Collection

The Mocs Arcade collects anonymous data about playtime, total plays, and other statistics. 


