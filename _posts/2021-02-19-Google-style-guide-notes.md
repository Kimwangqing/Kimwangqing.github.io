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

### Other punctuation conversions
* Don't use ampersands(&) as conjunctions or shorthand, and use *and*  instead. It is OK to use & when referencing UI elements that use *&*, or in table headings and diagram labels where space constraints require abbreviation. And of course it's fine to use `&` for technical purposes in code. 

## Accessible documentation
### General dos and don'ts
* Writing inclusive documentation.
* Avoid unnecessarily gendered language. 
Not recommended: Equipment installation and setup takes around 16 man-hours to complete.
Recommended: Equipment installation takes around 16 person-hours to complete. 
* Avoid unnecessarily violent language. 
* In HTML, use semantic tagging. For example, use the `em` element only to indicate emphasis, not to indicate italics. 
* Avoid when possible camel case and all caps. 
* Make sure the same meaning is conveyed to the reader without punctuation marks. For that reason avoid when possible the use of exclamation marks, question marks and semicolons.

### Reading ease
* Use shorter sentences. Try to use fewer than 26 words per sentence. 
* Define acronyms and abbreviations on first usage and if they're used infrequently. 
* Use parallet writing structures for similar things. Start each list in the same format.
* Place distinguishing and important information of a paragraph in the first sentence. 
* Use clear and direct language. 

### Headings and titles
* Use descriptive headings and titles to help a user navigate their browser and the page. 
* Don't skip levels of the heading hierarchy. For example, put an `<h3>`only under and `<h2>`. 
* Tag headings using heading elements. In HTML: `<h1>`. `<h2>`, and so on. In MD:`#`, `##`, and so on. 
* To change the visual formatting of a heading, use CSS rather than using a heading level that doesn't fit the hierarchy.

### Links
* Use meaningful link text. 
* Don't use *click here* or *read this document*. 
* Use an external link icon to indicate that the link goes to a new domain. 
* Let the reader know that the link is opening differently than expected. For example, if the following link opens in a new tab, the link text should let them know: 
  Accessible content (opens in a new tab).
* Use a standard phrase to clue readers in if you use an in-page link, so they know where the link is sending them. For example:
 Links to sections in the same page. 
* If a link downloads a file, the link text needs to indicate this action as well as the file type. 

### Images
* Provide `alt text` that adequately summarized the intent of each image. 
* Don't present new information in images; always provides an equivalent text explanation with the image. 
* Don't repeat images unless absolutely necessary. 
* Don't use images of text, code samples, or terminal output. Use actual text. 
* Use SVG instead of PNG if available. 

### Video, recordings, and GIFs
* Provide captions, transcripts, or descriptions of audio and video content. 

### Buttons and icons
* For form-submission buttons, use the native HTML `<button>` element.
* If you are unsure of the name of the icon, inspect the element to use the `aria-label`. 

### UI navigation
* When using angle brackets (>) to document menu paths, add an `aria-label` attribute because some screen readers interpret this symbol as *greater than* or * keyboard arrow right*.

### Tables
* Introduce tables in the text preceding the table because not all screen readers preannounce tables. 
* Use table headings for the first column and the first row only, Use the `th` element.
* Avoid when possible tables in the middle of a numbered procedure. 
* Don't use tables unless it's the best method to present your information. Tables are challenging for screen readers. 
* Don't use directional language to orient the reader, such as above, below, or right-hand side. This type of language doesn't work well for accessibility or for local localization reason. if a UI element is hard to find, provide a screenshot. 
Not recommended: In the left-side panel, click the button with three lines. 
Recommended: Click **Menu** *.

## Future features
Avoid trying to document future features or products, even in innocuous ways. 

## Global audience
### General dos and don'ts
* Use qualifying nouns for technical keywords. For example, when referring to a file called `example.yaml`, call it the example.yaml file and not `example.yaml` by itself. 
* Avoid negative constructions when possible. Consider whether it's necessary to tell the user what they can't do instead of what they can. 
* Avoid directional language (for example, above or below) in procedural documentation. 

