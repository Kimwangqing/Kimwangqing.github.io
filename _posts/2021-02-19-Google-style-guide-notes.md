---
layout: post
title: "Google style guide notes"
date: 2019-04-17
excerpt: "Google style guide notes"
tags: Tech-writing
comments: true
---
[TOC]

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
Use the full trademarked product name, except for cases where you are following the UI or are limited by space constraints ( as in a table heading)
* Company- and product-name possessives
Add **'s** to the end of the name. 
* Don't use **the** before a product name unless you're using the name to qualify something else. Don't use **the** before tool and API names. 
Not Recommended: Using the Cloud Datastore with the Cloud Dataproc.
Recommended: Using Cloud Datastore with Cloud Dataproc.
Recommended: The Cloud Datastore options page
Recommended; The Google Cloud Console
Recommended: The Transcoder API
Recommended: The `gcloud` command-line tool
* To refer to Google products as services, such as **the Google Kubernetes Engine services** or **the Compute Engine service*. However, if the term services leads to ambiguity, use the product names.

## Text-formatting summary
* Use **bold** formatting for UI elements and at the beginning of notices.
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
If it's unavoidable and you must mention a violent or harmful term such as *STONITH*, mention it once when you first explain the relevant feature, but phrase it in a way that de-emphasizes the term. 
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
Recommended: To make sure that administrators get the notification, add them to an allowlist (sometimes called a *whitelist*). Anyone who isn't on the allowlist is blocked...
Not recommended: You can allowlist a range of IP addresses by entering a CIDR block instead of a single address in the field. 
Recommended: You can allow requests from a range of IP addresses by entering a CIDR block instead of a single address in the field. 

#### Write around non-inclusive code terms
In some cases, non-inclusive terms are embedded in code (or similar) as names or keywords, and you can't simply ignore those terms and use different terminology. What you can do, however, is minimize your use of the term (hence avoid propagating it as a term of art), while still providing clear documentation to your readers. Don't use a non-inclusive name or keyword unless it's in code font. 

