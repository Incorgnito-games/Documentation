# Documentation
General Documentation, for technical specs and custom classes etc


# Project Tickets
When making an open ticket assign a value between 1-10 with 1-10 being the most labour intense/time consuming
This will help when coordinating different tasks, like picking off some low hanging fruit

# Quick Guide Setup

## Windows
Youll need to make sure you ave a few programs downloaded, 
- [Godot 4.3](https://godotengine.org/download/) make sure to download the one with .net
- [Microsoft Visual Studio Community](https://visualstudio.microsoft.com/vs/community/) or [JetBrains Rider](https://www.jetbrains.com/rider/)
  ==> keep in mind visual studio is different from visual studio code, as well be developing in C# we will use either ide's .net integrated capabilities, ill personaly be using rider, if you choose this make sure you pick the free tier, or you can try an old student email to possibly get it free as i did, 

- [Dotnet SDK 8.0](https://dotnet.microsoft.com/en-us/download) You sould be able to select this package wen installing visual studio if not download it
- [Git for Windows](https://git-scm.com/download/win)==> i would get use to te git bash that comes with the install rater then the gui, keep in mind tere is also git features uin the ide

### Setup
After installing all the requirments create a folder somewhere you want on you computer thats easily accessable, open git bash for windows and move to that directory and type

some usual commands:

```bash
cd  directory_name    <-- move into a folder
ls                     <-- list folders contents
cd ..                  <-- move up one director
cd ~                    <-- go to your root directory
mkdir    directory_name  <-- make a directory
less file               <-- show a file in terminal incremently
vim file_name          <-- command line editor, type :q to exit, :wq to save & exit
cat file_name          <-- print whole file contents to terminal
```

if unfamiliar with bash terminal it will come with time and theres lots of youtube primer videos to move up to speed, eventualy you may wish to migrate to your windows wsl server, which is a full fledged linux kernal allowing you a whole set of tools that may become handy especially if you start using  c++ 


Before you can clone the repo youll need to set up an ssh key to be able to access your github accounts repos(including this organizations)

inside the git bash terminal type

```bash
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```
just follow the prompts, you dont need a passphrase, then
```bash
eval $(ssh-agent -s)
ssh-add ~/.ssh/id_rsa
clip < ~/.ssh/id_rsa.pub
```

if you dont have clip in git bash just
```bash
cat ~/.ssh/id_rsa.pub
```
and copy the contents to your clipboard

Go to you github account, click settings in the top right and look for SSH Key in the left side bar, click new key and paste your key into the field and give it a name
this will alllow github to recoginize your computer with your account allowing you to use there servers

after this is done, set up your local git info and clone the repo

```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"

git clone git@github.com:Incorgnito-games/Incorgnito.git
```

This will set up your local git and clone the repo for the game itself, you may want to clone the repo for the concept art repo as well.

By default this will the develop branch of the repo, open the godot program by douple clicking on where you unzipped it(it may be a good idea to pin it to task bar) and click open project, then search for the directory where you cloned the repo into select it and bang theres your game.

You'll need to adjust you the default editor to point to your ide, eith rider or visual studio, go to editor then settings and search for dotnet in that sub menu select your editor of choice

ill follow up with a short git tutorial to get you moving tommorrow so you can start pushing things and making chnages, remmeber the documentaion wiki and convcept wiki can be easily updated from the site but youll find it very intuative to add file to your folders and just push commits once you get rolling

have fun

