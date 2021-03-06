Convivial
=========
A jQuery Social Sharing Plugin

Usage
-----
Example with custom tracking using Google Tag Manager
```javascript
$("#share").convivial({
	share: {
		facebook: true,
		twitter: true,
		googlePlus: true
	},
	buttons: {
		facebook: {layout: 'box_count'},
		twitter: {count: 'vertical'},
		googlePlus: {size: 'tall', annotation:'bubble'}
	},
	enableHover: false,
	enableCounter: false,
	enableTracking: true,
	customTracking: function(network, activity, target){
		dataLayer.push({
			'socialNetwork': network,
			'socialActivity': activity,
			'socialTarget': target,
			'event':'socialEvent'
		});
	}
});
```

Changelog
---------
#### Version 0.3.0
* Added Facebook app id support to popups  
* Added language support to Twitter follow button  
* Added language support to Twitter popups  
* Added language support to Google+ share popups

#### Version 0.2.0
* Added support for Google+ follow button  
* Added support for Twitter follow button

#### Version 0.1.1
* Adjust popup sizes
* Add cursor pointer to tumblr button

#### Version 0.1.0
* Added support for the [SharedCount](http://www.sharedcount.com/documentation.php) API
* Added support for custom analytics callback, e.g. Google Tag Manager
* Added support for Facebook App ID
* Added support for Google share button
* Added support for Facebook share button
* Added support for Tumblr share button
* Added support to initialize buttons when loading new AJAX content
* Forked Sharrre v1.3.5

Dependencies
------------
jQuery 1.7 or newer

Author Info
-----------
Convivial is by Stacey Moore  
Website: [staceymoore.com](http://www.staceymoore.com/)  
GitHub: [staceymoore](https://github.com/staceymoore)  
LinkedIn: [TheStaceyMoore](http://linkedin.com/in/thestaceymoore)

Credits
-------
Convivial is based on [Sharrre](https://github.com/Julienh/Sharrre) by Julien Hany
