# Mac productivity tips

## Screen space
### Window management
#### Spectacle https://www.spectacleapp.com/
Usefull for key based positioning of windows across desktops and screens with ability to resize at 1/4 1/2 and 3/4 of screen size on each side.

### Dock
#### Reposition
Reposition dock to either left or right of the screen to conserve height.
```
System Preferences -> Dock -> Position on screen -> Left/Right
```
#### Autohide
Let the dock automatically hide to preserve horizontal space also.
```
System Preferences -> Dock -> Position on screen -> Automatically hide and show the dock
```

#### Tweak the dock to display instantelly:
```
defaults write com.apple.dock autohide-delay -float 0; killall Dock;
```
#### Tweak the dock to display after N seconds to avoid miss fires:
```
defaults write com.apple.dock autohide-delay -float N; killall Dock;
```

#### Lower docker show animation duration
```
defaults write com.apple.dock autohide-time-modifier -float 0.2; killall Dock;
```

## Lock your screen
### Shorten password promt delay
Shorten screen saver or sleep password require timer to 5 seconds or immediatelly if you preffer that
```
System Preferences > Security & Privacy > General
check "Require Password" if not checked and select your interval from the select on the right
```

### Screen saver hot corner
Use a hot corner (my favorit is top left due to muliple displays layout) to enter screen saver fast when you have to leave from computer
```
System Preferences > Desktop & Screen Saver > Screen Saver > Hot Corners
select your corner and from the drop down select "Start Screen Saver"
```

### Sleep your Macbook display throw keyboard
You can also put your Macbook to sleep with the use of a keyboard, and it might end up being faster if you are anyway typing mostly at your computer
```
Non eject button Macbooks:
Control + Shift + Power Button

Eject button Macbooks:
Control + Shift + Eject Button
```

## File management
### Learn to cut files
To move a file from one place to the next you first have to copy it and paste it without cloning unlike the Windows univers.
```
Command + C - copy
Command + Option + V - paste without cloning
```

## Terminal
### Use the right tool iTerm 2 (https://www.iterm2.com/)
The mac OS X terminal is a powerfull tool, but as any build in tool it does not satisfy all needs. iTerm2 comes to the resque with support for split panes to allow you to work in multiple contexts side by side (really usefull for deploys and other remote upload/work), search support, paste history, autocomplete, themes, shell integration, inline images and automatic profile switching based on context. 
For the full features package install the iTerm3 (2.x.y beta version that will become later on the 3rd major release)

### Use Z to cd into commonly used paths (https://github.com/rupa/z/releases)
Are your projects located in a directory like Documents/Work/ProjectName/Version/RandomSubfolder and you are sick and tired of cd-ing each time into that long path? It might help you out to have them organised in such a manner, and they totally make sence but all that cd-ing each time you open up a terminal is wasting a thone of time. There is Z for the resque. It remembers the most cd-ed into directories and allows you to access them throw a shorthand

```
cd /Users/RandomUser/Documents/Work/WonderfullProject/v1/sources/
z sour - and TAB
```
It is that simple to access a long path, and it comes in handy when you have to path traverse a lot from the terminal.

#### Instalation
Download the newest release, extract the archive and copy z.sh it into /Applications
Edit your ~/.bash_profile and add the following line to it:
```
. /Applications/z.sh
```
Use Z happelly ever after.

### Do not forget about control + r
You are using the same commands all over again and do not remember each command exactelly each time? Check your recent history throw control + r. Use it and never forget about it, it will save a lot of time.

## Clock and calendar
Are you used to the Windows calendar on clock click feature? Just use Day-0 and remove your existing clock from the menu bar. http://www.shauninman.com/archive/2011/10/20/day_o_mac_menu_bar_clock

## Display blue emissions
Do not destroy your eyes at night, limit the blue radiations using f.lux
https://justgetflux.com/

## Package management
### Homebrew
Make sure to install Homebrew and use it as your package manager. This helps in setting up fast dev environments.
```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

#### Do not forget to update
Every once in a while make sure to update your brew recipes so that you stay up to date.
```
brew update
```

#### Do not forget to upgrade
Every once in a while after doing a brew update, make an upgrade also to fetch new versions for your used receipes.
```
brew upgdare
```

If for some reason you want to keep a package at it's current version, pin it before the upgrade.
```
brew pin package_name
```
