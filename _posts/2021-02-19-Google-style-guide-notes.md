---
layout: post
title: "Google style guide notes"
date: 2019-04-17
excerpt: "Google style guide notes"
tags: Tech-writing
comments: true
---
## Language and grammar
* Use second person.
* Use active voice.
* Use American spelling.
* Put conditional clauses before introductions, not after.
Not recommended: Click `Delete` if you want to delete the entire document.
Recommended:  To delete the entire document, click `Delete`.

## Formatting, punctuation, and organization
* Use sentence case for document titles and section headings.
* Use sentence case for document titles and section headings. 
* Use numbered list for sequences. 
* Put code-related text in code font, in MD, Use backticks(反引号)  and <code> in HTML.
*  Put UI element in bold.
Not recommended: Click the REFRESH button.
Recommended: Click **Refresh**.
* Use bullet lists for most other lists. 

## Word list
* on & about
Not recommended: For more information on indexes, see xxx.
Recommended: For more information about indexes, see xxx.
* above
Don't use. Instead, use *preceding*. 
* account name
Don't use. Instead, use *username*.
* action bar (title bar)
Don't use action bar in Android documentation. Instead, use *app bar*. 
* ad tech
Write out on first mention: advertising technology (ad tech). Don't use adtech or ad-tech.
* add-in
Not addin.
* add-on 
Not addon.
* ad hoc (临时、特设)
For example, ad hoc queries (动态查询、即席查度、临时构造的查询) or an ad hoc chart。
Don't use ad-hoc.
* administrator
In Android documentation, use *admin*. 
* AJAX (a net develop way: Asynchronous Javascript + XML)
Not Ajax
* aka (又名，亦称)
Don't use. Instead, write out *also known as*, or use parentheses or the word *or*.
Recommended: Geographic data, also known as geospacial data, is...
Recommended: Geographic data, or geospatial data, is...
Recommended: Geographic data (geospatial dat) is...
* allows you to
Don't use. Instead, use *lets you*. 
* among & between
* AM, PM
Use all-caps, no periods, and a space before. 
Recommended: 9:00 AM or 9:00 PM
* Android
Never android.
* and so on
Avoid using it whenever possible.
* any time (noun), anytime (adverb)
Recommended:
You can change this setting at any time. 
Anytime you can change this setting. 
* API
API console; not APIs console or developer console or dev console.
API key, not developer key or dev key.
APIs not API's.
* APK
Not apk.
* app
In general, use app instead of application when referring to programs for end users, especially in the context of mobile or web software. It's OK to use **application** to convey a sense of greater complexity, such as **application programming interface**.

## Product names
Use the full trademarked product name, except for cases where you are following the UI or are limited by sapce constraints ( as in a table heading)
* Company- and product-name possessives
Add **'s** to the end of the name. 
* Don't use **the** before a product name unless you're using the name to qualify something else. Don't use **the** before tool and API names. 
Not Recommended: Using the Cloud Datastore with the Cloud Dataproc.
Recommended: Using Cloud Datastore with Cloud Dataproc.
Recommended: The Cloud Datastore options page
Recommended; The Google Cloud Console
Recommended: The Transcoder API
Recommended: The `gcloud` command-line tool
* To refer to Google products as services, such as **the Google Kubernetes Engine services** or **the Compute Engine service*. However, if the term services leads to ambiguty, use the product names.

## Text-formatting summary
* Use **bold** formatting for UI elements and at the begining of notices.
* Italicize the following words:
	* When defining terms or using words as words, titles of books, movies, web services and other full-length. 
	* Parameter names. For example, when you refer to the parameters of a method like 
	* Mathematical variables and version variables. For example, *x+y=3*
	* Emphasis in HTML, use the <em> element, which render as italics in most contexts.
* Don't use underline.
* Code font
	* Use <code> for code font  in HTML for  or  " `" in markdown to apply a monospace font and inline code and user input.
	* Use <pre> for code blocks and code samples or "```".

### Sentence case and capitalization
 * Use American English style for general capitalization. 
 * Use sentence case in all headings, titles and navigation. 

### Other punctuation convertions
* Don't use ampersands(&) as conjunctions or shorthand, and use *and*  instead. It is OK to use & when referencing UI elements that use *&*, or in table headings and diagram labels where space constraints require abbreviation. And of course it's fine to use `&` for technical purposes in code. 

## Accesible documentation
* Writing inclusive documentation.
* Avoid unnecessarily gendered language. 
Not recommended: Equipment installation and setup takes around 16 man-hours to complete.
Recommended: Equipment installation takes around 16 person-hours to complete. 
* Avoid unnecessarily violent language. 
* In HTML, use sementic tagging. For example, use the `em` element only to indicate emphasis, not to indicate italics. 
* Avoid when possible camel case and all caps. 
* Make sure the same meaning is conveyed to the reader withoud punctuation marks. For that reason avoid when possible the use of exclamation marks, question marks and semicolons.
* Use shorter sentences. Try to use fewer than 26 words per sentence. 
* Define acronyms and abbreviations on first usage and if they're used infrequently. 
* Start each list in the same format.
* Place distinguishing and important information of a paragraph in the first sentence. 
* Use clear and direct language. 

### Headings and titles
* Use descriptive headings and titles to help a user navigate their brower and the page. 
* Don't skip levels of the heading hierarchy. For example, put an `<h3>`only under and `<h2>`. 
* To change the visual formatting of a heading, use CSS rather than using a heading level that doesn't fit the hierarchy.

### Links
* Use meaningful link text. 
* Don't use *click here* or *read this document*. 
* Use an external link icon to indicate that the link goes to a new domain. 
* Let the reader know that the link is opening differently than expected. For example, if the following link opens in a new tab, the link text should let them know: 
  Accessible content (opens in a new tab).
* Use a standard phrase to clue readers in if you use an in-page link, so they know where the link is sending them. For example:
 Links to sections in the same page. 
* If a link downloads a file, the link text needs to indicate this actio as well as the file type. 

### Images
* Provide `alt text` that adequately summarized the intent of each image. 
* Don't present new information in images; always provides an equevalent text explaination with the image. 
* Don't repeat images unless absolutely necessary. 
* Don't use images of text, code samples, or terminal output. Use actual text. 
* Use SVG instead of PNG if available. 

### Video, recodings, and GIFs
* Provide captions, transcripts, or descriptions of audio and video content. 

### Buttons and icons
* For form-submission buttons, use the native HTML `<button>` element.
* If you are unsure of the name of the icon, inspect the element to use the `aria-label`. 

### UI navigation
* When using angle brackets (>) to document menu paths, add an `aria-label` attribute because some screen readers interpret this symbol as *greater than* or * keyboard arrow right*.

### Tables
* Introduce tables in the text preceding the table because not all screen readers preannounce tables. 
* Use table headings for the first column and the first row only, Use the `th` element.
* If your tables include both row and column headings, then mark heading cells with the `scope` attribute.
* 














