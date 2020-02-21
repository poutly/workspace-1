# 𝟏. ***INSTALL***
*Note: You can install the latest versions from these sites, or the ones I currently use that work for me. 
<br>*PC, Windows x64; I currently use HerokuCLI ver. x64, Git-2.23.0-x64, and VSCode-1.38.0-insider-x64.
<br>- <https://devcenter.heroku.com/articles/heroku-cli>
<br>- <https://git-scm.com/downloads>
<br>- <https://code.visualstudio.com/insiders/>

# 𝟐. ***MAKE ACCOUNTS /APP/REPOSITORY***
Now you need to set up the coding platforms. 
<br>- <https://signup.heroku.com/> (Web hosting)
<br>- <https://github.com/join> (Backup Storage)
<br>- <https://www.name.com/account/create/>* (Custom URL, optional, $)
<br>- <https://freenom.com/> (free URL, shady)
<br>*Make Freenom OR Name.com. Pick one.

<br>a. Make a new heroku app at <https://dashboard.heroku.com/apps>
<br>b. Make a new github repository at <https://github.com/new> 
<br>*Make sure your repository is not private.

# 𝟑. ***SET UP YOUR VSCODE (CODING ENVIRONMENT)***
a. Make a folder where you want to store your code. Name it something recognizable like your intended site name. 
<br>I named mine `workspace-1`
<br><img src="https://i.imgur.com/VXSiEUi.png" width="500">
<br>
<br>b. Open the folder in VSCode.
<br><img src="https://i.imgur.com/YnSo4Uj.png" width="500">
<br>
<br>c. Make a new folder within your workspace. For example, *content*
<br><img src="https://i.imgur.com/lXvMVTL.png">
<br>
<br>d. Make a `index.html` within your content folder. In your new file, type something like: 
<br>```If you see this message, VSCode is connected to the Heroku app!```
<br>*The index page is the main page. It would be what you see first when you type in your url. 
<br>*For example, https://example.com*
<br>*Other pages would be named differently such as `page2.php`, and to get to it you'd need to put https://example.com/page2
<br><img src="https://i.imgur.com/a8jSXyZ.png">
<br>
<br>e. Make an `index.php` page in your workspace. Then, copy and paste (CTRL+S to save):
<br>```<?php require 'content/index.html' ?>```
<br><img src="https://i.imgur.com/AzMocyH.png" width="500">
<br>
<br>f. Now go to your terminal bash.
<br><img src="https://i.imgur.com/MSOeluZ.png" width="500">

# 𝟒. ***SETTING UP HEROKU***
a. Log into Heroku within VSCode by typing this into the bash: ```heroku login```
<br><img src="https://i.imgur.com/zl44hkl.png" width="500">
<br>･ Press enter after it says:
<br>`heroku: Press any key to open up the browser to login or q to exit`
<br>･ Heroku sign in should pop up into your browser, log into it with your Heroku credentials.
<br>
<br>b. To connect VSCode to the Heroku app, input these into the bash terminal, then press enter after each one: 
<br>```$ git init```
<br>```$ heroku git:remote -a workspace-1``` 
<br>
<br>c. To publish your code to the Heroku app, type something into `index.html`, and CTRL+S.
<br>Put this into the bash terminal, then press enter: 
<br>```$ git add .```
<br>```$ git commit -am "1st commit"```
<br>```$ git push heroku master```
<br>Check how your code/content looks at your app url, mine is located at: <https://workspace-1.herokuapp.com/>

# 𝟓. ***BACKING UP YOUR CODE WITH GITHUB***
a. Go to <https://dashboard.heroku.com/apps/workspace-1/deploy/github>. Replace <workspace-1> with your workspace's name as needed.
<br>Search your repository name and connect.
<br><img src="https://i.imgur.com/s94aA5I.png" width="500">
<br>
<br>b. Enable automatic deploys. This connects Heroku to Github whenever you deploy changes to your Heroku app.
<br><img src="https://i.imgur.com/D71T6uI.png" width="500">

# 𝟔. ***PUSHING TO GITHUB***
You need to connect the repository to your VSCode bash by inputting:
<br>```$ git remote add origin https://github.com/unrancid/workspace3.git```
<br>```$ git push -u origin master```
<br>*If you try to push but it gives you this error, input:
<br>```$ git pull origin master --allow-unrelated-histories```
<br><img src="https://i.imgur.com/mqP6hNk.png" width="500">