One scenario is if you're documenting an existing system in which an entity is already named using a non-inclusive term. 
![](https://github.com/Kimwangqing/pictures/blob/master/an%20existing%20system.png?raw=true)

Recommended: The configuration file helps you create a parent node (which is named `master` in the file).

Another scenario is if your documentation includes a non-inclusive term that's an established keyword, such as the keyword `SLAVE` in dialects of SQL.
![](https://github.com/Kimwangqing/pictures/blob/master/established%20non-inclusive%20term.png?raw=true)
Recommended: Start the replica by using `START SLAVE` statement.

#### Avoid bias and harm when discussing disability and accessibility
* Don't describe people without disabilities as "normal" or "healthy". Instead, use terms such as: *nondisabled person*, *sighted person*, *hearing person*, *person without disabilities*.
* Research the ways the people you're writing about prefer to be identified and the terms they prefer in many cases, avoid terms that remove personhood, or that define people by their disability. For example, avoid terms such as: *the disabled*, *a quadriplegic*. Instead, use terms such as: *people with disabilities*, *a quadriplegic person*. 
* Avoid terms that reflect or project feelings and judgments about a person's disability, such as: *victim of*, *suffering from*. Instead, use neutral terms such as: *experiencing*, *living with*. 
* Avoid euphemisms or patronizing terms such as: *special*, *differently abled*. 

## Third party sources
* Don't copy content from another source because it might violate copyright. Instead, paraphrase and link to their content. Content includes the following types:
	* Text
	* Image
	* Code
	* Logos
	* Speech
![](https://github.com/Kimwangqing/pictures/blob/master/third%20party%20source%20recommended&unrecommended.png?raw=true)

### Avoiding third-party content
Unless you are sure that your company owns the assets, avoid copying from these sources:
* Third-party sources: This list includes documentation, websites, books, blogs, videos, images, podcasts, and more.
* Reference sources: Avoid copying from dictionaries, encyclopedias, and Wikipedia.
* Open source product documentation: OSS has different license options, which can range from no reuse without attribution to complete freedom to use the material. It's not safe to assume that you can reuse this content freely. 
* Git content: Different GitHub uses might adopt different licenses for their content. It's not safe to assume that you can reuse this content freely. 

### Reusing content
You can reuse content if you are the source of that content.

## Voice and tone
* Without being overly colloquial, a voice that's casual and natural and approachable, not pedantic or pushy. Try to sound like a knowledgeable friend who understands what the developer wants to do. 
* Don't try to write the way you speak.
* Don't try to be super-entertaining. 

### Some techniques and approaches to consider
* Use transitions between sentences. Phrases like *Though* or *This way* can make paragraph less stilted.
  (Then again, sometimes transitions like *However* or *Nonetheless* can make paragraphs more stilted).

### Politeness and use of *please*
* It' s great to be polite, but using *please* in a set of instructions is overdoing the politeness. 
Not recommended: To view the document, please click **View**. 
Recommended: To view the document, clike **View**. 
Not recommended: For more information, please see [link to other document].
Recommneded: For more information, see [link to other document].
|Too informal|Just about right|Too formal|
|--|--|--|
|Dube! This API is totally awesome!|This API lets you collect data about what your users like.|The API documented by this page may enable the acquisition of information pertaining to user preferences.|
|Just like a certain pop star, this call gets your telephone number. The easy way to ask from someone's digits!|To get the user's phone number, call `user.phoneNumber.get()`.|The telephone number can be retrieved by the developer via the simple expedient of using the `get()` method on the user object's `phoneNumber` property. |

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

## Language and grammar
### Abbreviations
Abbreviations include acronyms, initialisms, shortened words, and contractions. 
In most contexts, the technical distinction between acronyms and initialisms isn't relevant; it's fine to use the word *acronym* to refer to both. 

* An acronym is formed from the first letters of words in a phrase, but it pronounced as if it were a word itself:
	* NATO for North Atlantic Treaty Organization

* An initialism is also formed from the first letters of words in a phrase, but each letter is pronounced separately:
	* CIA for Central Intelligence Agency
	* FYI for For You Information
* A shortened word is just part of a word or phrase, sometimes with a period at the end:
	* Dr. for doctor
	* etc. for et cetera
	* min for minutes
	* CA for California
* Some abbreviations can be either acronyms or initialisms depending on the speaker's preference; examples includes *FAQ* and *SQL*. In some cases, the pronunciation determines whether to use *a* or *an*.
* Don't create your own abbreviations. Use recognizable and industry standard abbreviations. 
* Spell out a term. When an abbreviations is likely to be unfamiliar to the audience, spell out the first mention of the term and immediately follow with the abbreviation in parentheses, as in the following examples:
	* Border Gateway Protocol (BGP) 
	* elliptic-curve cryptography (ECC)
  For all subsequence mentions of the abbreviation, use the abbreviation by itselft. 
* Consider your audience to decide to spell out a term. If the majority of your audience is 

#### Long and short version of a word
* Some words have a long version or short version, for example:\
	* *application* and *app*
	* *demonstration* and *demo*
	* *synchronize* and *sync*
 * The short versions of the words are not abbreviations, and if you use them, you don't need to put a period after them.
 * If you're not sure whether a word is an abbreviation or just a short version of a longer word, use the speaking test: if you speak the short version as a word, for example, *This is a demo version of the product*, you can usually treat it as a word and not an abbreviation. 
* Capitalize the spelled-out version of the abbreviation only if the long form is a proper noun or is conventionally capitalized. Don't capitalize it only because the abbreviation includes capital letters. 

#### Creating abbreviations
Don't create your own abbreviations. Use recognizable and industry standard acronyms and initialisms. 

#### Making abbreviations plural
Making abbreviations plural. In general, treat abbreviations as regular words when making them plural, for example, *APIs*, *SKEs*, and *IDEs*. If the abbreviation ends in *s*, *sh*, *ch*, or *x*, then add *es*, for example, *OSes*, *DISHes*, *DCCHes*, *BMXes*. 

#### When to spell out a term
* In general, when an abbreviation is likely to be unfamiliar to the audience, spell out the first mention of the term and immediately follow with the abbreviation in parentheses, as in the follow examples:
	* *Border Gateway Protocol (BGP)*
	* *elliptic-curve cryptography (ECC)*
		* For all subsequent mentions of the abbreviation, use the abbreviation by itself.
		* Capitalize the spelled-out version  of the abbreviation only if the long form is a proper noun or is conventionally capitalized. 
		* Don't capitalize it only because the abbreviation includes capital letters. 
* If the first mention of a term occurs in a heading or title, you can use the abbreviation and then spell out the abbreviation in the first paragraph that follows the heading or title. 
* When deciding to spell out a term, consider your audience. If the majority of your audience is likely to recognize and understand the term, then you don't need to spell it out. For example, *API* you don't need to spell out application programming interface. 
	* If you're explaining the general concept of an API to someone with no programming experience, spelling out the abbreviation can be helpful. 
* The following abbreviations rarely need to be spelled out:
	* API
	* DVD
	* PDF or XML
	* HTML
	* PC
	* RAM
	* REST
	* Units of measurement such as MB or GB
	* URL
	* USB

#### Abbreviations not to use
* Prefer English terms over Latin abbreviations. Don't use *i.e.* or *e.g.*; instead, use *that is* or *for example*, respectively.
* Don't use Internet slang abbreviations such as *RTFM* means read the fucking manual.
* If the full spelled-out word is common and easily understandable, use that rather than abbreviating. For example, write *approximately* instead of *approx*.

#### Periods with abbreviations
* Don't use periods with acronyms or initialisms.
* Put a period at the end of a shortened word, except for date and time abbreviations. 
* If you write or say an abbreviation as a word, for example *app* or *sync*, don't put a period after it. 
* Don't use a period with an abbreviation for the name of a country, US state. 

#### Abbreviations as verb
* Don't use acronyms, initialisms, or shortened words as verbs.

### Active voice
In general, use active voice, in which the grammatical subject of the sentence is the person or thing performing the action, instead of passive voice, in which the grammatical subject of the sentence is the person or thing being acted upon. 
* One reason is that it's easy to neglect to indicate who or what is performing a particular action, and it's ofter hard for readers to figure out who's supposed to do something. It's possible to indicate who's performing the action in passive voice using by, but the resulting prose is generally not as good as if you were to recast the sentence as active voice. So whenever possible, make the doer the subject of the sentence. 
Not recommended: The service is queried, and acknowledgment is sent. 
Recommended: Send a query to the service. The server sends an acknowledgment. 

#### Exceptions
For example, passive can be okay in the following instances:
* To emphasize an object over an action.
Recommended: The file is saved. 
* To de-emphasize a subject or actor.
Not recommended: You created over 50 conflicts in the file. 
Recommended: Over 50 conflicts were found in the file. 
* If your reader don't need to know who's responsible for the action. 
Recommended: The database was purged in January. 

### Anthropomorphism
Don't attribute human qualities to software or hardware. 
Recommended: The pc detects a new device. 
Not recommended: The PC sees a new device. 

### Articles(a, an, the)
Some abbreviation can be both acronyms and initialisms, requiring **a** in one instance and **an** in the other. 
For example, **FAQ**, which some pronounce "fak" and other spell out, requires **an** when spelled out and **a** when pronounced as a word. 
The following is a list of these kinds of abbreviations with our recommendations for which article to use:

* An SQL
* An FAQ

#### More materials about articles
##### Nouns that need determiners
  **Countable singular nouns**

##### Nouns that don't need determiners: Plural nouns (not necessary)
  Plurals can go without determiners, too. Although you can say "the cats", you can also say "cats", if you don't have any particular cats in mind. 

##### Nouns that don't need determiners: Mass nouns (not necessary)
Mass nouns, also called uncountable nouns, don't need a determiner, either. 
*Fruit is on sale.*
*The fruit is on sale.* is also fine. 

##### Definite article 
*The* is called definite article because you use it when you're talking about something that is distinguished from other things. 
For example, 
*The cat crossed the road.*
It indicates:

* this cat might be distinguished from other things.
* Or just because it's the only cat mentioned earlier in the conversation. 
*Thank you for taking the time to review my application.*
It indicates you're talking about a definite amount of time, whatever amount of time it takes to review your application. 
*Thank you for taking time to review my application.*
It indicates you're thanking the readers for any amount of time they might take to review your application, even if it's a millisecond. 
For the reason, *Thank you for taking the time* seems like the better option. 

##### *A* the indefinite article
You use it when you're talking about something that you're not trying to distinguish from other things. 
For example,
*A cat crossed the road.*
It could be any cat. 

Determiner
* Countable singular nouns **have** to have a determiner.
* Proper nouns, plural nouns, and mass nouns aren't necessary to have determiners. 

##### Collective nouns
Thought there is no rule state you must use a singular verb or a plural verb after a collective noun, it depends on you're thinking of the collective noun as a single unit or different unit separately. 
For example, 
*Tim's family are ranchers.* (is better, because talking about one family a bunch of separate individuals.)
*Tim's family is rancher.*
*Tim's family is wealthy.* (is better, because talking about one family one unit.)
*Tim's family are wealthy* 

###### Institutions and animate vs. inanimate nouns
* Institution names, such as the United States, Congress, and the House of Lords, tend to use singular verbs, because we see these institutions as units and we don't think of the members as individuals. For example,
*Congress is meeting today.*
*The members of Congress are meeting today.* (If you want to emphasize the individuals in Congress.)
* Institution names are animate, they can use a plural or a singular verb. 
* Inanimate objects, such as *sugar* or *furniture* are called mass nouns or uncountable nouns, and are always singular. 
  For example, 
  *This sugar is very sweet.* or *My furniture is too old.*
  You can't say, *My furniture are....* 
  If you want to talk about individual grains of sugar or individual pieces of furniture, then you have to say something like *Eight grains of sugar were here.* or *These pieces of furniture are new.*

###### Preposition phrases
* When a prepositional phrase comes after a collective, the verb takes its cue from the subject of the sentence. 
For example,
*a large group of students*, *group* is the collective noun and the subject of the sentence, and the prepositional phrase *of students* comes after the collective noun.
In this case, just ignore the prepositional phrase *of students* that modifies the subject and take you cue from the subject *a large of group*.
* It depends on you're thinking of the collective noun as a single unit or different unit separately. 
  * If you're in the United States and you're thinking of the group as a single unit, you'd generally use a singular verb. 
    *A large group of students is arriving at soon.*
  * If you're in Britain or are thinking of the students as individuals, you'd generally use a plural verb.
    *A large group of students were listening.*

###### Consistency
It would be better to stick with all singular or all plural.
For example,
*The faculty is meeting today, but they are not happy to be meeting.* Here is a mixed structure with a singular verb and a plural verb. 

### Capitalization
* Follow the official capitalization for the names of brands, companies, software, products, services, features, and terms defined by companies and open source communities. 
Recommended in Kubernetes context: A job creates one or more Pods.
Recommended: The Cloud Scheduler job publishes a message to a Cloud Pub/Sub topic at one-minute intervals. 
* If an official name begins with a lowercase letter, then put it in lowercase even at the start of a sentence. But it's better to revise the sentence to avoid putting a lowercase word at the start,if possible. 
* Don't use all-uppercase, except in the following contexts:
  * In official names;
  * In abbreviations that are always written in all-caps;
  * Or when referring to code that uses all-caps.
* Don't use camel case, except in the following contexts:
  * In official names;
  * Or when referring to code that uses camel case. 

#### Capitalization in titles and headings

* Use sentence case in document titles and headings. 
* Don't put a period at the end of a title or heading. 
* Capitalize the first word in the following contexts:
	* The first word in the title;
	* The first word in a subheading after a colon;
	* Any proper nouns or other terms that are always capitalized a certain way. 

<a name="reference1">
#### Capitalization in references to titles and headings
</a>
* In references to any title or heading from a document that follows this guide, use sentence case even if the title or heading itself uses title case. 
* That way, when the title or heading is eventually updated to sentence case, the reference will match. 
* When you reference the title of any source that doesn't follow this guide, retain the original capitalization. 

#### Capitalization and colons
* Use a lowercase letter to begin the first word of the text immediately following a colon, unless the text is one of the following:
	* A proper noun
	  *Open source software: Istio*
    * A heading
    * A quotation
      *Arthurian wit: "Bring me you sworde"
    * Text that follows a label such as Caution or Note

#### Capitalization and figures
* Use sentence case for captions.
* Use sentence case for labels, callouts, and other text in images and diagrams.
  
#### Capitalization in glossaries and indexes
* Use lowercase for glossary and index terms unless the term is a proper noun or another reason to require capitalization.
* Use sentence case for glossary definitions.

#### Capitalization and hyphenated words
* Capitalize only the first element in the word, unless a subsequent element is a proper noun or proper adjective. 

#### Capitalization in lists
* Use sentence case for  items in all types of lists. 

#### Capitalization for tables in text
* Use sentence case for all the elements in a table: contents, headings, labels, and captions. 

### Clause order
* Mention the circumstance or goal before you provide the instruction. 
Recommended:
* For more information, see [link to other document].
Not recommended:
* See [link to other document] for more information.
Recommended:
* To delete the entire document, click **Delete**.
Not recommended:
* Click **Delete** if you want to delete the entire document.
Recommended:
* If you app is located in one of the following regions, using custom domains might add noticeable latency to responses. 
Not recommended:
* Using custom domains might add noticeable latency to responses if your app is located in one of the following regions.

### Contractions
#### Negation contractions
* It's fine to use *-n't* contractions. such as *isn't*, *don't*, and *can't*.

#### Noun + verb contractions
* Avoid contractions formed from nounds and verbs.
Reconmmended: The browser is fast, simple, and secure. 
Not recommended: The browser's fast, simple, and secure. 
Recommended: The following guides are a good way to learn to use Universal Analytics.

#### Don't use double contractions
* shouldn't've -- shouldn't have -- should not have
* wouldn't 've -- wouldn't have -- would not have

### Plurals in parentheses
* Instead of putting optional plurals in parentheses, use either plural or singular constructions and keep things consistent throughout your documentation. 
Recommended:
* To find your API, visit the Creentials page. 
Not recommended:
* To find your API key(s), wait the Credential page. 
Recommended;
* The value of the parent depends on the values of its children. 
Not recommended:
* The value of the parent depends on the value(s) of its child(re).

### Possessives
* To form a possessives of a singular noun (regardless of whether it ends in *s* ), add  *'s*  to the end of the word.
  For examples:
  *alias's*
  *application's*
  *business's*  
  *user's*
* For a plural noun that 
	* Doesn't end in *s*, add *'s* to the end of the word, add *'s* to the end of the word.
	  For examples:
	  *women's*
    * Does end in *s*, add an apostrophe but no additional *s*.
      For examples:
      *the Williamses'*
      *users'*
* The possessive of *it* is a special case because it doesn't take an apostrophe. 
 For example, *Each component has its own set of traits.*
       
#### Company-and product-name possessives
* Avoid forming a possessive with a product name, regardless of who owns the product name. 
Recommended: The capabilities of Search are vast.
Not recommended: Search's capabilities are vast.
* To form the possessive of a company name, add *'s* to the end of the name.
Recommended: Google's new office is nearby. 

### Prepositions
* There's no rule against placing a preposition at the end of a sentence, place the preposition where it makes the most sense and makes the sentence easiest to read. 
Recommended: For details, see the client library documentation for the language you're interacting with. 
Not recommended: For details, see the client library documentation for the language with which you're interacting. 
* Omit unnecessary prepositions, and don't clutter the sentence with too many prepositions. 
Recommended: The icon for the connector manager turns green within a few minutes, and the connector instance is displayed shortly after. 

### Present tense
* In general, use present tense rather than future tense.
* Try to avoid using *will* where possible. 
Recommended: Send a query to the service. The server sends an acknowledgment. 
Not recommended: Send a query to the service. The server will send an acknowledgment. 
* Future tense is unavoidable where possible because you're talking about the future. 
 For example, *The hedgehog will hibernate starting in October.* 
* Also avoid the hypothetical future *would*. 
Recommended: If you send an unsubscribe message, the server removes you from the mailing list. 
Not recommended: If you send an unsubscribe message, the server would then remove you from the list. 

### Pronoun
#### Ambiguous pronoun references
* Avoid vague and confusing reference between a pronoun and its antecedent. 
Recommended: If you type text in the field, the text doesn't change. 
Not recommended: If you type text in the field, it doesn't change. 
Recommended: The name of the function to execute in the given script. The name doesn't include parentheses or parameters. 
Not recommended: The name of the function to execute in the given script. It doesn't include parentheses or parameters. 
* In many cases, it's best to use these types of words as adjectives modifying nouns instead of using them as pronouns. 
Recommended: Set this value to true. 
Not recommended: Set this to true. 

#### Gender - neutral pronouns
* Don't use gender-specific pronouns unless the person you're referring to is actually that gender. 
* In particular, don't use *him*, *his*, or *her* as gender-neutral pronouns, and don't use *he*, *she* , or other such punctuational approaches. **Instead, use the singular *they* **. 
* *Singular they* has been in use for a long time.
  *Singular they* is the use in English of the pronoun they or its inflected or derivative forms, them, their, theirs, and themselves (or themself) as an epicene (gender-neutral) singular pronoun. It typically occurs with an unspecified antecedent, as in sentences such as:
*Somebody left their umbrella in the office. *
*But a journalist should not be forced to reveal their sources.*. 
* For example, *Each student should save their questions until the end.*
or use a plural noun: *Students should save their questions until the end.*
or use the formal one: *One should save one's questions until the end.*
or use *his or her*: * Each student should save his or her questions until the end.*

#### Optional pronouns
* To avoid ambiguity and clarity meaning in sentences. use optional pronouns, such as *that* and *who*. 
Recommended: Make sure that all  the files are correct.
Not recommended: Make sure all the files are correct. 
Recommended: Right-click the link that you want to open. 
Not recommended: Right-click the link you want to open. 

#### Personal pronouns
* Avoid first-person pronouns (*I*, *we*, *our*, and *ours*) except in the following contexts:
	* The question in FAQs.
	* A document whose author makes comments in the first person. 
	* Using *we* to refer to your organization, after using your organization's name. For example, "Example Pet Store recommends that you feed your addrdvark Standardized Aardvark Treats. We cannot guarantee the happiness of your aardvark otherwise."
* Use the second - person pronoun (*you*) whenever possible. 

#### Relative pronouns
* *That* and *Which* don't mean exactly the same thing, so don't substitute one fro the other. 
* *That* introduces a restrictive clause. It isn't preceded by a comma. 
   Recommended: The echidna that has a long snout is furry. 
   This sentence describes a particular echidna, the one that has a long snout. 
*  *Which* introduces a nonrestrictive clause and is preceded by a comma. 
  Recommended: The echidna, which has a long snout, is furry. 
  This sentence describes all echidnas, and mentions in passing that they all have long snouts. 
* When referring to a person, use *who*, not *that*. 
 Recommended: Grant access to the autherticated user who provides an invitation token. 
 Not recommended: Grant access to the autherticated user that provides an invitation token. 
* You can use *whose* to refer to people, animals, and things. *Whose* is the possessive form of both *who* and *which*. 
 Recommended: Examine the variables whose values are set at compile time. 

### Second person
* In general, use second person rather than first person, that means *you* instead of *we*.
* It's important to figure out who the *you* is that you're addressing and to be consistent about that. Make it clear to the reader who you expect them to be. 
Recommended: If you're deleting multiple entries at a time. 
Not recommended: If we're deleting multiple entries at a time. 
* If you're telling the reader to do something, then use the imperative with an implicit *you*. 
Recommended: Click **Submit**. 
* This issue can also interact with tense. 
Recommended: Create an XML entry. 
Not recommended: You'll need to create an XML entry. 
* It's best to avoid *our*.
Recommended: For details, read *All About Pandas*. (All About Pandas is a hyperlink in blue)
Also recommended: For details, read the documentation. (the document isn't a hyperlink)
Not recommended: For details, read our documentation. 

### Spelling
* In general, in cases where American spelling differs from British spelling, use the American spelling.
* When in doubt about the spelling, first see the word list, then see Merriam-Webster's Collegiate Dictionary. 
Recommended: *color* not *colour*; *authorize* not *authorise*, *center* not *centre*
*accessorize* not *accissorise*; *curb* not *kurb*...

### Verb forms in reference documentation
* In a specification, that's aimed at implementors of an API, it may make more sense to use the verb form without the *-s*, In that context, you're telling the reader what their implementation of the method should do (create a new task), whereas in reference docs aimed at developers, you're telling them what the existing method does (creates a new task).

## Punctuation
### Colons
* When a colon introduces a list, the text that precedes the colon must be able to stand alone as a complete sentence. 
Recommended: The fields are defined as follows:
Not recommended: The fields are: 

#### Bold colon
* When non-italic text that precedes a colon is bold, make the colon bold too. 

#### Code text preceding colon
* When text that precedes a colon is tagged as <code>, don't include the colon in the <code> tagging unless it is part of the code. 

#### Colons within sentences
* In general, the first word in the text that follows a colon should be in lowercase. 
Recommended: Tone: concise, conversational, friendly, respectful. 
Recommended: When you add or update content to an existing project, remember to take these steps: review the style guide, use checklists, enlist a fellow writer or an editor to copyedit your work, and request a developmental edit if you feel that it's warranted.
* Unless the text is one of the following conditions:
	* A proper noun (Open source software: Istio)
	* A heading (capitalize the first word in a subheading after a colon, and any proper nouns or other terms that are always capitalized a certain way)
		* Even though you're using sentence case, don't put a period at the end of a title or heading. 
	* A quotation (Arthurian wit:"Bring me you sworde")
	* Text that follows a label, such as Caution or Note 

### Commas
#### Serial commas
* In a series of three or more items, use a comma before the final *and* or *o*. 
Recommended: I dedicate this book to my parents, Ayn Rand, and God. 
Not recommended: I dedicate this book to my parents, Ayn Rand and God. 

#### Commas after introductory words and phrases
* In general, place a comma after an introductory word or phrase. 
Recommended: Finally, only groups that contain parameters appear in this list. 
Recommended: Based on the requirements of your game, you can implement this method to update game information. 

#### Commas separating two independent clauses
When a coordinating conjunction (*and*, *but*, *or*, *nor*, *for*, *so*, or *yet*) separates two independent clauses, insert a comma after the first clause (before the conjunction) **unless both clauses are very short**.
Recommended: The libraries make feed creation easier, and they ensure that only valid feeds are produced. 
Not recommended: The libraries make feed creation easier and they ensure that only valid feeds are produced. 
Recommended: Type your ID and click **OK**.
Not recommended: Type your ID, and click **OK**. 

#### Commas seperating independent from dependent clauses
* When an independent clause and a dependent clause are separated by conjunction, insert a comma **only if**  the sentence could be misunderstood withoud one. 
Recommended: Direct-access flags are plain variables and can be read directly. 
Not recommended: Direct-access flags are plain variables, and can be read directly.
Recommended: The manager acknowledged the last team member who entered the room, and started the meeting. 
Not recommended: The manager acknowledged the last team member who entered the room and started the meeting. 

#### Setting off other kinds of clauses
* To set off certain kinds of clauses with a comma or other punctuation for clarity. 
* A  couple of specific places where commas are a good idea. 
	* In general, put a comma before the word *which* at the start of a nonrestrictive clause. 
	* in general, put a semicolon or a period or a dash before a conjunctive adverb, such as *otherwise*, or *therefore*, and put a comma after the conjunctive adverb. 
* In general, don't use a comma before the causal conjunction *because* unless it is being used at the start of a nonrestrictive clause. 
Recommended: Name of the group, which has a maximun length of 200 characters. 
Not recommended: Name of the group which has a maximun length of 200 characters. 
Recommended: The variable must have a value, otherwise, the server retures an error. 
Not recommended: The variable must have a value otherwise the server retures an error. 
Recommended: You can use the same key name in multyple backend services and backend buckets beacuse each set of keys is independent of the others. 
Not recomended:  You can use the same key name in multyple backend services and backend buckets, beacuse each set of keys is independent of the others. 

#### Punctuating numbers
* In accordance with standard American number-formatting.
* In numbers four or more digits long, use commas to set off groups of three digits. counting leftward from the dicimal point. 
* For more decimal numbers, don't use any digit-group separators to the right of the decimal point.  
|Recommend |Not recommended |
| -- | -- |
| The limt 1,532,782 bytes per day. | The limit is 1532782 bytes per day. |
| The API supports up to 2,000 vertices. | The API supports up to 2000 vertices.|
| $0.0316008/vCPU hour | $0.031 600 8/vCPU hour |

### Dashes
(* A hyphen (-) is a punctuation mark that's used to join words or parts of words. 
* A dash is longer than a hyphen and is commonly used to indicate a range or a pause. The most common types of dashes are the **en dash**, and the **em dash*.)

#### Em dashes
* Also known as a  long dash, to indicate a break in the flow of a sentence or an interruption.
* Don't put a space before or after it. 
(* Em dashes save other punctuation would be awkward. For example, em dashes can replace parentheses at the end of a sentence or when multiple commas appear in a parenthetical phrase. 
After a split second of hesitation, the second baseman leaped for the ball (or, rather, limped for it).
After a split second of hesitation, the second baseman leaped for the ball -or, rather, limped for it).
Microsoft system: 2014 + alt + x)

#### En dashes
* Don't use. Instead, use a hyphen or the word *to*.
* Range of numbers with units
* Range of numbers
(En dashes are slightly shorter than em dashes. 
* Using endashes to indicate spans of time or ranges or numbers. 
* Using endashes to indicate the connection between two words that are already hyphenated or when you are using a two-word phrase as a modifier, which is you create a compound word. 
* Microsoft system: 2013 + alt + x)

#### Colon instead of dashes in description lists
* It's common but nonstandard method to use an em dash, an en dashes or a hyphen surrounded by spaces to separate an item and its description. 
Recommended: Example: This is an example.
Not recommended: Example - This is an example.

### Ellipses
* Ellipses is the plural of ellipsis. An ellipsis is made up of** three** contiguous periods. Technically, the dots in an ellipsis are ellipsis points, but for our purposes, you can think of them as periods. 
* Ellipses indicate the omission of part of a sentence, paragraph, or larger block of text where the omission is not pertinent to the understanding of the subject at hand. 

#### Ellipses in a user interface
* When ellipses appear in a user interface, exclude them from the documentation describing the user interface unless their omission could cause confusion. For example, if the text on the button in the UI reads **Save...** document it as *click **Save** *. 

#### Ellipses in text
* Don't use ellipses in your written documentation. 
* It's acceptable to use ellipses in quoted text (to replace a portion of the quoted text) except when they appear at the beginning or end of the text.
Not Recommended: My high school English teacher made me learn that Shakespeare quote:"... all the men and women merely players."
Not Recommended: My high school English teacher made me learn that Shakespear quote:"All the world's a stage, and all the men and women merely players..."
Recommended: My high school English teacher made me learn that Shakespear quote:"All the world's a stage, .... And one man in his time plays many parts."

#### Punctuation and spacing of ellipses
* Keep all three ellipsis points together. 
* Insert one space before and after the ellipsis unless a punctuation mark immediately follows the ellipsis, in this case, don't insert a space after the ellipsis. 
Recommended: You don't need to understand all the other Python code in there ... we'll explain it all in class. 
Recommended: You don't need to understand all the other Python code in there ...; we'll explain it all in class. 
Not recommended: You don't need to understand all the other Python code in there...we'll explain it all in class. 

### Exclamation points
Don't use exclamation points in text except when thy're part of a code example. 

### Hyphens
#### Compound modifiers
* Use hyphenated compound modifiers before a noun. 
* A compound modifier acts as a single unit to modify the noun. 
* When you use a compound modifier after a noun, don't hyphenate it.
Recommended: The app uses Android-specific techniques.
Recommended: The app uses techniques that are Android specific.

#### Adverbs ending in *-ly*
Don't hyphenate adverbs ending in *-ly* except where needed for clarity.
Recommended: Free, simple, and publicly available implementations. 
Not recommended: Free, simple, and publicly-available implementations. 
Recommended: To get profile information for the currently authorized user. 
Not recommended: To get profile information for the currently-authorized user. 

#### When to hyphenate
* Don't hyphenate a word that has a prefix or suffix except in the following situations:
	* Where not doing so could cause confusion--for example, *re-count*, *re-mark*.
	* When a number or capital letter follows the prefix--for example, *non-English*, *pre-1500*, *post-twelfth graders*.
	* When the prefix ends in vowel, and the word it precedes starts with the same vowel--for example, *co-op*, *de-energize*. 
	* When the prefix is self--for example, *self-aware*, *self-important*. 
	* When the prefix is followed by a word that is already hyphenated.
	* When the prefix is followed by a compound word that contains a space. In this case, the space is replaced with a hyphen--for example, *twentieth century* but *pre-twentieth-century music*. 

#### Compound words
* Compound words are two or more words that are joined to form a new word. To determine whether to hyphenate a compound word to check the word list. 

#### Range of numbers
* Use a hyphen, not an en dash to indicate a range of numbers. 
* If a hyphen introduces ambiguity, use words *from*, *to*, *through* for clarity. 
* Don't mix hyphens with words. 
Recommended: 8-20 files. 
Recommended: from 8 to 20 files
Not recommended: from 8-20 files

#### Space around hyphens
* Never place a space on either side of a hyphen except when using a suspended hyphen, in which case you can leave a space after (bu not before) the hyphen. 

#### Suspended hyphends
* When two or more compound modifiers have a common base, you can keep the hyphens but leave out the base for all except the last modifier. 
Recommended: You can set up the system to scan for new files at one- or two-hour intervals. 
Recommended: You can set up the system to scan for new files at one-, two-, or three-hour intervals.

### Parentheses
* Don't put important information in parentheses.

### Periods
#### Periods with lists
* Whether to end a list item with a period depends on several factors, including the kind of list that the item appears in. 

##### Descriptions lists
* Don't put a period at the end of a term.
* Do put a period at the end of a description.
* In most contexts, start each term with a capital lette. 

Recommended:
The following words are adjectives:
**Big**
A short word.
**Relevant**
A fancy word.
**Gratuitous**
A long word.

**Emu**
The best kind of bird.
**Crow**
The other best kind of bird.
**Peacock**
Also the best kind of bird.

Not recommended:
The following words are adjectives:
* Big
* Relevant
* Gratuitous
* Purple--this is a color.

##### Bulleted lists
* In general, use a period at the end of each item in a bulleted list, except in the following cases:
	* If the items consists of a single word, don't add end punctuation.
	* If the item doesn't include a verb, don't add end punctuation. 
	* If the item is entirely in code font, don't add end punctuation.
	* If the item is entirely link text or a doucment title, don't add end punctuation.
Recommended:
You can do any of the following by using the API:
* Create an item.
* Replace one item with another.
* Update an item.
* Delete an item.

Recommended:
The API supports the following actions:
* Create
* Replace
* Update
* Delete

Recommended:
The SDK supports the following UI elements:
* Text box
* Bulleted list
* Button

##### Numbered lists
Use the same guidelines as for bulleted lists.

#### Period with URLs
* When a period follows a URL or a file path, it can be hard to tell whether the period is part of the URL. 
* To indicate that the punctuating period isn't part of the URL, try one of the following techniques:
	* Whenever possible, avoid putting URLs in text. 
	* Rewrite the sentence so that the URL isn't at the end of the sentence. 
	* Put the URL on a separate line from the text, omitting the final period. 
Recommended:
We use the feedback to improve the API, in accordance with Example Pet Store's Privacy Policy: http://www?examplepetstore.com/privacy/
Not recommended:
We use the feedback to improve the API, in accordance with Example Pet Store's Privacy Policy at http://www?examplepetstore.com/privacy/.

#### Periods with quotation marks
* When a sentence ends with material inside quotation marks, place the period inside the quotation marks even if the period isn't part of the material inside the quotation marks.
If the material inside the quotation marks ends with a question mark or an exclamation mark, don't use a period. 
Recommended: ...you might say "Fixed typo."
Recommended: Children always ask "Why?"

#### Periods with parentheses
* If the last part of a sentence is contained inside parentheses, put the period after the closing parentheses.
* If the parentheses contain a complete sentence, put the period inside the parentheses.
Recommended: Your application could show a notific when a relevant file or folder has changed (even if that change occurs while your application isn't running).
Recommended: App Engin applications are easy to create, easy to maintain, and easy to scale. (With App Engine, there are no servers for you to maintain.)

#### Periods with headings
* Don't end the headings with periods.

#### Periods with numbers
* Use a period to represent a decimal point.

#### Periods with captions
* In general, don't use periods with captions.

#### Periods with abbreviations
Abbreviations include acronyms, initialismes, shortened words, and contractions.
##### Periods with acronyms or  initialisms 
* Don't put periods after the letters of an acronym or initialism.
  For example, *NATO*, *CIA*. 
##### Periods with shortened words
Sometimes put a period after a shortened word.
* Put a period after a shortened word. For example, *Dr. for doctor*, *etc. for et cetera*, except for *date* and *time*. For example, *PM*, *AM*, *Jan*, *Feb*.
* Don't put periods after the short version if some words have a long version and a short version.
  For example, *app for application*, *min for minutes*, *demo for demonstration*
* Don't use a period with an abbreviation for the name of a country. For example, *US state*, *the District of Columbia (DC)*. 

### Quotation marks
#### Commas and periods with quotation marks
* Commas and periods go inside quotation marks in the standard American style, despite it being inconsistent with the standard British style. 
American: See the section titled "Care and feeding of the emu."
British (Not recommended): See the section titled "Care and feeding of the emu".
* When you put a keyword or other literal string in quotation marks, put any other punctuation outside the quotation marks. 
* Don't put quotation marks around an item that's in code font, unless the quotation marks are part of the item.
Recommended: If you enter `escape`, the program crashes. 
Acceptable: If you enter "escape", the program crashes.
Not recommended: If you enter "escape," the program crashes.

#### Straight and curly quotation marks
Curly quotes are the quotation marks used in good typography. There are four curly quote characters: the opening single quote, the closing single quote, the opening double quote, and the closing double quote.
Straight quote are a typewriter habit. In traditional printing, all quotation marks were curly. But typewriter character sets were limited by mechanical constraints and physical space. 

* Most typefaces support two forms of quotation marks and apostrophes: straight marks and curly, or typographic marks. Some tools like Google Docs, automatically convert straight quotation marks and apostrophes to the curly versions. However, our guidance is to **always use straight quotation marks and straight apostrophes** for the following reasons:
   * It's easy to get the direction of curly quotation marks (especially apostrophes) wrong. Using straight marks avoids this problem.
   * Code requires straight marks.
   * Coding tools (for example, Subversion)don't produce curly marks by default.
   
### Semicolons
#### Between two independent clauses
* Use a semicolon between two closely related independent clauses that are not quite unrelated enough to merit a period, but where a comma isn't quite enough. 
Recommended: The Earth Engine image must have exactly one or three bands when exporting to GME; other images cause the export to fail.
Recommended: You can easily test compatibility by computing the centroid; if it is on the opposite side of the planet, reverse the order of your vertices. 

#### Before a conjunctive adverb
* A semicolon precedes a conjunctive adverb that joint two independent clause. Conjunctive adverbs includes: *accordingly*, *also*, *besides*, *consequently*, *furthermore*, *hence*, *however*, *indeed*, *in face*, *likewise*, *similarly*, *therefore*, and *thus*.
Recommended: The style of this button is up to your; however, you must still follow branding guidelines.
Recommended: This setup places the head-tracked node below the Main Camera; therefore, only the stereo camera are affected by the user's head motion.

#### Before an independent clause
* A semicolon can appear before an independent clause that is introduced by a phrase such as *that is*, *for example*，or *namely*. 
Recommended: The next polling interval to use; that is, the number of seconds before the client should contact the server again.
Recommended: The URL from which a video ad loads; that is, the URL to use to fetch to the video ad. 

#### Between complex items in a series
* When you have a series of long or complex items, such as items that themselves contain punctuation, use semicolons, rather than commas, as separators. 
Recommend: If you don't have time, then focus on the improvements that will have the greatest benefit: what matters most to your users; what is most important to fix; and what is easy or feasible to fix in the available time. 
Recommended: Review your document one more time, checking for the following: present tense and active voice; typos, punctuations, and grammar; and whether you can shorten anything. 

#### Single quotation marks
* The only times to use single quotation marks are the following:
   * In code examples, in language that use single quotation marks.
   * When nesting a quotation inside another quotation.
American (and Google): She said, "I heard him shout 'Help', and saw him floundering in the water".
   
### Slashes 
#### Slashes with dates
* Don't use date formats that rely on slashes.
Recommended: Call this method five or six times.
Not recommended: Call this method 5/6 times.

#### Slashed with alternatives
* Don't use slashes to separate alternatives.

#### Slashes with file path and URLs
* Use forward slashes, as appropriate, in computer file paths and URLs.
Recommended:https://developers.google.com/cardboard/
* Where very long URLs extend beyond a line, add a line break immediately after a slash. Don't ever insert an extraneous hyphen into a URL to break it between two lines. 
Recommended: https://developers.google.com/
cardboard/

#### Slashes with fractions
* Don't use slashes with fractions because they can be ambiguous.
3/4 could be interpreted either as three-quarters or as stating that 4 is an alternative to 3.
Recommended: 3/4 (fractions format)
Recommended: 0.75
Recommended: 75%
Not recommended: 3/4

#### Slashes with abbreviations
* Don't use abbreviations that rely on slashes. Instead, spell the words out. 
Recommended: care of, with
Not recommended: c/o, w/

## Formatting and organization
### Dates and times
#### Expressing times
* Use the 12-hour clock, except it required to use 24-hour time.
* If the UI, a command, or a code sample uses the 24-hour format, use that format throughout the page for consistency. 
* Use exact times when possible, but **noon** and **midnight** are OK.
* Use hyphens in time range. Don't add spaces before or after the hyphens. 
Recommended: 5-10 minutes ago.
* Capitalize AM and PM, and leave one space between it and the time. 
Recommended: 3:45 PM.
* Remove the minutes from round hours.
Recommended: 3 PM.

##### Expressing time zones
* Avoid using time zones unless in cases where you need to use a time zone-such as describing real events at real times-use the following guidelines:
	* Let the reader know if the time is local to their time-for example, *10 AM your local time*. 
	* If a time zone is necessary, use the timestamp format as seen in the user interface (if available).
	* If using a specific time zone, spell out the region and include the UTC or GMT label as a parenthetical. For example:
		* US and Canada Pacific Standard Time (UTC-8)
		* US and Canada Pacific Daylight Time (UTC-7)
	* Don't abbreviate the name of the time zone. 

### hen giving only the month and year, don't use a comma.
Recommended: She was born in January 2017.
* In most cases, don't abbreviate the day of the week or the month. However, when conserving space, such as in a heading or table, it's okay to abbreviate the month and the day of the week to their three-letter abbreviations. Capitalize the first letter and don't add a period at the end of the abbreviation.
* If you abbreviate, do so for the entire date. Don't mix written-out forms with abbreviated forms in the same date.
* Be consistent in where you apply abbreviations throughout your documentation. If you choose to abbreviate in table cells, do so in all table cells.
Recommended: Mon, Sep 3, 2019
Not recommended: Mon, September 3, 2019

##### Dates in the middle of a sentence
* When a `MONTH_DAY, YEAR` date appears in the middle of a sentence, add a comma after the year. 
Recommended: The January 19, 2019, release of...
* However, if the date in the middle of the sentence consists of the month and year only, don't use a comma. 
Recommended: The January 2019 release of...

##### Why we prefer dates written out
* Don't express months as numbers unless you don't have the option, because different regions of the world put parts of the date in a different order for numeric dates. 
	* In the UK, the order is usually day, month, and then year.
	* In the US, the order is usually month, day, and then year.
	* In some other parts of the world, the order is year, month and then day.
	Recommended: February 12, 2019
	Recommended: Sunday, February 12, 2019
	Not recommended: 02.12.2019
	Not recommended: 02/12/2019
	
##### Numeric-only date format
* If you must express a date in numerical date format, use the format `YYYY-NN-DD`,  and separate the elements by using hyphens. This conforms to ISO 8610 international standards for numerical date format. 
Recommended: 2019-04-04
Not recommended: 2019/04/05

##### Expressing divisions of the year
* Avoid referring to seasons. 

### Figures and other images
* Use imgage only  when they provide useful explaination, or for screenshots of UIs that are important to discuss. 
* Use SVG files if possible because SVGs stay sharp when you zoom in on the image. If you do'nt have an SVG file, then save it as a PNG file. 
* If you're exporting an image to a format that can include information on seperate layers (for example, PDF or TIFF), flatter the image an export. 
* Don't use image maps, instead, provide a list of thext references following the image.  

#### Creating and saving images
* Don't use images of text, code samples, or terminal output, use actual text. 
* Make your screenshots of windows looks like reeal windows, for example, include the windows 's title bar, and if the window has a drop shadow, then include the drop shadow. 
* Don't include personally identifying information (PII). If a source screeshot includes PII, hide it with a solid-color overlay with 100% opacity. Don't rely on blurs, mosaic effects, such effects can be reversed to reveal the original information.

#### Text associated with images
* An introductory sentence should precede images. The sentence can end with a colon or a period:
	* If it immediatetly precedes the image, ues a colon.
	* If there's more material, such as a note paragraph between the introduction and the image. * You don't need to introduce screenshots that immediately follow procedural text that describes a UI.

##### ALT text
* A concise description of the image that can replace the image.in situations where the image isn't visible.
* Alt text is used by assistive technologies, such as screen readers, and might appear if the image cannot load. 
* If the image is decorative (not informative) or it's provided only as a visual aid for information, then provide empty alternative text `alt=''`
* When using the `<img>` element, the `alt` attrubute is required, even if its assigned valued is an empty string. 
* Don't include phrase like *image of* or *photo of*. 
* Include puntuation. 
* Use consistent alt text for repeated instances of an image, such as controls, status indicators, or icons that appear multiple times in your document.
* When possible, avoid using alt-caps in alt text.
* Don't introduce diagrams in the alt text. 
* Use full sentences. 
* Keep alt text length to 155 charatcters or less. 
For example, An emu foot has three toes. 

##### Figure caption
* A description of the image that provides more information about the image, which are concise and comprehensive summaries of a figure or image. 
* Figure captions attribute are optional. 
* Use punctuation in figure captions.
* When you refer to a figure, don't use spatial description such as "the imge below". Instead, mention it by number. 
For example, "...as shown in figure 1." Don't capitalize the word *figure*.

##### Figure description
* A textual representation of the figure, the information that is conveyed in the image is captured in the text, and the information about what an image is trying to convey. 
* Use when a figure caption doesn't convey the purpoes or complete information of the figure. 
* Use punctuation in figure descriptions. 

##### Text in figures
* When possible, avoid using explanatory text in screenshot graphics.
* If you must embed text in an image, then be sure to also provide the same information in a form that people with visual disablilities can use, such as a figure description.
* Keep text brief. Avoid complete sentences and punctuation when possible. 
* Don't include figure descriptions or captions in the figure or image. Instead, put figure descriptions and captions in text following the figure. 
* Use sentence case. 
* Use numbered callouts in figures to help you writer a figure description.
* Use full trademarked product names. 

#### Laying out image on one page
* To place the image align left. 
* Don't center the image on the page.
* Don't make your image too small. It's fine for an image to take up the full width of a page. 
* Don't use an image that's wider then the column it appears in. For example, the main-body column is 856px wide, so use images that are no wider then that. In that context, the high-resolution 2x version of the image should be no wider than 1712px. 
* Screenshots at full resolution often take up too much space on the page, so you may have to resize them. 
* If the images designers provide are wider than 856px, ask them to provide the relevant graphics as 856px/1712px pairs. 

### Footenotes
* Avoid using footnotes beacause they aren't accessible and can present challenges for localization efforts. 
* Instead of a footnote, consider using the following formats to convey information:
	* Add a link.
	* Use a note.
	* Put it in a parenthetical.
* Use a symbol instead of a number, if the only way to convey this information is to use a footnote. Use symbols in the following order:	
	* `*`	
    * `#`
Recommended: You want to add a footnote to this sentence.*
Not recommended: You want to add a footnote. 1

### Headings and titles
* Use descriptive headings and titles because they help a user navigate their browser and the page. 

#### Formatting a heading or title
* Use sentence case for headings and titles. 
* Use punctuation in heading sparingly. Punctuation can be a sign that your heading is too complicated. Consider rewriting. 
* When using an abbreviation in a heading or title, spell out the abbreviation in the first paragraph that follows the heading or title. 
* Avoid using code items in headings when possible. 
* To change the visual formatting of a heading, use CSS rather than using a heading level that doesn't fit the hierarchy.
* Don't put a link in a heading.
* Don't skip levels of the heading hierarchy. 
  Recommended: 
  # Level 1
  ## Level 2
  Not recommeded:
  # Level 1
  ### Level 3
* Don't use empty headings or headings with no associated content. 
  Recommend:
  ## Level 2
  This level is considering to ...
  Not recommended:
  ## Level 2
  ### Level 3
  This level is considering to...
#### Referring to subsections
* In a section of the page that summarize the following subheadings-for example, an H2 section that discusses the following H3 sections-use the phrase *in the following sections* to connnect to heading together. 
* Don't use the phrase *in this section* or *in these sections* because these phrases are too ambiguous. 

### Key terms
* When need to draw attention to a particular word or phrase in the prose of your documentation, such as when introducing a key concept or new word, or when discusssing a particular word, use italics. 
Recommended: A *Clos network* is a kind of multistage circuit switching network...
Not recommended:  A **Close network** is a kind of multistage circuit switching network...

### Letters an letters (Pluralizing a single letter)
To form the plural of a single letter, italicize the letter and add an apostrophe followed by the unitalicized letter s.
Recommended: We called tech support because the printer wasn't printing uppercase *B*'s or lowercase *P*'s. 
Recommended: Mind your *P*'s and *Q*‘s. 

## Linking
### Cross-references
* In general, cross-references link to nonessential information that adds to the reader's understanding. To get more information, read [Capitalization in references to titles and heading](#reference1).
* **This markdown syntax can only be interpreted by haroopad.**

#### References to other documents
Recommended: To begin coding right away, read [Building your first app](www.bing.com)
Not recommended: See [this blog post]().
Not recommended: Click [here]().
* Don't force links to open in a new tab or window. Let the reader decide how to open links. 
<a href="/style/accessibility" target="_blank">Accessible content</a>
<a href="/style/accessibility" target="_blank">Accessible content (opens in a new tab)</a>
* In the rare situation that a link needs to open in a new tab or window, let the reader know that the link opens differently than expected. 
Recommended:
<a href="/style/accessibility" target="_blank">Accessible content (opens in a new tab)</a>
Not recommended:
<a href="/style/accessibility" target="_blank">Accessible content</a>
* When the link text doesn't clearly indicate why you're referring the reader to this information, then give an explanation, but don't repeat the link text. 
Recommended: For more information about authentication and authorization, see [Using OAuth 2.0 to access Google APIs]().
* If a link downloads a file, then make that clear in the link text, and mention the file type. 
Recommended:
For more information, [download the security features PDF.]() 
* Click the link to the doloading web*.
* To avoid link fatigue, don't provide duplicate links to the same document within a given page. It's OK to add a secondary link if you're linking to a particular section of another page. 

#### Wording cross-reference
When a cross-reference includes information that describe the cross-reference links to, Use *about* instead of *on*.
Recommended: For more information about indexes, see [Managing indexes]().
Not recommended: For more information on indexes, see [Managing indexes]().

#### Formatting cross-reference
* When a cross-reference is a link, don't put the link text in quotation marks.
Recommended: For more information, see [Meet Android Studio]().
Recommended: Learn about [what's new in Android Wear 2.0]().
Not recommended: For more information, see "[Meet Android Studio]()".
* For an unlinked reference to a document section, or part of a series, such as an episode in a web series, use quotation marks.
Recommended: For more information, see "Describing system versions" in the following section.
* For an unlinked reference to the title of a full-length work, such as a book, movie or web series, use italics.
Recommended: see *The Chicago Manual of Style*.

#### URLs in links to pages on the same server
* When you're linking to another page on the same server, use a site-relative URL starting with `/`.

#### URLs in links to pages on a different server
* If the server that you're linking to supports HTTPS, start the URL with `https`. 
* If the server doesn't support HTTP, start the URL with `http`.
* Use an external link icon to indicate that the link goes to a different domain or server. 
Recommended: For more information, see [Links and Hypertext]()(Here is an external link icon).

### Headings as link targets
#### Add a custom anchor
You might want to add a custom anchor to a heading for several reasons:
* You want to use an anchor that's shorter than the automatically generated anchor.
* Add a custom anchor reduces the likelihood of breaking existing links if the heading text changes later.

#### HTML 
* Add a `section` element with an `id` attribute, and put hyphens between words. Don't use `<a name>`. 
Recommended:
`<section id="reference-to-guide">
<h2>Reference to guide</h2>
...
</section>`
Acceptable:
`<h2 id="reference-to-guide">Reference to guide</h2>`

#### Markdown
* To add an anchor to a heading in MD, replace `ID_OF_ANCHOR` with the ID for this heading. 
* Use lowercase for `id` values, and put hyphens between words.
Recommended:
`## Help conserve habitat for pollinators {: #help-conserve-habitat-for-pollinators}

### Link text
* To write link text, use descriptive phrases that provide context for the material that you're linking to.
* Different readers experience links differently. 
  * Users of screen reader software ofen jump from one link to the next without reading the words.
  * Other readers visually scan a documentation to find relevant links. 
  * Effective link text helps to improve accessiblity and scannability.
  
#### Structuring link text 
* To write link text effectively, use one of the following forms:
  * Make the link text match the title or heading that you're linking to.
  Recommended: For more information, see [Link text]().
  
#### Writing link text
Apply the following guides when you write link text:
* When you write a complete sentence that refers the readers to another topic, introduce the link with the phrase *For more information, see...* or *For more information about..., see...*.
* When you write unique, descriptive link text that makes sense without the surrounding text. Don't use phrases like *click here*, or *click this document*. They're bad for accessibility and scannability.
Recommended: For more information, see [Care and feeding of your wombat]().
Not recommended: Want more? [Click here]().
Not recommended: For more information, see [this document]().
* Don't use a URL as link text. Instead, use the page title or a description of the page. 
Recommended: For more information about protocols, see [www.w3.org]
Not recommended: See the HTTP/1.1 RFC at <a href="http://www.w3.org/Protocols/rfc2616/rfc2616.html">http://www.w3.org/Protocols/rfc2616/rfc2616.html</a>.
* In some legal documents, such as Terms of Service documents, it's okay to use URLs as link text. 
* When link text is a description of the target page, use the following guidelines to help users can determine if the link is relevant:
  * Keep link text short where possible. 
  * Place important words at the begining of the link text. 
  * Don't use the same link text in the same document for different target pages.
*  Use expternal link icon appropriately.
*  If a link downloads a file, write link text that indicates this actions as well as the file type.
Recommended:
	<a href="/readme.txt">download the README.txt file</a>.	
* If the text includes an abbreviation in parentheses, include the long form and the abbreviation in the link text. 
Recommended: [Google Kubernetes Engine (GKE)]()
Not recommended: [Google Kubernetes Engine]()(GKE)

#### Punctuation with links
* If you have punctuation immediately before or after a link, put the punctuation outside out the link tags. 
Recommended: For more information, see <a href="#Test your code</a>.
Not recommended: For more information, see <a href="#Test your code.</a>

#### Styling link text
If you write sitewide CSS for your website, apply the following styling guidelines:
* Contrast link text color and regular text color.
* Underline link, and don't underline non-link text.
* Make visited link change color. 
  
### Linking to other sites
* When the information relies on something about third-party, it's better to link to good documentation elsewhere than to try to thoroughly document someone else's standart in out documentation. 
* Sometimes a few sentences of basic information can save readers a trip to an external site. For example, API documentaion has traditionally included a brief explanation of REST. As knowledge of REST becomes more widespread, we might be able to assume that readers already know about it, and can remove those brief explanations. 
* Another example. 
  * If you want to mention one HTTP status code, then decribing it in your document to make sense. 
  * If you want to make sure that your reader understand the idea of HTTP status codes, then linking them to an external document, such as the HTTP spec, might be a good idea. 
  * If you might discuss third-party tools or products, in such cases, it's okay to link to a relavant site. 
  * Make sure that any site that you link to is high quality, reliable, and respectable. 
  * If the URL has a local indicator, remove it and then test the link. For example, in a Wikipedia link, 
  change the following:
  https://en.wikipedia.org/wiki/Oprating-system-level_virtualization
  to this:
  https://wikipedia.org/wiki/Oprating-system-level_virtualization
* Don't force links to open in a new tab or window. Let the reader decide how to open links. 
  * In the rare situation that a link needs to open in a new tab or window, let the reader know that the link opens differently than expected. 
  Recommended: 
  <a href="/style/accessibility" target="_blank">Accessible content (opens in a new tab)</a>   
* Use an external link icon after the address of the external link.
  
### URLs for images
* When you're including an image that's served from the same domain as your page, use a relative URL starting with `/`. 
#### HTML
Insert the URL in the src attribute of your <img> element.
```
<img
  src="/shared/images/arrow-24.png"
  alt="Alt text description of arrow image."
/>
```

#### Markdown
Insert the URL in parentheses after the image's alt text.
`![ALT text.](/shared/images/arrow-24.png)`

## Computer interfaces
### API reference code comments
* When you're documenting an API, provide a complete API reference. 

#### Documentation basics
* The API reference **must** provide a description for each of the following:
	* Every class, interface, struct, and any other similar member of the API (such as union types in C++).
	* Every content, field, enum, typedef, etc. 
	* Every method, with a description for each parameter, the return value, and any exceptions thrown. 
	
#### Classes, interfaces, structs
* Make the first sentence unique and descriptive, yet short.
	* Don't repeat the class name in the first sentence. 
	* Don't say "this class will/does.."
The following example is the first sentence of the description for Android's `ActionBar` class:
*A primary toolbar within the activity that may display the activity title, application-level navigation affordances, and other interactive items.*

#### Method
* In the first sentence for a method description, briefly state what actio the method performs. In subsequent sentences, explain why and how to use the method, state any prerequistes that must be met before caling it. 
  For example, here's the description for Android's `Activity.isChangingConfigurations()` method:
  *Checks whether this activity is in the process of being destroyed in order to be recreated with a new configuration. This is often used in `onStop()` to determine whether the state needs to be cleaned up or will be passed on to the next instance of the activity via `onRetainNonConfiguration().*
* Use present tense for all descriptions. For example, *Adds a new bird to the omithology list.*

#### Description
* If a method performs an operation and returns some data, start the description with a verb, for example: 
*Adds a new bird to the omithology list and returns the ID of the new entry.*
* If it 's a "getter" method and it returns a boolean, start with "Checks whether ..."
* If it's a "getter" method and it returns something other than a boolean, start with "Gets the..."
* If it has no return value, start with a verb like one of the folloowing:
	* Turning on an ability or setting:"Sets the ..."
	* Updating a property: "Updates the ..."
	* Deleting something:"Deletes the ..."
	* Registering a callback or other element for later reference:"Registers ..."
	* For a callback: "Called by ..." For example, "Called by Android when ..."

#### Parameters
* Capitalize the first word, and end the sentence or phrase with a period. 
* Begin descriptions of non-boolean parameters with "The" or "A" if possible:
	* *The ID of the bird you want to get.*
	* *A description of the bird. *
* For boolean parameters for requesting an action, start sentences with "if ture ..." and "if false ..."
	* *If true, turn traffic lines on. If false, turn them off. *
* * Don't put the words "true" and "false" in code font or quotation marks.

#### Return values
* Be as breif as possible in the return value's description.
* Put any detailed information in the class description.
	* If the return value is anythins other than a boolean, start with "The ..", for example:
		* *The bird specified by the given ID.*
	* If the return value is a boolean, use the format "True if ..."; false otherwise, for example:
		* *True if the bird is in the sanctuary; false otherwise.*

#### Exceptions
* Where the reference generator automatically insert the word "Throw", begin your description with "If ...", for example:
	* *If no key is assigned.* 
* Otherwise use "Throw when", for example:
	* *Throw when no key is assigned." 

#### Deprecations
* Tell the user what to use as a replacement. For example:
	* *Deprecated. Use #CameraPose instead.*
	* *Deprecated. Access this field using the `getField()` method.

### Code in text
* In HTML, use <code> element.
* In MD, use backticks (`).

####  Method name
* Omit the class name, for example:
	* Recommended: To retrieve the zebra's metadata, call its `geet()` method.
	* Not recommended: To retrieve the zebra's metadata, call its `animal.get()` method. 

#### HTTP status codes
* Call it a status code instead of a response code or error code, and put the number and the name in code font, Use the following formatting:
  an HTTP `400 bAD Request` status cod
* To refer to a range of codes , use the following form:
  an HTTP `2xx` or `400` status code
* If you prefer to specify an exact range, you can do so:
  an HTTP status code in the `200` - `299` range. 

#### Keywords
* Don't use keywords as verbs or nouns.
* Don't  try to inflect them.
* Don't form pjurals and don;t make them possesive.
* It's okay to use lowercase, plain text string to discuss the `string` dada type
|Recommend |Not recommended |
| -- | -- |
| To retrieve the data, send a `GET` request. | Retrieve inofrmation by `GETting` the data.|
| You can't close the file before opening it. | Close()ing the file requires you to have open()ed it first.|

### Code samples
* Don't use tab, instead, use spaces.
* Mark code block as preformatted text. In HTML, use a `<pre>` element; In MD, indent every line of the code block by four spaces (**tested in haroopad and typora, both of them use four sapces to indent, and both of them can interpret html tag `<pre>`) or use a code fence (```)**.
* For most programming, indent by two spaces per indentation level. However, for Python and the Android Open Source Project, use four spaces. 
For example:
<pre class="prettyprint">
function helloWorld() {
  alert('Hello, world! This sentence is so long that it wraps onto a second
    line.');
}
</pre>

    function helloWorld() {
      alert('Hello, world! This sentence is so long that it wraps onto a       second
        line.');
    }

#### Introductory statements
* In most cases, precede a code sample with an introductory sentence or paragraph. 
* The introduction can end with a colon or a period; usually a colon if it immediately precedes the sample; usually a period if there's more material between the introduction and the sample; or if the introduction paragraph ends in a sentence that isn't directly related to the sample.
Recommended: The following code sample shows how to use the method. For more information about other methods, see [link]. (sample)
Recommended: The following code sample shows how to use the method: (sample)  For more information about other methods, see [link].
Not recommended: The following code sample shows how to use the method. For more information about other methods, see [link]: (sample)

### Command-line syntax
#### Formatting 
* Use a `<pre>` element in HTML.
* In MD, indent every line of the code block by four spaces (**tested in haroopad and typora, both of them use four sapces to indent, and both of them can interpret html tag `<pre>`) or use a code fence (```)**.
* For multiple elements, do the following:
	* When a line exceed 80 characters, add a line break before some characters, such as a single hyphen, double hyphen, underscore, or quotation marks.
	* After the first line, indent each line by four spaces to vertically align each line that follows a line break.
	* When you split a command line with a line break, each line except the last line must end with the command-continuation charatcter with which can work for commands.
		* Linux or Cloud Shell: A backslash typically preceded with a space ( \)
		* Windows: A caret preceded with a space ( ^)

#### Command prompt
* For the multiple-lines of input, then start each line of input with the `$` prompt symbol. 
* Don't show the current directory path before the prompt, even if part of the instruction incluces changing direactories. 
* If the overall context of the command interface changes, such as from the local machine to a remote machine, then add an additional prompt indicator for the new context.
Recommended:
`$ adb devices`
Rcocommended:
`$ adb shell
shell@ $ screencap /sdcard/screen.png
shell@ $ exit
$ adb pull /sdcard/screen.png`
* When showing a one-line command, the command prompt is optional for the `$` symbol.
* If the document includes both multi-one and one-line commands, then using the command propt for all the commands for consistency. 
* If the document includes a combination of input  lines, then using seperate code blocks for input and output. 
Recommended:
`$ cat ~/.ssh/my-ssh-key.pub`
The output is similar to the following:
Recommended:
`ssh-rsa KEY_VALUE USERNAME`

#### Required items
* Use text without breakets or braces for commands and arguments (Depending on the circumstances), this is likely to be in code fond.
Recommended: (in the following examples, all words and arguments are required)
`gcloud compute project-info describe`
`gcloud alpha functions get-logs FUNCTION_NAME`

#### Optional arguments
* Use square brackets around an optional argument. 
* If there are more than one optional argument, enclose each item in its own set of square brackets.
Recommended:
`gcloud dns GROUP [GLOBAL_FLAG] [FILENAME]`

####  Mutually exclusive arguments
* Use curly braces to indicate that the use must choose one and only one of the items inside the braces. 
* Use vertical bars (also known as pipes) to indicate the seperate the items. 
* There can be more than two mutually exclusive choices, seperated from each other by pipes.
Recommended (choose either of them)
`{FILE_1|FILE_2}`
Recommended (optional)
* Lef side of pipe, if the souce code is deployed from a cloud repository, the following is requried:
Recommended:
`--source=CLOUD_SOURCE --source-url=SOURCE_URL`
* Right side of pipe, if the source code is in a local directory:
Recommended:
`{--source=CLOUD_SOURCE} --source-url=SOURCE_URL | --bucket=BUCKET [--source=LOCAL_SOURCE]}`

#### Repeat argument
* Use an ellipsis (...) to indicate that the user can speicify multiple values for the argument.
Recommended:
`gcloud dns GROUP [GLOBAL_FLAG ...]

#### Output from commands
* Don't have to show the output for every command. 
* Only add output if it adds value. 
	* If the reader needs to copy a value from the output. 
	* Or need to verify a value in the output. 
* Seperate the command from the output. 
Recommended:
The output is similar to the following:
The output is the following:

#### Command line terminology
* Avoid mapping nomenclature of the `gcloud` tool's commands to Linux commands.
* Linex commands can describe what the entire command does. 

##### gcloud commands
* You can use commands alone or with one or more flags. For example:
Command alone:
`gcloud init`
Command with a flag:
`gcloud init --skip-diagnostics`

##### Linux commands
* Linux commands use options parameters, arguments, and a host of specialized syntax elements. 
For example:
`find /usr/src/linux -follow -type f -name '*.[ch]' | xargs grep -iHn pcnet`
The command consists of the following elements:
* `find` is the command name.
* `/usr/src/linux` is an argument that specifies the path to look in. 
* `-follow` is an option. The hyphen `-` often called a dash, is part of the option. 
* `-type` is an option with a value of `f`.
* `-name` is an option with a value of `*.[ch]`, where the asterisk (`*`) is a metacharacter signifying a wildcard. 
	* Metacharacters are used in Linux shell commands for globbing or filename expansion. 
	* In addition to the asterisk, metacharacters include the question mark (`?`) or caret (`^`).

### Placeholders formatting
#### Placeholder variables in inline text
* In HTML, wrap placeholders in `<code><var> elements like this:
  `<code><var>PLACEHOLDER_VARIABLE</var></code>`
* In MD, wrap placeholders in backticks(`), and use asterisks before, like this:
 (*`PLACEHOLDER_VARIABLE`*).

#### Placeholder variables in blocks
* In HTML, wrap the code block in a `<pre>`element, and tag placeholders with <var> elements.
<pre class="devsite-click-to-copy">
gcloud compute forwarding-rules create <var>FORWARDING_RULE_NAME</var> \
    --global | --region=<var>REGION</var> \
    --load-balancing-scheme=<var>LOAD_BALANCING_SCHEME</var> \
    --network=<var>NETWORK</var> \
    ...
</pre>
* In MD, wrap the code block in a code fence (```), like this:
 ```
 PLACEHOLDER_VARIABLE
 ```
#### Placeholder variable text
* Use uppercase characters with underscore delimiters:
In HTML:
Recommended:
https://developers.google.com/<var>API_NAME</var>
Not recommended:
https://developers.google.com/<var>API-name</var>
In MD:
Recommended:
https://developers.google.com/*`API_NAME`*
* Don't include possesive pronouns in placeholders.
Not recommended:
https://developers.google.com/<var>MY_API_NAME</var>

#### Explaining placeholders
* When you use a placeholder in text or code, include an explaination for the placeholder for the first time you use it. 
The following is an example of a command that use a placeholder with an explanation of that placeholder:
<pre class="devsite-click-to-copy">
gcloud compute instances create <var>INSTANCE_NAME</var> \
    --metadata enable-guest-attributes=TRUE
</pre>

<p>Replace <code><var>INSTANCE_NAME</var></code> with the name that
you want your new VM instance to have.</p>

### UI elements and interaction
#### Focus on the task
* What the user should accomplish, rather than focusing on the gestures when state instructions. 
* Avoid to referring to UI elements, help the user understand the purpose of an instruction.
Recommended: Refresh the page.
Recommended: Click **Refresh**.
Not recommended: Click the REFRESH button.
Recommended: Expand the **Advanced options** section.
Recommended: To expand the **Advanced options** section, click the expander arrow. 
Not  recommended: Click the zippy to expand the **Advanced option** section. 

#### Formatting names of UI elements
* When referring to any UI element by name, put its name in bold.
* Include names for buttons, menus, dialogs, windows, list items, or any other feature on the page that has a visible name. 
* Don't use code font for UI elements, unless it's an element when required. In that case, use both code font and bold. 
* Don't make an official feature name or product name bold, except when it refers to an element on the page that uses the name, such as a window title or button name. 
* Use sentence case. 
| Guidance | Recommended |  Not recommended |
| -- | -- | -- |
|Use sentence case and appropriate formatting and terminology for all labels.| In the **New Project** window or In **New project**, select the **New Activity** checkbox or select **New activity**, and then click **Next**. | In the New Project window, select "New Activity", and then click the "Next" button.|
|When a label is all uppercase, use sentence case.| Click (<the refresh icon>) **Refresh**.| Click REFRESH. |
|When referring to multiple labels that are inconsistently, use sentence case for all of the labels.| Click **New project**, and the click **New activity**.| Click **NEW PROJECT**, and then click **New Activity**. |

#### Referring to UI elements
* Don't use UI elements as if they were verbs or nouns.
|Recommended| Not recommended|
| -- | -- |
| In the **Name** field, enter an account name.|Name the account.|
| To save the settings, click **Save**.| **Save** the settings.|
| In the **Service account ID** field, or in the **Service account ID**, enter a name. | Specify a **Service account ID**.|

#### Terminology and usage
* If you want to clarify for the reader, add the name of the UI element. For example, both of the following sentences are valid:
Recommended: Go to **File > Tools**.
Recommended: In the **File** menu, click ** Tools**. 

#####  Windows, pages, dialogs and panes
**Windows**
* * Most often, a window is the entire application window in a desktop environment, it can also refer to modular application elements that you can open and close. 
Recommended: In the **MyApp** window, click  **Edit**.
Not recommended: In the **MyApp** page, click **Edit**.  
**Pages**
* Page is referring to a web page in general, and to a sub-page of a console in particular.
Recommended: In the Google Cloud Console, go to the **Development** page.
Not recommended: In the Google Cloud Console, go to the **Development** window.
**Dialogs**
* A dialog is a smaller window that is detached from the main window and appears in front of the window. 
Recommended: In the **Welcome** diaglog, click **OK**.
Not recommended: n the **Welcome** pop-up window, click **OK**.
**Panes**
* A pane, originally means a section of a window, 
* A pane is similar to a window inside of the application. 
* A pane is tightly coupled to the other UI regions and usually cannot be hidden on its own.
* Whereas, a window is distinctly seperate and can be hidden. 
Recommended: In the **Create service account** panel, click **Start**.
Not recommeneded: In the **Create service account** window, click **Start**.

##### Menu bar
* The menu bar appears at the top of the window or at the top of the screen, 
* To tell the reader where to find a command in a menu, use a phrase like *in the **File** menu, select **Open**. 
Using angle brackets
* If you use angle brackets, follow these guides:
	* Put a non-breaking space (`&nbsp;`) before each angle bracket.	
	* Don't bold each menu name separately; instead, enclose the entire sequence in a single bold element. 	
	* Wrap the angle bracket with a span tag and add an `aria-label` attribute with *and then* text. Otherwise, some screen readers might read it as greater than.  For example:
	 `<span arial-label="and then">></span>`
	In the following example, the text renders as *Select **View > Tools > Developer Tools**. 
HTML:
	Select <b>View&nbsp;<span aria-label="and then">></span> Tools&nbsp;<span aria-label="and then">></span> Developer Tools</b>.
MD:
	Select **View&nbsp;<span aria-label="and then">></span> Tools <span aria-label="and then">></span> Developer Tools**.
	* This notation is useful for abbreviation a longer phrase like *in the **File** menu, select **Open**.*
	* This notation applies only to **menu items**. Don't use it to describe a combination of different UI elements.
	Recommended: 
	Select **MyApp>Preferences**, and then select the **Language** preference pane. 
	Not recommended: 
	Select **MyApp>Preferences>Languages>+>CSS**. 

##### Toolbar
* A toolbar is a set of buttons for common user actions. Refer to the toolbar by name if you think that the user needs help finding a button.
Recommended:
On the **Dashboard** toolbar, click **Edit**.
Recommended: Click **Edit**.

##### Buttons and icons
**Buttons**
* A button initiates an action when clicked or tapped, in the case of a touchscreen.
Recommended: Click **OK**. 
Not recommended: Click the "OK" button.
**Icon**
* An icon is a symbol or image that represents an object or a function. 
* An icon can be a button as well. 
* If the button includes an icon, write the name of the button as shown in the tooltip, and add the button icon before the name. 
Recommended: Click  **+** **Add**.
Not recommended: Click the **+** icon. 
* If a UI element name ends with an ellipsis(...), leave out the ellipsis. 
Recommended: Click **Browse**.
Not recommended: Click **Browse ...**.
* Don't use directional language to orient the reader, such as *above*, *below*, or *right-hand* side. Phrases like those don't work well for accessibility or for localization. 
* If a UI element is hard to find, provide a screenshot. 
Recommended: Click **#** **Menu**.
Not recommended: In the left-side panel, click the button with three lines. 

##### Tab (标签)
* A tab is a navigation element that looks like a file tab. To refer to a tab, use the form the `LABEL_NAME` tab. 
Recommended: Select **Tools > Options**, and then click the **Edit** tab. 

##### Text box
* A text box is a box that the use can type in, and use the `LABEL_NAME` box.
* Format the text by using the `<code>` in HTML or by using code formatting (monospace) in other markup. 
* In Google Cloud docutmentation, use *field* instead of *box*. 
Recommended: In the **Owner** box, enter your name. 

##### List box, combo box, and spin box
**List box**
* A list box is a box that offers the user a list of items. 
* To refer to a list box, use the form the `LABEL_NAME` list or the `LABLE_NAME` box. 
Recommended: In the **Item** list, select **Desktop**.
**Combo box**
* A combo box is a combination of a text box and a list box. 
* To refer to a combo box, use the form the `LABEL_NAME` box. 
* To refer to entering a value into a combo box, use the verbs *type* or *select* or *enter*. 
Recommended: 
In the **Font** box, type or select the font that you want to use.
**Spin box**
* A spin box is a box that lets the user choose a value by clicking arrows or by typing. 
* To refer to a spin box, use the form the `LABEL_NAME` box. 
* To refer to entering a value into a spin box, use the verb *enter*. 
Recommended: 
In the **Font size** box, enter a font size. 

##### Checkbox
* A checkbox is a small box that indicates whether an option is on or off. 
* To refer to a checlbox, use the form the `LABEL_NAME` checkbox. 
* Be wary of using the verbs *check* and *uncheck*, which can be ambiguous; It's often best to use *select* and *clear* instead. 
Recommended:
Select the **Automatically check for updates** checkbox. 
Recommended: Clear the **Bookmarks** checkbox. 

##### Radio button
* A radio button is a small button used to choose one item from a group of mutually exclusive options.
* To refer to a radio button, use the radio button's label, or refer to the group of buttons by it's label. 
Recommended:
Select **Do not remember passwords**.
Recommended:
Choose your preferred **Startup mode**. 

##### Expand arrow
* An expan arrow is the UI element used to expand or collapse a section of navigation or content. 
* Avoid referring to these explicitly in documenation, but when you do, use the terms *expander arrow* and *expandable section* rather than terms like *expando* or *zippy*. 
Recommended: To expand the **Advanced options** section, click the [arrow button] expander arrow. 
Not recommended; To expand the **Advanced options** section, click the zippy. 

##### Toggle
* A toggle is the UI element that switches back or forth between on and off states. 
* To refer to a toggle, can use the words of toggle as a verb. 
Recommended:
You can toggle Magic Mode in the **Settings** window. 
Recommended:
To enable the setting, click the Wi-Fi toggle. 

##### Pressing and typing keyboard keys
* To indicate that the user should press a given keyboard key or combination, use the `<kbd>` element.
Recommended: `Press <kbd>Control+C</kbd>.
* If you're working with non-HTM markup, use monospace formatting, which is how <kbd> renders. 
* In MD,  enclose the key name in backticks(`). 
* To refer to key that the user types to enter that key's value as text input, use the `<code>` element, not the `<kbd>` element. 
* To refer to a keyboard key, use the key's name. If that's ambiguous, use the form the `KEY_NAME` .
Recommended: Press `Esc`.
Recommended: Press the `Esc`key. 
* Spell out the name of modifier keys, such as Command, Control, Option, and Shift. To refer to a key combination, use the form `MODIFIER+KEY_NAME`.
* Don't use the symbols for those keys. 
* To refer to a key or combination that uses the Shift key, use the form `MODIFIER+SHIFT_KEY_NAME`. 
Recommended: Press `Control+Shift+?`.
* Spell out the name of characters that could be confusing in keyboard shortcut, such as comma, hyphen, period, and plus. 
* To refer to pressing a key or combination to cause an action to occur, use the verb *press*. 
* To refer to typing a key or combination as part of text, use the verb *enter* or *type*. 

##### Prepositions
* When documenting the UI, use the following prepositions. 
  | Preposition | UI element | Recommended |
  | ----------- | ---------- | ----------- |
  |in |dialogs, field, lists, menus, panes, windows, panes|In the **Alert** dialog, click **OK**. In the **Name** field, enter `wsfc-1`. In the **File** menu, click **Tools**.|
  |on|pages, tabs, toolbars|On the **Edit** tab, click **Save**. On the **Dashboard** toolbar, click **Edit**.|
  
##### Verbs in procedures
* To describe an action on the page, use the following verbs. 
	* Click
		* Use *click* not *click on*.
		Recommended: Click **OK**.
		Not recommended: Click on **OK**.
		Use hyphenate *right-click*, *left-click*, and doube-click.
	* Drag
		* Use drag, not *click and drag* and not *drag and drop*, although you can use drag-and-drop as an adjective. 
		Recommended: Drag the USER to the **Authorized** box. 
	* Enable
		* For turing on or activation an option or feature, use *enable* or *turn on*. 
		Recommended: To enable the API, click the toggle. 
		* For making it feasible to do something, use *lets you*.
		Recommended: The API lets you detect features in images.
			Not recommended: The API enables you detect features in images.		
			Not recommended: The API allows you detect features in images.			
	* Tap
		* Tap capacitive and on-screen buttons.				
	* Enter
		* Use to refer to the user entering text. 
		* *Type* is also okay.
		Recommended: In the **Owner** box, enter your name. 
			Recommended: In the **Size** box, type a font size. 		
	* Press
		* For mechanical button, use *press*.	 
	* Select
		* Use to describe choosing an item from among multiple options, selecting text, or marking a checkbox. 
		Recommended: Select **Automatically check for updates**.
		Not Recommended: Check  **Automatically check for updates**. 
        * Don't use *unselect*. Instead, use *clear* for checkboxes, and *deselect* for other UI elements. 
          Recommended; Clear **Automatically check for updates**.
          Not recommended: Deselect / Uncheck **Automatically check for updates**.	
	* Turn on, turn off
		* For turning on or activating an option or feature, use *turn on* or *enable* consistently between procedures and the surrounding text. 
		Recommended: To turn on Magic Mode, follow these steps. 
		Recommended: You can toggle Magic Mode in the **Setting** window. 

## HTML and CSS
### HTML formatting
The following are some basic guidelines, which apply to other documenation source files too, such as YAML and Markdown.
* Don't use tabs to indent text, use spaces only. 
* Indent by two spaces.
* Use all-lowercase for elements and attributes.
* Don't leave trailing spaces at the end of a line. 

## Names and naming
### Example domains and names
#### Example domain names 
* When you need a generic domain name in an example, use example.com, example.org, or example. net.

#### Example email addresses
* When you need a generic email address, use one of the domains listed in "Eample domain names"-for example, sara@example.com.

### Filenames and types
#### Types
Recommended: `avoiding-cliches.jd`
Recommended: `avoiding_cliches.jd`
Not recommended: `avoidingcliches.jd`
Not recommended: `avoidingCliches.jd`

#### Consistency
* If you're adding to a directory where everying else already uses underscores, and it's not feasible to change everything to hyphens, it's okay to use underscore to stay consistent. 
For example, if the directory already has `lesson_1.jd`, it's okay to add your new file as `lesson_4.jd` instead of `lesson-4.jd`. 

#### Other exceptions
* It's okay to have some inconsistency in filenames if it can't otherwise be avoided. For example, sometimes tools that generate reference documentation product filenmaes based on different sytle requirements or based on the design and naming conventions.

#### Referring to filenames
When referring to a specific file, do the following:

* Use code font. 
* Use the exact spelling of  the filename even if it doesn't follow naming guidelines. 
Recommended: In the following `build.sh` file, modify the default values for all parameters. 

#### Referring to file interactions
* When interacting with files and file types, don't use the file types as a verb. 
Recommended: Extract a zip file. 
Not recommended: Unzip a zip file. 

#### Referring to file types
* Use the formal name of the type. 
* Capitalize the file type name in all caps  bacause many file type names are acronyms or initialisms.
* Don't use the filename extension to refer to the file type. 
Recommended: a PNG file
Not recommended: a `.png` file
* The following tables lists exmples of filename extensions.
|Extension|File type name|
| -- | -- |
|.csv|CSV file|
|.exe|executable file|
|.gif|GIF file|
|.img|disk image file|
|.json|JSON file|
|.pdf|PDF file|
|.ps|PowerShell file|
|.py|Python file|
|.sh|Bash file|
|.sql|SQL file|
|.tar|tar file|
|.zip|zip file|

### Trademarks
#### Using trademarks as adjectives
Using a trademark term as an adjectives, never as a  noun or a verb. Whenever possible, a trademark should be followed by a common descriptive name (noun) of the product it modifies. For example, APPLE computer, TIVO digital video recorder. 

#### Possessives of trademarks
* Add 's to the end of the name. 
* Avoid forming a possessive with a product name, regardless of who owns the product name. 
Recommended: Google's new offfice is nearby.
Recommended: The capablities of Search are vast. 
Not recommended: Search's capablities are vast. 


















##### Description lists that use run-in headings 
**Run-in headings, the things like "Tip", "Note", etc.**
* Start each term or phrase with a capital letter. For the descriptions, start text that follows period with a capital letter, and text that follows colons with a lowercase letter. 
* End the introductory term or phrase with a period or colon. If a description follows a period, end the description with a period. If it follows a colon, depend on conditions, if it's a list of items or short phrases without verbs, don't include a period. Instead, use the month, quarter, or temperature (if relevant).
Recommended: 

#### Dimensions
* Use a lowercase *x*  between the numbers in the dimensions, with no space between the numbers and the *x*. 
Recommended: 192x192
Not recommended: 192 x 192

#### Exponents
* Don't use space between the base and the exponent. 
Recommended: 2<sup>3</sup>




















To find your API key(s), visit the Credentials page.
* Use second person.
* Use active voice.
* Use American spelling.
* Put conditional clauses before introductions, not after.
Not recommended: Click `Delete` if you want to delete the entire document.
Recommended:  To delete the entire document, click `Delete`.




## API documentation
* API documentation has traditionally included a brief explanation of REST. As knowledge of REST becomes more widespread, we might be able to assume that readers already know about it, and can remove those brief explanations.


