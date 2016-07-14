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

### File management
#### Learn to cut files
To move a file from one place to the next you first have to copy it and paste it without cloning unlike the Windows univers.
```
Command + C - copy
Command + Option + V - paste without cloning
```
