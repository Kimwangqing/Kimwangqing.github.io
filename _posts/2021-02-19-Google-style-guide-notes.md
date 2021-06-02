---
layout: post
title: "Google style guide notes"
date: 2019-04-17
excerpt: "Google style guide notes"
tags: Tech-writing
comments: true
---
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
* To refer to Google products as services, such as **the Google Kubernetes Engine services** or **the Compute Engine service*. However, if the term services leads to ambiguty, use the product names.

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

#### Capitalization in references to titles and headings
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

#### Commas seperating two independent clauses
When a coordinating conjunction (*and*, *but*, *or*, *nor*, *for*, *so*, or *yet*) separates two independent clauses, insert a comma after the first clause (before the conjunction) **unless both clauses are very short**.
Recommended: The libraries make feed creation easier, and they ensure that only valid feeds are produced. 
Not recommended: The libraries make feed creation easier and they ensure that only valid feeds are produced. 
Recommended: Type your ID and click **OK**.
Not recommended: Type your ID, and click **OK**. 

#### Commas seperating independent from dependent clauses
* When an independent clause and a dependent clause are separated by conjunction, insert a comma **only if the sentence could be misunderstood withoud one**. 
Recommended: Direct-access flags are plain variables and can be read directly. 
Not recommended: Direct-access flags are plain variables, and can be read directly.
Recommended: The manager acknowledged the last team member who entered the room, and started the meeting. 
Not recommended: The manager acknowledged the last team member who entered the room and started the meeting. 

#### Setting off other kinds of clauses
* To set off certain kinds of clauses with a comma or other punctuation for clarity. 
* A  couple of specific placeds where commas are a good idea. 
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
* For more decimal numbers, do not use any digit-group separators to the right of the decimal point.  
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

##### Numbered, lettered, and bulleted lists
* End each list item with a period or other appropriate sentence-ending punctuation, except in the following cases:
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

##### Description lists
* in general, don't add an explanatory phrase to only a single list items. Instead, use a description list, and provide explanation list, and provide explanatory phrases for all items. 
* In most contexts, start each term with a capital lette. 
* Don't end the term with a period. Do generally put a period at the end of each description element. 

Recommended:
The following words are adjectives:
**Big**
A short word.
**Relevant**
A fancy word
**Gratuitous**
A long word

Not recommended:
The following words are adjectives:
* Big
* Relevant
* Gratuitous

##### Description lists that use run-in headings 
**Run-in headings, the things like "Tip", "Note", etc.**
* Start each term or phrase with a capital letter. For the descriptions, start text that follows period with a capital letter, and text that follows colons with a lowercase letter. 
* End the introductory term or phrase with a period or colon. If a description follows a period, end the description with a period. If it followis a colon, depend on conditions, if it's a list of items or short phrases without verbs, don't include a period.          


#### Description lists
* Don't put a period at the end of a term
* Don't put a period at the end of description

#### Bulleted lists
* In general, use a period at the end of each item in a bulleted list. 
* Eexptions: single-word items, items entirely in code font, items with no verbs. 


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





























