Image Naming Conventions
=========================

Intro:
------
Conventions that should be used when naming image assets.  There is a need for image file naming conventions after experiencing a wide range of inconsistent naming even on the same project.


Format:
-------
__[type*]_[descriptor*]_[size]_[position]_[state].[filetype]__

underscore is used b/c it is needed for android.  all lowercase letters. try not to use a version number. '*' signifies that this field is required.

###Type: 
the type of image.  From background, icon, logo, button

###Descriptor:

###Position: 
options: [top, right, bottom, left, center, trcorner, tlcorner, brcorner, blcorner]

###Size: 
options: [large, normal, small]

###State: 
options: [up, down, over, active, focus, disabled, error, warning, success]

Examples:
----------
 - btn_login_small_bg_left_up.png
 - icon_search_over.png
 - logo_google.png
