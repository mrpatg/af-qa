# Aronfield QA Testing Guide

This document will lay out an overview for the process, procedure and tools used to do a full Quality Aassurance test on a client site.

For a small business/brochure site, this QA process should take Approx 2 hours to complete. Start by opening or creating a pulse in the QA board on Monday and title it (QA - SITENAME.COM). Keep it handy to enter in any notes you have as you go. When you begin set the status to "In Progress". If there are issues when completed, mark the status as "Needs Attention", and let a PM know. When the QA test is complete with no issues or they are resolved, let a PM know before marking it completed.


### Validation/Content Testing
* Click through every link on the site and verify they are NOT broken and lead to the desired page.
* Verify all links are relative (//page) and not (http://devsite.com/page). This includes images.
* Verify no dead or empty pages with no content
* Check web address is correctly redirecting by visiting the 4 variations of the domain: (http://www.domain.com, http://domain.com, https://www.domain.com, and https://domain.com) All should redirect to https://domain.com
* Check for spelling mistakes or inaccurate or out of date information.
* Ask the developer to create a test content page with the html file located in this repository, if they have not done so already. This will be used later in Browser Testing

### Accessibility Testing
* Verify color choices have enough contrast with page elements to accommodate color blind users (no white on yellow, or dark on dark, etc. Text and links need to stand out and be clearly readable).
* Make sure all images/links have alt/title tags with a summary of the image/link(hover over an image or link, and you should see a small popup with info).
* Use http://wave.webaim.org and make a list of any Errors and Warnings. This needs to be performed for all major page templates.

### Input Testing
* Go through every form field and verify any required or optional fields behave as required.
* Verify fields that are restricted (eg numbers only) only allow numbers and not alpha characters or punctuation
* Verify any date fields are correctly receiving input, and correcting or rejecting malformed dates.
* Verify text area inputs preserve new line spacing when submitted.

### Browser Testing
* Identify the major page layouts on a site. (eg a site with 30 pages, might have only 3 layouts that need to be tested. Ask developer)
* Use BrowserStack (http://browserstack.com) to load/click through the website, the layouts, and contact forms.
* Use the following browsers/devices for testing:
  * Mac OS Safari
  * Windows Chrome
  * Windows Firefox
  * iOS iPhone X
  * iOS iPhone 5S
  * iOS iPad 6th
  * iOS iPad Mini 4
  * Android Galaxy S9
  * Android Pixel 3 XL
  * Android Moto G 2nd Gen
* Make a note of any issues that you find, and mark them in the pulse comments along with the device/page/element for the developer to reproduce
* Browse the Test Content page on each device, and make note of any striking out of place items or odd looking/behaving elements.


### Performance Testing
* Establish a baseline test using http://webpagetest.org (use default settings). Copy down the Performance Results in the QA pulse comments as the starting data. Make a PM aware of this result, and they will let you know if it is acceptable or if it needs addressed, as it changes on site by site basis.
* Run an initial test through Google Page Speed Insights - https://developers.google.com/speed/pagespeed/insights/. Place any low score results in the pulse.
* Verify SSL present by running a test through SSL Labs - https://www.ssllabs.com/ssltest/. Post results of the test (Grade) in the pulse. If there are issues, take a screenshot and post that in the pulse and alert a developer.


### QA Process
* Create one pulse for the QA process, and add any issues as items/comments in that pulse.
* If issues are outstanding, mark the corresponding segmnent as "needs attention" and make a PM aware of them, you may be asked to assign them to a developer.
* When the developer resolves the issues, go back through the entire QA test, as new issues could have arisen.
* If no issues exist, let a PM know and they will have you mark it completed.
