kiwispec.xctemplate
===================

Whut?
-----
Writing a lot of Kiwi specs lately, I decided I needed a template in Xcode for creating a spec. I had resorted to copy-paste of files before, but that proved bit too cumbersome after a while and since I'm actually to lazy to keep on copy-pasting, this template happened. Now I just have to hit ⌘-N, select the kiwi template and I'm set.

![Look ma, no copy/pasting!](http://cl.ly/image/0V3U381r3K3x/Image%202013.11.14%2021%3A06%3A42.png)

Installation
------------
1. Clone the repo to your machine. 
2. Copy the `Kiwi Spec.xctemplate` folder into `~/Library/Developer/Xcode/File Templates/Cocoa Touch` (it's entirely possible you might have to create some folders in order to be able to do that)
3. You don't even have to restart Xcode

Usage
-----
Hit ⌘-N in the correct group in your project (or right click and select `New File...`).

In the dialog select the `Kiwi spec` template that should now be present.

![](http://cl.ly/image/2U2p2P3N2m0r/Image%202013.11.14%2021%3A15%3A46.png)

Enter the class for which you want to make a spec for (without the `Spec` part!):

![](http://cl.ly/image/0l241V3Y2234/Image%202013.11.14%2021%3A15%3A12.png)

And that's it.

This will create a file with the following contents:

```objective-c
//
//  YourMommaSpec.m
//  HipsterProject
//
//  Created by Tom Adriaenssen on 14/11/13.
//  Copyright (c) 2013 Tom Adriaessen. All rights reserved.
//

#import "Kiwi.h"
#import "YourMomma.h"

SPEC_BEGIN(YourMommaSpec)

describe(@"Description for YourMomma spec", ^{
    
	beforeAll(^{ 
		// Runs once at the start of the spec
	});

	afterAll(^{ 
		// Runs once at the end of the spec
	});

	beforeEach(^{
		// Runs before each example 
    });
   
    afterEach(^{
		// Runs after each example
    });

    it(@"example description", ^{

    });

});

SPEC_END
```

And then it's up to you to write an awesome spec. 

License
-------
Not copyrighted. Yeah, baby!
