# Slim Popups Usage
===================

## Basic Usage
* Create a directory in your theme called /slim-popups/
* Include one or more files with your popup content
* File location is /child-theme-name/slim-popups/my-file-name.php
* Use the template tag/function in anywhere before or in wp_footer, to ensure js file has time to load

```
slim_popup( 'my-file-name' );
```

### Example with default settings

```
$options = array(
	'css'  			=> true, 	// whether or not to load the stylesheet
	'style'			=> 'modal', // 'modal' or 'slideup'
	'time'			=> '4000',  // time in milliseconds
	'type' 			=> 'exit',  // 'exit' or 'timed'
);
slim_popup( 'my-file-name', $options );
```

### Example showing the ability to use multiple/different popups on the same site. (Please don't be annoying!)

```
$options = array(
	'css'  			=> true, 	// whether or not to load the stylesheet
	'style'			=> 'slide', // 'modal' or 'slideup'
	'time'			=> '4000',  // time in milliseconds
	'type' 			=> 'timed', // 'exit' or 'timed'
);
slim_popup( 'my-file-name', $options, array(
	'cookieName' => 'myCategoryPopup',
) );
```