# jAlert

GitHub Project Link : http://rajkumarpb.github.io/jAlert

I am not the author of this plugin. I just found it somewhere and thought it can be helpful for people like me!

This is just an fork of the work from ( http://labs.abeautifulsite.net/archived/jquery-alerts/)
Since it isn't available in github and replaced with better one, I thought of put it here.

Demo : http://labs.abeautifulsite.net/archived/jquery-alerts/demo/

### Why we need to revamp such old jquert Alert plugin?

Well, not everyone has the luxury to use the cutting edge, latest bootbox or flex! For people who are restricted with older browsers, who need smaller footprint and without bootstrap, this kinda plugins help. Especially in corportate, where still IE8 is the king and devs have to bang their hand in the wall to fix so many issues, where this plugin will give nice, simple alternative to the ugly browser alert!

Setup
======

Include the CSS/JS files somewhere in the page(js should be after jQuery! Duh!)
```html
<script src="jquery.alerts.js" type="text/javascript"></script>
<link href="jquery.alerts.css" rel="stylesheet" type="text/css" media="screen" />
```

Quick Use 
==========
```js
jAlert('This is a custom alert box', 'Alert Dialog');

jConfirm('Can you confirm this?', 'Confirmation Dialog', function(r) {
    jAlert('Confirmed: ' + r, 'Confirmation Results');
});

jPrompt('Type something:', 'Prefilled value', 'Prompt Dialog', function(r) {
    if( r ) alert('You entered ' + r);
});

//Use HTML in messages!
jAlert('You can use HTML, such as bold, italics, and underline!');

// To have custom button names in confirm other than Ok/Cancel
jCustomConfirm('Can you confirm this custom dialog?', 'Confirm Header', 'Think about it', 'Maybe Later');
```

You can even change the style dynamically. Just check out the demo page! This jAlert might not win beauty contest, but this is lot easier to use, looks like browser alert and smaller in size(~6KB js & css files combined)! Contributors are welcome!

To change **Theme**, just add 
```js
$.alerts.theme = '_blue';
```
in any html inside document.ready.

**Additional Information** : It supports IE7 and above! Yay! So for anyone out there who want an simple jquery alert plugin, this is it for you! Never tested in IE6, but as per the original author, it should work in IE6 too!

Angular Alert
=============

Add the dependency in module

````js
angular.module('appName', ['jalert'])
````

And you can use it like 
````html
<input type="button" name="Click Me!" value="Click" jalert jalert-type="confirm" jalert-message="This is message!" jcallback="testCallBack()"/>
````
if you need regular alert without any callback, call like this
````html
<input type="button" name="Click Me!" value="Click" jalert="This is message!"/>
````
Normal alert with Callback, then call like this
````html
<input type="button" name="Click Me!" value="Click" jalert="This is message!" jcallback="testCallBack()"/>
````

License 
=========
This plugin is dual-licensed under the GNU General Public License and the MIT License and is copyright 2008 A Beautiful Site, LLC.

