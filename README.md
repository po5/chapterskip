# chapterskip
Automatically skips chapters based on title.

## Installation
Place chapterskip.lua in your mpv `scripts` folder.

## Usage
Select which categories to skip.  
Globally: `script-opts/chapterskip.conf` > `skip=opening;ending;more;categories`  
Within an auto profile: `mpv.conf` > `script-opts=chapterskip-skip=opening;ending;more;categories`

The default categories are:
- prologue
- opening
- ending
- preview

Additional categories can be defined with `categories=my-new-category>Part [AB]/Ending 1; another-category>Part C` in `script-opts/chapterskip.conf`

## Category syntax
List of `category name>slash-separated lua patterns`, separated by semicolons.  
A `+` can also be used instead of `>`.

Index-based skips are possible by starting your category name with `idx-`. All patterns will be treated as integers. Chapter indexes start at 1.