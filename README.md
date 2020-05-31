
# Color Picker list for Rofi

I generated this Color Picker lists to be used as a quick search/select tool utilizing rofi, xclip and xdotool.

[Material Color Chart](https://htmlcolorcodes.com/color-chart/material-design-color-chart/)

# Requirements
 * Obviously you will need [Rofi](https://github.com/DaveDavenport/rofi).
 * The actual [Font Awesome](http://fontawesome.io/) font 
 * A CLI clipboard utility like [xclip](https://github.com/astrand/xclip), [xsel](https://linux.die.net/man/1/xsel) or [pbpaste](https://developer.apple.com/legacy/library/documentation/Darwin/Reference/ManPages/man1/pbpaste.1.html).
 * xdotool (or another tool to  simulate keyboard input and mouse activity)


### snippet
```c
g/^\d/delete
%s/\(#.\{6\}\)/\=printf("<span color='%s' weight='normal' fallback='true' lang='red%d'>  Red%d<\/span>",submatch(0) ,line('.')-1,line('.')-1)
%s/$/\=printf('-%-4d', line('.')-1)
```