### Write precise sentences
* Use active voice and present tense. The subject of the sentence is the person or thing perform the action. With passive voice, it's often hard for readers to figure out who's supposed to do something. 
* Address the reader directly. Use *you*, instead of *the user* or *they*. 
* Avoid phrasal verbs when possible. A phrasal verb combines multiple words to form a single verb phrase. Try to substitute a simple verb first. There might not be a better verb, for example, a few exceptions to this rule include *set up*, *log in*, and *sign in*. 
* Don't use too many modifiers. In particular, don't use more than two nouns as modifiers of another noun. 
Not recommended: A hybrid cloud-native DevSecOps pipeline
Recommended: A cloud-native DevSecOps pipeline in a hybrid environment
* Don't misplace modifiers. For example, place a word like *only* immediately before the noun or verb it relates to. 
Not recommended: Developers only need to apply for one token. 
Recommended: Developers need to apply for only one token. 
* Don't omit relative pronouns. To provide clarity and to avoid ambiguity, use relative pronouns such as *that* or *who*. 
Not recommended: Right-click the link you want to open. 
Recommended: Right-click the link that you want to open.
* Clarify antecedents. Using pronouns can get tricky when translators are working with small, unconnected strings of text. Help them out by making things as clear as possible. 
Not recommended: If you use the term *green beer* in an ad, then make sure it's targeted. 
Recommended:  If you use the term *green beer* in an ad, then make sure the ad is targeted. 

### Be consistent
* Use standardized phrase for frequently used sentences, for example, introductory phrases. 
* Use the conditional clause first. If you want to tell the audience to do something in a particular circumstance, mention the circumstance before you provide the instruction. 
  Not recommended: Click **Delete** if you want to delete the entire document. 
  Recommended: To delete the entire document, click **Delete**.
  Not recommended: Using custom domains might add noticeable latency to responses, if you app is located in one of the following regions. 
  Recommended: If your app is located in one of the following regions, using custom domains might add noticeable latency to responses. 
* Make list items consistent. Make list items parallel in structure. Be consistent in your capitalization and punctuation. 
* Use consistent typographic formats. Use bold and italics consistently. Don't switch from using italics for emphasis. 

### Be inclusive
* Don't to be more culturally specific. Don't refer to specific holidays, culturally practices, or sports unless you're certain they're know worldwide. 
* Use a diverse set of example names. If you need to use people's name, for example, as email addresses, use a diverse set of names. Don't use real people, including yourself, your family, or your friends. 
* Avoid colloquialisms, idioms, or slang that can be confusing and difficult to translate. Phrases like *ballpark figure*, *back burner*. 
* Avoid referring to seasons. 

## Inclusive language
### Avoid ableist language
* Ableist language includes words or phrase such as *crazy*, *insane*,*dumb*, Choose alternative words 
Not recommended: Before launch, give everything a final sanity-check.
Recommended: Before launch, give everything a final check for completeness and clarity. 
Not recommended: It cripples the service, causing a poor user experience until the queue clears. 
Recommended: It slows down the service, causing a poor user experience until the queue clears. 

### Avoid unnecessarily gendered language
Avoid to be sensitive to other possible sources of gendered language. 
Not recommended: Equipment installation and setup takes around 16 man-hours to complete.
Recommended: Equipment installation takes around 16 person-hours to complete.
Not recommended: This API might be just what your globally conscious company needs to help all mankind. 
Recommended: This API might be just what your globally conscious company needs to help all of humanity. 

### Avoid unnecessarily violent language
Avoid graphically violent or harmful terms. For example, avoid using the term *STONITH*, instead, describe the process used to stop an errant node in context using more specific terms. 
If it's unavoidable and you must mention a violent or hamful term such as *STONITH*, mention it once when you first explain the relevant feature, but phrase it in a way that de-emphasizes the term. 
Recommended: This might require you to fence failed nodes. 
Sometimes okay: This might require you to fence failed nodes(sometimes referred to as STONITH). 

* Avoid the use of figurative language that can be interpreted as violent, such as *hang* and *hit*. Although there may also be nonviolent interpretation for these terms, avoiding their prevents unintentional harm that might be caused by the violent interpretations.
* Avoid the use of figurative language that relates to the slaughter of animals. For example, avoid using the metaphor of pets versus cattle when comparing on-premises or stateful system with stateless cloud systems. 

