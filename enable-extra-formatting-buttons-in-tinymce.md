#WPRecipes

##How to enable some useful text formatting options in TinyMCE in WordPress
*21/12/2014*

Most of the time default TinyMCE editor in WordPress is pretty adequate for everyday text formatting. However, there are a lot of extra formatting options which are hidden out of the box. Enabling these options will give you extra formatting features that will be useful for many of us. In this article, I will show you how to enable these hidden formatting options in TinyMCE. Just add the following code block in your theme’s functions.php file

```php
function tinymce_enable_more_buttons($buttons)
{
    $buttons[1] = 'fontselect';
    $buttons[2] = 'fontsizeselect';
    $buttons[3] = 'styleselect';
    return $buttons;
}
 
add_filter("mce_buttons_3", "tinymce_enable_more_buttons");
```

Here is how it will look in the TinyMCE

![TinyMCE](img/format.gif) 
