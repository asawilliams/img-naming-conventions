Image Naming Conventions
=========================

Intro:
------
There is a need for image file naming conventions after experiencing a wide range of inconsistent naming even on the same project. The convention proposed should be usable on most types of projects (web -> native desktop), but the main consideration is for the web.  This is not supposed to be a perfect convention. There will be exceptions where these rules do not fit the need.

Format:
-------
__[type]-[descriptor*]-[size]-[state]-[position]-['sprite'].[filetype]__

Dash ('-') is used for the delimitor to help with SEO considerations.  While most images are for styling purposes and do not need to be indexed; it's nice to be consistent between images that should be used for SEO and those that do not.

###Type: 
Referrs to the element the image is trying to construct (icon, btn, dialog, bg, ...). This should either be used with all the images in the project or none of them.  
There are two instances where including this can help.  If you are required to have a flat folder structure where there are no subfolders.  This helps not only specify the intent of use, but also puts all the types together when listing in alphabetical order.  The second way this can help is when a designer is sending the assets to the developer.  Sometimes it is difficult to know the intent of the asset when it is outside of a subfolder context.  Having the type can make it easier to know which subfolders the assets should go.    

###Descriptor:
A descriptive name for the specific UI created. It is a required part of the image's name. For instance, if you are creating a login button, then 'login' might be an appropriate descriptor. The descriptor may be more than one word and in that case should still be separated by a underscore.  When naming try use the intent.  For instance, instead of icon-pencil-small-up.png, replace 'pencil' with 'edit'.  This helps if your design changes and are no longer using a pencil to signify the edit intent.  If 'pencil' was in the name you would have to change all the instances where the file name is used.

###Size: 
options: [ _large, normal, small_ ]  
If there are multiple sizes for the same type of UI then you add a size to the name.  It is unwise to use numbers to signify because those dimensions might change, but a size category is a little more flexible.

###State: 
options: [ _up, down, over, active, focused, disabled, selected, error, warning, success_ ]  
There could possibly be more options depending on if you have custom states, but these are the most common ones.

###Position: 
options: [ _top, right, bottom, left, center (horizontal), middle (vertical), trcorner, tlcorner, brcorner, blcorner_ ]
Where in the asset is used to construct the overall element.  For instance, if images are created in three parts: left, middle, and right, due to rounded corners and/or gradients then you would have image names like btn-login-left.png, btn-login-center.png, and btn-login-right.png.

###Sprite:
'-sprite', should be put at the end when the image is a sprite.  All images that are included in a sprite should have an underscore (_) at the beginning of the file to denote that it should not be referenced in code, but instead by its spritesheet.

Order
------
Order of the image name parts is really important.  It allows us to see the images grouped together in the filesystem that makes sense.  Without this order, parts of a button could found in different parts of the list.

Retina
------
When the image is X times larger (greater than 1x) than the intended display diamentions than the name of the image should have '@[x]x' at the end; where [x] should be how many times larger the image is to the displayed diamentions.  The most common is '@2x' for iOS retina images.  
This part of the name is only needed if there is more than one size of image.  For instance, if there are only 2x images than it is not required, but if there are 1x and 2x than 2x should be labeled but not the 1x images.


Examples:
----------
 - btn-login-small-up-left.png
 - icon-search-over@2x.png
 - logo-google.png
 - icons-navigation-sprite.png
