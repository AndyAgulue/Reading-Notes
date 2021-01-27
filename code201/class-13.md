# class 13 notes

## Local Storage for Web Applications

Persistent local storage is one of the areas where native client applications have held an advantage over web applications. For native applications, the operating system typically provides an abstraction layer for storing and retrieving application-specific data like preferences or runtime state. These values may be stored in the registry, INI files, XML files, or some other place according to platform convention. If your native client application needs local storage beyond key/value pairs, you can embed your own database, invent your own file format, or any number of other solutions.

Historically, web applications have had none of these luxuries. Cookies were invented early in the web’s history, and indeed they can be used for persistent local storage of small amounts of data. But they have three potentially dealbreaking downsides:

- Cookies are included with every HTTP request, thereby slowing down your web application by needlessly transmitting the same data over and over
- Cookies are included with every HTTP request, thereby sending data unencrypted over the internet (unless your entire - Cookies are limited to about 4 KB of data — enough to slow down your application (see above), but not enough to be terribly useful. 

What we really want is:

- a lot of storage space
- on the client
- that persists beyond a page refresh
- and isn’t transmitted to the server
- Before HTML5, all attempts to achieve this were ultimately unsatisfactory in different ways.

### HTML5 Storage 

`HTML5` storage is a way for web pages to store named key/value pairs locally, within the client web browser. Like cookies, this data persists even after you navigate away from the web site, close your browser tab, exit your browser, or what have you. Unlike cookies, this data is never transmitted to the remote web server (unless you go out of your way to send it manually). Unlike all previous attempts at providing persistent local storage, it is implemented natively in web browsers, so it is available even when third-party browser plugins are not.

### Using HTML5 Storage

HTML5 Storage is based on named key/value pairs. You store data based on a named key, then you can retrieve that data with the same key. The named key is a string. The data can be any type supported by JavaScript, including strings, Booleans, integers, or floats. However, the data is actually stored as a string. If you are storing and retrieving anything other than strings, you will need to use functions like parseInt() or parseFloat() to coerce your retrieved data into the expected JavaScript datatype.

`interface Storage {`
    `getter any getItem(in DOMString key);`                                    
    `setter creator void setItem(in DOMString key, in any data);`                                    
 `};`                                      

                                      
Calling `setItem()` with a named key that already exists will silently overwrite the previous value. Calling `getItem()` with a non-existent key will return null rather than throw an exception.

Like other JavaScript objects, you can treat the localStorage object as an associative array. Instead of using the `getItem()` and `setItem()` methods, you can simply use square brackets. For example, this snippet of code:

`var foo = localStorage.getItem("bar");`
`// ...`
`localStorage.setItem("bar", foo);`

…could be rewritten to use square bracket syntax instead:

`var foo = localStorage["bar"];`
`// ...`
`localStorage["bar"] = foo;`

There are also methods for removing the value for a given named key, and clearing the entire storage area (that is, deleting all the keys and values at once).

`interface Storage {`
  `deleter void removeItem(in DOMString key);`
  `void clear();`
`};`

Calling `removeItem()` with a non-existent key will do nothing.

Finally, there is a property to get the total number of values in the storage area, and to iterate through all of the keys by index (to get the name of each key).

`interface Storage {`
  `readonly attribute unsigned long length;`
  `getter DOMString key(in unsigned long index);`
`}`;
If you call `key()` with an index that is not between `0–(length-1)`, the function will return null.

### Tracking Changes to HTML5 Storage Area

If you want to keep track programmatically of when the storage area changes, you can trap the storage event. The storage event is fired on the window object whenever `setItem()`, `removeItem()`, or `clear()` is called and actually changes something. For example, if you set an item to its existing value or call `clear()` when there are no named keys, the storage event will not fire, because nothing actually changed in the storage area.

The storage event is supported everywhere the localStorage object is supported, which includes Internet Explorer 8. IE 8 does not support the W3C standard addEventListener (although that will finally be added in IE 9). Therefore, to hook the storage event, you’ll need to check which event mechanism the browser supports. (If you’ve done this before with other events, you can skip to the end of this section. Trapping the storage event works the same as every other event you’ve ever trapped. If you prefer to use jQuery or some other JavaScript library to register your event handlers, you can do that with the storage event, too.)

`if (window.addEventListener) {`
  `window.addEventListener("storage", handle_storage, false);`
`} else {`
  `window.attachEvent("onstorage", handle_storage);`
`};`

The handle_storage callback function will be called with a StorageEvent object, except in Internet Explorer where the event object is stored in window.event.

`function handle_storage(e) {`
  `if (!e) { e = window.event; }`
`}`

At this point, the variable e will be a StorageEvent object, which has the following useful properties.

STORAGE EVENT OBJECT

`key`	(string)	The named key that was added, removed, or modified
`oldValue`	(any)	the previous value (now overwritten), or null if a new item was added
`newValue`	(any)	The new value, or null if an item was removed
`url*`	(string)	The page which called a method that triggered this change

*Note: the url property was originally called uri. Some browsers shipped with that property before the specification changed. For maximum compatibility, you should check whether the url property exists, and if not, check for the uri property instead.*

The storage event is not cancelable. From within the handle_storage callback function, there is no way to stop the change from occurring. It’s simply a way for the browser to tell you, “hey, this just happened. There’s nothing you can do about it now; I just wanted to let you know.”

### Limitations in Current Browsers

5 megabytes is how much storage space each origin gets by default. This is surprisingly consistent across browsers, although it is phrased as no more than a suggestion in the HTML5 Storage specification. One thing to keep in mind is that you’re storing strings, not data in its original format. If you’re storing a lot of integers or floats, the difference in representation can really add up. Each digit in that float is being stored as a character, not in the usual representation of a floating point number.

“QUOTA_EXCEEDED_ERR” is the exception that will get thrown if you exceed your storage quota of 5 megabytes. “No” is the answer to the next obvious question, “Can I ask the user for more storage space?” At time of writing (February 2011), no browser supports any mechanism for web developers to request more storage space. Some browsers (like Opera) allow the user to control each site’s storage quota, but it is purely a user-initiated action, not something that you as a web developer can build into your web application.


