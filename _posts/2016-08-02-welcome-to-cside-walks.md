---
layout: post
title:  "Welcome to CSide Walks"
date:   2016-08-02 14:00:00 +0100
---

This is the first post. As such there is not much to tell yet. You can subscribe to the [feed] to keep updated.

``` java
package CSideWalks

/**
 * The root of out CSide Walks.
 */
public object CSideWalksRoot

	/**
	 * Initialize the global objects accessible with `$CSideWalks`.
	 */
	public Object Globals = CSideWalks::CSideWalksGlobals

	/**
	 * OSpace startup logic.
	 */
	public function Void Startup()
	
		//
		// Initialize globals object
		//
	
		Object	globals = $CSideWalks = .Globals.Initialize()
	
		//
		// Initialize objects with __Init methods
		//
	
		$Kernel.OSpaceUtils.InitObjects(globals.f__InitObjs)
		
	end

end
```

[feed]: /feed.xml
