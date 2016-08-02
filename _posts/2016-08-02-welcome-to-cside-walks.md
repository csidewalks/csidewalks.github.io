---
layout: post
title:  "Welcome to CSide Walks"
date:   2016-08-02 14:00:00 +0100
---

This is the first post. As such there is not much to tell yet. You can subscribe to the [feed] to keep updated.

``` java
package CSIDEWalks

/**
 * The root of OScript Adventures.
 */
public object CSIDERoot

	/**
	 * Initialize the global objects accessible with `$CSIDE`.
	 */
	public Object Globals = CSIDE::CSIDEGlobals

	/**
	 * OSpace startup logic.
	 */
	public function Void Startup()
	
		//
		// Initialize globals object
		//
	
		Object	globals = $CSIDE = .Globals.Initialize()
	
		//
		// Initialize objects with __Init methods
		//
	
		$Kernel.OSpaceUtils.InitObjects(globals.f__InitObjs)
		
	end

end
```

[feed]: /feed.xml
