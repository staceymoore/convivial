Convivial
=========
A jQuery Social Sharing Plugin

Usage
-----
Example with custom analytics using Google Tag Manager
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
Added support for custom analytics callback, e.g. Google Tag Manager
Added support for Facebook App ID
Added support for Google share button
Added support for Facebook share button
Added support for Tumblr share button
Added support to initialize buttons when loading new AJAX content
Forked Sharrre v1.3.5

Dependencies
------------
jQuery 1.7 or newer

Credits
-------
Convivial is based on [Sharrre](https://github.com/Julienh/Sharrre) by Julien Hany