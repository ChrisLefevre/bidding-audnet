# Prebid.js &amp; Audience Network Debug Tool

## Implementation Steps:

* Copy all lines of code from [here](prebid-audNet-debugTool/prebid_audNet_debugTool.js)
* Open Chrome Dev Tools
* Click on the “Sources” Tab
* Click on “Snippets” (could be under more options button)
* Click on “+ New Snippet”

![alt text](/resources/images/snippet_setup.png)

* Name the Snippet (ie “Prebid.js & Audience Network Debug Tool”)
* Paste the Code into the Box on the Right of your New Snippet
* Right Click on the Code You Just Pasted and Click “Save”
* Navigate to Any Page With Prebid.js & Audience Network, after the page completes the auction, navigate to Sources → Snippets and right click your new snippets Name and click “Run”
* This will print out full details on the auction including these sections:
    * **Audience Network** - this is all the info for our bids, i've included other columns here like format (so we can see fullwidth or native), bid id, and placement id.  
    * **All 320x50's** - This is all the info for all bidders mapped to a 320x50 size on the page
    * **All 300x250's** - This is all the info for all bidders mapped to a 300x250 size on the page (our fullwidth and native would show up here)
    * **All Bids With Undefined Sizes** - this info is all bidders not mapped to a size (which is probably a problem)
    * **All Bidders / All Sizes** - this is an aggregation of all the bids on the page
    * **Winning Bidders for All Sizes** - this is all the winners for each ad slot on the page
    * **Full Details for All Bidders** - this is the entire prebid.js bid response object printed out so you can dig into it if necessary (you can see our tag and the exact key values being sent to DFP)
    
![alt text](/resources/images/example_output.png)
