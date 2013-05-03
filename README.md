# jsPlumb
jsPlumb provides a means for a developer to visually connect elements on their web pages. It uses SVG or Canvas in modern browsers, and VML on IE 8 and below. The latest version is 1.4.0.

The project started out life on Google Code and was hosted there up until April 30, 2013.  From May 1st, 2013, jsPlumb lives on GitHub only.

If you're new to jsPlumb, please do take the time to read the [documentation](http://jsplumb.org/doc). 
There are a few integration issues that you should be aware of: z-index needs special attention, for example.

## Requirements
- jQuery:

jsPlumb requires jQuery 1.3.x or later; it has been tested on 1.3.2, 1.4.x, 1.5.x, 1.6.x, 1.7.x, 1.8.x and 1.9.x. To support dragging, you will need jQueryUI 1.7.x or 1.8.x. NOTE: jQuery 1.8.x only works with jQueryUI 1.8.22 and above.

__There is a bug in jQuery 1.6.x and 1.7.x's SVG support for IE9__ - see [this issue](http://bugs.jquery.com/ticket/10832). It means that mouse events do not get posted. There is another discussion of the issue [here](http://forum.jquery.com/topic/1-6-2-broke-svg-hover-events).
This issue is fixed in jQuery 1.8.

- MooTools:

jsPlumb requires MooTools 1.3.x or 1.2.4 (tested on 1.3.2 and 1.2.4; it might work on other versions). To support
dragging in MooTools, you will need Drag.Move from MooTools More. jsPlumb has been tested with Drag.Move from MooTools 
More 1.3.2.1 and 1.2.4.4, but I would recommend using 1.3.2.1 as there were bugs on IE with the getPosition() 
function of MooTools, which the Drag.Move class uses.

__Firefox 11 and MooTools 1.3.x do not play well together in SVG mode__ - see [this issue](https://github.com/mootools/mootools-core/issues/2331)

- YUI3:

jsPlumb requires YUI 3.3.x (tested on 3.3.0; it actually might work on other versions). You do not need to 
include anything other than 'node' in your code that works with jsPlumb, but due to the asynchronous nature of 
module loading with YUI, you need to ensure you use jsPlumb's `ready` function to wrap your initialisation
code, or you cannot be sure that everything that is required is available:

    jsPlumb.ready(function() { 
      ...
    }); 

## jsPlumb in action
Links to various demonstrations can be found [here](http://jsplumb.org).

[TweetPlumb](http://tweetplumb.com) is a great Twitter visualisation built (I say it's great because I built it 
myself!) using jsPlumb.

## Documentation
Documentation can be found in the doc folder of the project, or you can view it online [here](http://jsplumb.org/doc).

API documentation is in the apidoc folder of the project, and online [here](http://jsplumb.org/apidocs/).

The Bezier curve functions used by jsPlumb have been extracted to a separate project:

[https://github.com/sporritt/jsBezier](https://github.com/sporritt/jsBezier)

## Tests
Tests can be found [here](http://jsplumb.org/tests/all-tests.html)

## Twitter
The Twitter account I use for this project is [jsplumblib](http://twitter.com/jsplumblib)

..but of course things fall through the cracks with Twitter. So maybe use this instead:

## Mailing List
Sign up for the jsPlumb announcements mailing list [here](http://eepurl.com/bMuD9).

## License
All 1.x.x versions of jsPlumb are dual-licensed under both MIT and GPLv2. 
