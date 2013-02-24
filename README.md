Image Naming Conventions
=========================

Intro:
------
There is a need for image file naming conventions after experiencing a wide range of inconsistent naming even on the same project. The convention proposed should be usable on most types of projects (web -> native desktop).

Format:
-------
__[type*]_[descriptor*]_[size]_[state]_[position].[filetype]__

Underscore ('_') is used because for native Android development image assets are required to have an underscore as the delimiter.  Because we are using a delimiter we do not need to use uppercase letters to signify change in word.

The type is used incase all the assets need to be in the same folder.  This allows for all the similar purpose images to be grouped together.  It is more than likely (and it is recommended) that you will have a folder structure for these images and will probably have a similar name for the type as the containing folder.  Example, all images in the 'icons' folder will be prefixed with 'icon_'.

###Type: 
Referrs to the element the image is trying to contruct. It is a required part of the image's name.  Being required is a little contriversal. The reason for it being required is so that designers mix using and not using it. 
The image could be part of a button or dialog so you could use 'btn' or 'dialog'. While you might have an icon as a part of the button, the icon could stand alone or be used in another element.  In this case you would use 'icon' instead of 'btn'.

###Descriptor:
A descriptive name for the specific UI created. It is a required part of the image's name. For instance, if you are creating a login button, then 'login' might be an appropriate descriptor.

###Size: 
options: [ _large, normal, small_ ]
If there are multiple sizes for the same type of UI then you add a size to the name.  It is unwise to use numbers to signify because those dimensions might change, but a size category is a little more flexible.

###State: 
options: [ _up, down, over, active, focused, disabled, selected, error, warning, success_ ]
There could possibly be more options depending on if you have custom states, but these are the most common ones.

###Position: 
options: [ _top, right, bottom, left, center (horizontal), middle (vertical), trcorner, tlcorner, brcorner, blcorner_ ]

Order
------
Order of the image name parts is really important.  It allows us to see the images grouped together in the filesystem that makes sense.  Without this order, parts of a button could found in different parts of the list.

Examples:
----------
 - btn_login_small_up_left.png
 - icon_search_over.png
 - logo_google.png
 - icons_navigation_sprite.png