### Write diverse and inclusive examples
* Avoid being too culturally specific to the US. Be mindful when referring to specific holiday. (Don't use to refer to the end of the year. Instead, refer to specific quarters or months), cultural practices, sports, figures or speech, etc. 
* When writing about older adults, avoid terms and figures of speech such as *the elderly*, *the aged*, *seniors*, *80 years young*. Instead, use terms such as *older adults*, *aging population*, or mention the person's relative age or relationship to the other people in your example when those details are relevant. 

### Write about features and users in inclusive ways
* Avoid referring to people in divisive ways. For example, instead of referring to people as 'native speakers' or 'non-native speakers' of English, consider whether or not your document needs to discuss this at all, and revise in order to discuss the feature in terms that are relevant to anyone regardless of what languages they know. 
* Avoid using socially-charged terms for technical concepts where possible. For example, avoid terms such as *blacklist*, *native* feature, and *first-class citizen*, even though these terms may still be widely used. Instead of *first-class*, consider other terms such as: *core feature*, *built-in*, *top-level*. 

### Replace or writer around non-inclusive terms
Many non-inclusive terms are in wide use in the industry, such as *whitelist*. If replacing an established term could cause confusion for reader, you can directly refer to the non-inclusive term on the first use, and put it in parentheses. Then use the inclusive, replacement term throughout the rest of the document. 
Recommended: To make sure that administrators get the notification, add them to an allowlist(sometimes called a *whitelist*). Anyone who isn't on the allowlist is blocked...
Not recommended: You can allowlist a range of IP addresses by entering a CIDR block instead of a single address in the field. 
Recommended: You can allow requests from a range of IP addresses by entering a CIDR block instead of a single addrss in the field. 

#### Write around non-inclusive code terms
In some cases, non-inclusive terms are embedded in code (or smilar) as names or keywords, and you can't simply ignore those terms and use different terminology. What you can do, however, is minimize your use of the term (hence avoid propagating it as a term of art), while still providing clear documentation to your readers. Don't use a non-inclusive name or keyword unless it's in code font. 

One scenario is if you're documenting an existing system in which an entity is already named using a non-inclusive term. 
!(https://github.com/Kimwangqing/pictures/blob/master/an%20existing%20system.png?raw=true)

Recommended: The configuration file helps you create a parent node (which is named `master` in the file).

Another scenario is if your documentation includes a non-inclusive term that's an established keyword, such as the keyword `SLAVE` in dialects of SQL.
!(https://github.com/Kimwangqing/pictures/blob/master/established%20non-inclusive%20term.png?raw=true)
Recommended: Start the replica by using `START SLAVE` statement.

## Link text
		* For example: For more information, see Load balancing and scaling. 
		* For example: For more information about how to capitalize such reference, see Capitalization in references to titles and headings. 
			* Load balancing and scaling 显示为蓝色链接
			* 首字母大写
		* Don't use phrases like *click here* or *see this document*. 
		Not recommended: Want more? `<a href="/wombats">Click here!</a>`
		Not recommended: For more information, see `<a href="/wombats">this document</a>`.
		* Don't use a URL as link text, Instead, use the page title or a description of the page. 
		Not recommended:See the HTTP/1.1RFC at `<a href="http://www.wa.org....html</a>`
		Recommended: For more information about protocols, see `<a href="http://www.wa.org....html</a>`.
		* If a link download a file, write link text that indicate this action as well as the file type. 
		  Recommended: `<a href="/readme.txt">download the README.txt file</a>`.
	    * If the text includes an abbreviation in parentheses, include the long form and the abbreviation in the link text. 
	     Not recommended: Google Kubernetes Engine(GKE).
	     (Google Kubernetes Engine 为可点击蓝色，（GKE）为不可点击）。
	     Recommended: Google Kubernetes Engine(GKE).
	     (Google Kubernetes Engine（GKE） 为可点击蓝色。)
	    * Link text should be distinguishable from the rest of the text on the page. 
	    * Make visited links change color. This helps readers navigate your site effectively, without revisiting content that they've already read.

## Link to other sites
		* It's better to link to good documentation elsewhere than to try to thoroughly document someone else's standard in our documentatoin. 
		* On the other hand, sometimes a few sentences of basic information can save readers a trip to an external site. For example, out API documentation has traditionally included a brief explanation of REST. As knowledge of REST becomes more widespread, we might be able to assume that readers know about it, and can remove those brief explanations. 
		* Make sure any site you link to is high quality, reliable, and respectable. 
		* If the URL has a locale indicator, remove it and then test the link. For example, in a Wikipedia link, change the following:
		  `https://en.wikipedia.org/wiki/Operating-system-level_....`
		  to this:
		  `https:wikipedia.org/wiki/Operating-system-level_...`
	    * Don't force links to open in a new tab or window. Let the reader decide how to open links. In the rare situation that a link needs to open in a new tab or window, let the reader know that the link opens differently than expected. 
	      Not recommended: `<a hred="/style/accessibiliity" target="_blank">Accessible content</a>`
	      Recommended: `<a hred="/style/accessibiliity" target="_blank">Accessible content (opens in a new tab)</a>`.

 ## URLs for images		
		* Use a site-root-relative URL (starting with "/").		
		* HTML sample		
		  `<img		
		  src="/.../images/xxx.png"		
		  alt="Alt description"		
		  />`		
		* MD sample		
		  `![Alt description](/../images/xxx.png)`

## API documentation
* API documentation has traditionally included a brief explanation of REST. As knowledge of REST becomes more widespread, we might be able to assume that readers already know about it, and can remove those brief explanations.



























