---
layout: post
title: "IBM style guide notes"
date: 2019-04-17
excerpt: "IBM style guide notes"
tags: Tech-writing
comments: true
---
## Abbreviation 
### General usages
* Choose the indefinite article *a* or *an* before an abbreviation. 
* If can be plural, by adding a lowercase following an abbreviation. 
  `IDs` 
  
  >Microsoft: Microsoft Foundation Classes (MFC)
* For a unit of measurement, an abbreviation is both singular and plural.
  `1 mm`
* Do not use an abbreviation unless the sentence makes sense. 
  `PDFs for portable document formats. (incorrect)`
* Do not use abbreviation as verbs.
* Do not use an apostrophe ('s) to show the possessive form.
  `HTML's properties are editable.(incorrect)`
  `HTML properties are editable. (correct)`

### Spell out
* If an abbreviation is not commenly know, or if you are unsure whether it is commonly known, spell out the term as its first occurence in text, followed by the abbreviation in parenthese.
`minimum recovery time(MRT)`

### Do not capitalize initial letters
* Many spelled-out abbreviation do not require initial uppercase letters.
  `Graphical User Interface(GUI)(incorrect)`
  `graphical user interface(GUI)(correct)`
* Most language or protocol names have initial uppercase letters.
  `Hypertext Transfer Protocol(HTTP) 
  Wireless Applicaion Protocol(WAP)`
* Do not capitalize letters in the middle of a word to show the origin of an initialism. 
  `eXtensible markup language(XML)(incorrect)`
  `Extensible Markup Language(XML)(correct)`
  
> Microsoft 
  Don’t spell out the term
if the acronym is listed in The American Heritage Dictionary or if the A–Z word list says to use the acronym without spelling it out. If you’re sure your audience is familiar with an acronym, it’s OK to use it without spelling it out.

### Periods with abbreviations
* Omit period in uppercase abbreviations.
  `E.S.T.(incorrect)`
  `EST(correct)`
* Include periods in lowecase abbreviations that relate to time or that can be confused with words.
  `a.m.` `p.m.` `hr.` `yr.` `no.`
  Abbreviate units of time only when space is limited, such as in tables or in detailed diagrams.
When you must abbreviate units of time, use these abbreviations for both the singular and
plural forms and insert a period after them: sec., min., hr., d., mo., and yr.
* Omit periods in abbreviations for units of measurement, unless they can be confused with words.
  `b.p.s(incorrect)`
  `bps(correct)`
* Omit periods in abbreviations for academic degrees. 
  `BA` `PhD` `MA`
* Include periods in abbreviatons for social titles.
  `Dr.` `Ms.`
* If an abbreviation that requires a period occurs at the end of a sentence, do not include another period.
  `The meeting starts at 9:00 a.m..(incorrect)`
  `The meeting starts at 9:00 a.m.(correct)`

### Do not use latin abbreviations
Do not use Latin abbreviations, instead of using their English equivalents. 

Latin abbreviation|English equivalent
:-|:-
e.g.|use *"for example"*.
etc.|use *", and so on"*. `Monday, Tuesday, Wednesday, and so on.` Otherwise, rewrite the component to replace etc.with more descriptive, such as `, and other output`
i.e.|use *"that is"*.

### Abbreviation in titles and headings
* Avoid using abbreviations in headings and titles, unless an abbreviation is well known or the spelled-out form is too long. 
  `Creating Unified Modeling Language diagrams`
  `You can use Unified Modeling Language (UML) diagrams to model complex systems.`
  
  `Creating UML diagrams`
  `You can use Unified Modeling Language (UML) diagrams to model complex systems.`

  `Creating Unified Modeling Language (UML) diagrams`
 `You can use UML diagrams to model complex systems.`

### Abbreviation in glossaries
* For the abbreviation, provide a See reference that is the spelled-out term, and do not provide a definition. 
  `DBCS`
  See <u>double-byte character set</u>.
* For the spelled-out term, provide a definition, and do not provide a See reference to the abbreviation. Put the abbreviated term in parenthese after the spelled-out term.
  `double-byte character set (DBCS)`
A set of characters in which each character is represented by 2 bytes. These character sets are
commonly used by national languages such as Japanese and Chinese that have more symbols
than can be represented by a single byte.

## Anthropomorphism
Focus technical information on users and the actions that they perform, not on products and the actions that it performs. 
A product focus is acceptable in marketing content.
### Avoid a product focus
`The Delivery Information window allows you to specify the name of the sender.`
`This menu enables you to create diagrams.`

### Prefer a user focus
`In Delivery Information window, specify the name of the sender.`
`Use this menu to create diagrams.`

### Hardware and software can perform actions
Inanimate objects such as hardware and software can perform actions, and some verbs are appropriate for both people and things. For example, a program can search for a text string, or an application can read data from a file.
`The application asks you for a value.(anthropomorphic)`
`The application prompts you for a value.(appropriate verbs)`
`The control partition decides to switch roles.(anthropomorphic)`
`The control partition switches roles.(appropriate verbs)`

## Articles
* For file name extensions that begin with a period, such as `.exe`, the period is pronounced as *dot*, and use the indefinite article *a*.
  `a .test file`

  Use *a*|Consonant sound
:-|:-
historical|H, as in hit
LAN|L,as in land
one|W, as in won
unit|Y,as in you
x4|B, as in by four
** *u* begins with a consonant sound in unit, *u* begins  with a vowel sound, such as, sound as *a* in but and sound as *u:* in blue.**

  Use *an*|Vowel sound
:-|:-
HTTP|A, as in ache
LU|E, as in elf
MVS|E, as in empty
RPO|A, as in are
SQL|E, as in estimate

## Capitalization
In general, use a lowercase style in text and use sentence-style capitalization for headings.
Headings, captions, lables, or interface elements follow sentence-style capitalization or headline-style(标题式) capitalization. 
### Sentence-style capitalization
This style is predominantly lowercase; capitalize only the initial letter of the first word in the text and other words that require capitalization, such as proper
nouns. Examples of proper nouns include the names of specific people, places, companies, languages, protocols, and products.(专有名词也需要大写，但这里没说明是句式类大写还是标题类大写)
  `Requirements for Linux and UNIX operating systems`

In general, use sentence-style capitalization for headings.
* Figure captions
* Glossary definitions
  
### Headline-style capitalization
The following items use headline-style capitalization:
* Titles of books
* Titles of CDs
* Titles of stand-alone information units, such as information centers, quick start guides, and courses. 

In headline-style capitalization, capitalize the initial letter of the following words:
* The first and last words of the text 
* All nouns, pronouns, adjectives, verbs, adverbs, and subordinating conjunctions（从属连词）, such as *after*, *although*, *because*, *before*, *how*, *if*...
* Any word in a hyphenated compound that is not an article, preposition, or coordinating conjunction

Do not capitalize the initial letter of the following words:
* Articles, except as the first word
* Coordinating conjunctions, such as, *and*, *but*, *or*
* Prepositions, exccept as the first or last word
* The *to* in an infinitive（不定式）
`Variables to Be Determined by the Program`

#### Subtitle in a headline-style title
* Use headline-style capitalization for a subtitle that is displayed on the same line as the title, is short, or is essential to the title.
• Use sentence-style capitalization for a subtitle that is displayed separately from the title, is lengthy, or is supplementary to the title.

### Capitalization in glossary
* Use lowercase for glossary terms unless a proper noun or other reasons. 
* Use sentence-style capitalization for glossary definitions.

### Capitalization in indexes
Use lowercase for index terms a term is a proper noun or for other reasons.

### Capitalization in interfaces
#### Sentence-style capitalizaion
* Check box labels
* Field labels -[1](#ftnote1 "ftnote1")
* Group box labels -[2](#ftnote2 "ftnote2")
* Hover help running text -[3](#ftnote3 "ftnote3")
* List box entries -[4](#ftnote4 "ftnote4")
* Messages
* Navigation links
* Radio button labels -[5](#ftnote5 "ftnote5")
* Status bar text -[6](#ftnote6 "ftnote6")
* Web page titles and web navigational elements

#### Headline-style capitalization
* Button labels
* Column headings -[7](#ftnote7 "ftnote7")
* Icon labels
* Manu name and manu items -[8](#ftnote8 "ftnote8")
* Palette titles -[9](#ftnote9 "ftnote9")
* Portlet titles -[10](#ftnote10 "ftnote10")
* Tab titles -[11](#fnote11 "ftnote11")
* Toolbars and toolbar button labels
* Tooltip labels
* Window titles

### Capitalization and abbreviations
Many spelled-out abbreviations do not require initial uppercase letters.
`Graphic User Interface(GUI)(incorrect)`
`graphic user interface(GUI)(correct)`

Most spelled-out form of language and protocol names have initial uppercase letters.
`Hypertext Transfer Protocol(HTTP)`
`Unified Modeling Language(UML)`

But, do not capitalize letters in the middle of a word to show the origin of an initialism.
`eXtensible markup language(XML)(incorrect)`
`Extensible Markup Language(XML)(correct)`

### Capitalization and hyphens
* When a hyphenated word occurs at the **beginning of a sentence**, capitalize only the first element in the word unless a subsequent element is a proper noun or proper adjective.
`Power-Saving techniques are important for notebook users.(incorrect)`
`Power-saving techniques are important for notebook users.(correct)`
*  When a hyphenated word occurs at the **beginning of a heading with sentence-style capitalization**, capitalize only the first element in the word unless a subsequent element is a proper noun or proper adjective.(当一个带连字符的单词出现在标题的开头并带有句子风格的大写时，只将单词中的第一个元素大写(无论它是不是专有名词），但如果后面有专有名词或专有形容词，该专有名词或专有形容词使用大写。)
  `Case-Sensitive languages...(incorrect)`
  `Case-sensitive languages...(correct)`
* When a hyphenated word occurs **in a heading with headline-style capitalization**
* , capitalize the first element in the word; the last element in the word, regardless of its part of speech; and any element that is not an article, preposition, or coordinating conjunction.（当带连字符的单词出现在标题中，并带有标题式大写时，请将单词中的第一个元素以及单词的最后一个元素（除非是冠词、介词或并列连词）不论其词性都大写。）
`Designing Interfaces for Non-English-speaking Users (incorrect)`
`Self-contained Sensors (incorrect)`
`Once-a-day Notifications (incorrect)`
`Designing Interfaces for Non-English-Speaking Users (correct)`
`Self-Contained Sensors (correct)`
`Once-a-Day Notifications (incorrect)`
  
### Capitalization and colons
In general, use a lowcase letter on the text that immediately follows a colon.
`Three security measures are evaluated: a firewall, an encryption key, and a password.`

Use an uppercase in the following items:
* Item in a vertical list
  `You can use the following background colors:`
  `. Blue`
  `. Green`
* Note 
  `CAUTION: Do not remove or install this unit without using the provided lift tool.`
  `Error: An incorrect value was entered.`
* Proper noun
  `You can use the following languages: Jave, C, and C++.`
* Quotation
  `The manager's instrutions were clear:"Submit the report by Monday."`
* Subheading on the same line as a heading
  `Input/output operations: Move mode and locate mode`
  
### Letters capitalization
* Use the capitalization for the letter that appears in the begining or the middle or the end of words that is appropriate for the context, which means use the capitalization if the original words are capitalized, and use lowercase letters if the original words are lowercase letters.
 `The H in HTML stands for Hyertext.`
 `Double the letter m in the word programming.`
* If you refer t a letter and the capitalization is irrelevant, use an uppercase letter.
 `Beginner typists often mistype P's and Z's.` 

### Do not use uppercase letters for the follows
* Do not use uppercase letters for emphasis.
Do Not change the default settings.(incorrect)
**Important:** Do not change the default settings.(corrtect)
* Do not create terms with internal uppercase letters.
`CopyPool (incorrect)`
`Copy pool (correct)`
* Do not capitalize the names of features and components unless they are sold seperately(单独了售) or are trademarkded.
`Open the Table Partitioning feature. (incorrect)`
`Opne the table partitioning feature. (correct)`
* Do not capitalize collective（集合名词） or generic term (总称)
`The Dispatcher (发报机)(incorrect)`
`The dispatcher (correct)`
`The Paging Supervisor (incorrect)`
`The paging supervisor (correct)`

### Do not start a sentence with a lowcase term
Do not start a sentence with a lowcase term, if so, rewrite the sentence.
`if expressions, unlike if statements, return a value.(incorrect)`
`Unlike if statements, if expressions return a value.(correct)`

## Prepositions
* Include prepositions to increase clarity.
 `Unload the file using the ULOAD utility.(ambiguous)`
 `Unload the file by using the ULOAD utility.(clear)`
* Omit unnecessary prepositions. For example, when the verb alone is more clear than the prepostions in phrasal verbs （动词短语）.
 `click is more clear than click on.`
 `start is more clear than start up.`
* Avoid using too many propositions. Too many prepositions can clutter the text.
 `The report is a list of the status of all of the event monitors for this process.(awkward)`
 `The report lists the status of all event monitors for this process.(improved)`
* Use a prepostion at the end of a sentence to avoid an awkward or stilted（呆板的）constructions.
 `Click the item for which you want to search.(awkward)`
 `Click the item that you want to search for.(improved)`
* Use a prepostion instead of an apostrophe（撇号）and the letter *s ('s)* to show the possessive form of abbreviations, brand names, product names, or inanimate objects.
 `The GUI's layout is intuitive.(incorrect)`
 `The layout of the GUI is intuitive.(correct)`
 `Use Rational&reg; Software Architect's views to model systems or applications.(incorrect)`
 `Use the views in Rational&reg; Software Architect to model systems or applications.(correct)`
 `Edit the object's properties.(incorrect)`
 `Edit the properties of the object.(correct)`

## Pronone
### Avoid ambigrous pronoun references
Ensure that the noun to which a pronoun refer is clear. Avoid a sentence in which a pronoun can refer to more than one noun or in which a pronoun refer to an unstated noun,
`Maria told Susan that her report was late.(two persons can be referred)`
`Maria told Susan that Susan's report was late.(correct)`
`If the field is populated with default text(如果字段充满了默认文本）, it does not change.(anbiguous pronoun)`
`If the field is populated with default text, the text does not change.(correct)`
`Back up the files weekly. This is imortant for several reasons.(unstated noun)`
`Back up the files weekly. This practice is important for several reason.(correct)
`
### Avoid gender-specific pronouns
Many terms, such as *customer engineer*, *programmer*, or *administrator*, do not apply gender-specific pronouns to one gender, such as *he*, *her*, *himself* unless the person you refer to is male or is female.

Use these techniques to avoid gender-specific pronouns:
* Use the imperative mood（祈使句）.
 `The operator should turn the blue switch on her right to Remote.(incorrect)`
 `Turn the blue switch on the right to Remote.(correct)`
* Use the second person: *you*, *yourself*, or *yours*.
 `The user can now move his cursor in four directions.(incorrect)`
 `You can now more your cursor in four directions.(correct)`
* Use plural nouns and pronouns: *they*, *their*, *them*, *theirs*, or *themselves*.
 `A customer engineer must be trained on the hardward that he services.(incorrect)`
 `Custumer engineers must be trained on the hardward that they service.(correct)`
* Do not use combine pronouns.
  Incorrect: `he or she`, `he/she`, `him or her`, `him/her`...
* Do not use a singular noun and a plural pronoun.
 `Each employee is expected to clean their work areas before they go home.(incorrect)`
 `All employees are expected to clean their work areas before they go home.(correct)`

### Personal pronouns
Follow these guidelines for personal pronouns:
* Avoid the first-person pronouns, such as *I* and *we*, except in these situations:
  * In the questions of frequently asked questions(FAQs)
  * In articles（论文）, white papers or documents that have listed authors and in which the authors describe their own opinions.
* Use the second-person pronoun or the subject of a imperative sentence can be understood.
* Avoid third-person pronouns that are generic-specific（可以用第三人称复数，这样不会有特指）.

### Relative pronouns （关系代词）
* Use *that*, without a comma, to introduce a restrictive clause that is essential to the meaning of the sentence; if the clause is removed, the meaning of the sentence changes.
` The system units that have two drives installed are floor-standing models（落地式）.`
In the restrictive example, some system units have two drives, and some do not. Only the units that have two drives installed are floor-standing model.
* Use *which*, preceded by a comma, to introduce a nonrestrictive clause that is parenthetical（补充说明的） to the meaning of the sentence; if the clause is removed, the meaning of the sentence does not change.
` The system units, which have two drives installed, are floor-standing models.`
In the nonrestrictive example, all the system units are floor-standing models, and they all have two drives installed.
* Use *who*, not *that* or *which*, to refer to a person. Use *whose* with both animate and inanimate objects. 
`Database administrators that require additional information...(incorrect)`
`Database administrators who require additional information...(correct)`

##Spelling
Use US English spelling in all pubications.
`colour (British)`
`color (US)`
`metre (British)`
`meter (US)`
`programme (British)`
`program (US)`
`organise (British)
`organize (US)`

If certain publications are distributed in regions that use UK English, decide which spelling is appropriate.

### General guidelines
* Avoid using words that primarily function as verbs to be nouns or adjectives include *configure*, *compile*, *debug*, *fix*, and *install*.
 `during the install (incorrect)`
 `during the installation (correct)`
 `the debug function (incorrect)`
 `the debugging function (correct)`
* Avoid using a phrasal verb (a verb combining with a proposition) if the verb alone provides the same meaning.
 `click instead of click on`
 `print instead of print out`
 `start instead of start up`
* Do not omit the verb from the second clause in two coordinate clauses.
 `The file names are displayed in uppercase characters and the other flle attributes in lowercase characters. (incorrect)`
 `The file names are displayed in uppercase characters, and the other file attrubutes are displayed in lowercase characters. (correct)`
* Avoid using a dangling modifier (无明确对象的修辞语) by using a present participle or a past paticiple at the begining of a sentence.
 `Having configured your environment, the program is ready to be used. (incorrect)`
 `After you have configured your environment, the program is ready to be used. (correct)`

### Mood
* Use the imperative mood for instructions, such as in procedures.
 `Select one or more check boxes.`
 `Before you install the product, back up your files.`
* Do not use subjunctive mood in technical documentation.
 `It is important that the file be saved... (incorrect)`
 `Important: Save the file... (correct)`
 `If you were to save the file... (incorrect)`
 `If you save the file... (correct)

### Person

#### First person
* Avoid using first person. The first person focuses on the writer, not on the reader or the information being presented.
* The use of first person is acceptable in the following situations:
 * In FAQs.
 * In articles, white papers, or document that have listed authors and in which the authors describe their own options.

#### Second person
* Use sencond person ss much as possible. The second person focuses on the reader.
`When you create a database, you must provide a unique name.`
* Use the imperative mood, when instruct the user to perform an action. 
 `Press Enter to begin processing.`

#### Third person
* Use the third person to describe concepts, facts, and results. The third person focuses on the information being presented. 
`Specify whether users can add themselves to a project.`
* Do not use gender-specific pronouns, such as *she*, *he*, unless the context requires them.

### Tense
* Use the simple present tense as much as possible.
 `When you open the latch, the panel will slide forward. (incorrect)`
 `When you open the latch, the panel slides forward. (correct)`
* Use the past or future tense when you cannot use the present tense or it does not make sense to use the present tense.
 `If you selected New in the previous window, the current window will display the recommended default values. (incorrect)`
 `If you selected New in the previous window, the current window displays the recommended default values. (correct)`
 `Cancel a broker deployment only if you are sure that the broker never responds to the deployment request. (incorrect)`
 `Cancel a broker deployment only if you are sure that the broker will never respond to the deployment request. (correct)

### Voice
* Use active voice as mucu as possible. Active voice focuses on the performer of the action. 
 `The limits window is used to specifiy the minimum and maximum values. (passive)`
 `In the limits window, specify the maximum and minimum values. (active)`
* Passive voice is acceptable when the following conditions:
 * The systme perform the action.
 * It is more appropriate to focus on the receiver of the action.
    `The file is saved when you press Enter.`
 * It is more appropriate to avoid blaming the user for an error, such as in an error message.
    `Error: An incorrect value was entered.`

---

<a id="ftnote1">1 字段标签（Field labels）: it is the text portion of the field that appears between the double chevrons(《》). It is a tab in the Data Element level, when you create a data element, there is a tab for Field Label, where you can specify the Long text, Medium text, Short text for that data element. ![](img/fieldlabels.png)</a>

<a id="ftnote2">2 组框标签（Group box labels）: 用于包含一组同类型的对象，可根据查看需要作收缩或者展开的一个框对象，并可以设置标题信息。 如图: ![](img/groupboxlabels.png)</a>

<a id="ftnote3">3 悬停提示文本（Hover help running text）

<a id="ftnote4">4 列表框（ListBox）用于提供一组条目（Enties 数据项），用户可以用鼠标选择其中一个或者多个条目，但是不能直接编辑列表框的数据。当列表框不能同时显示所有项目时候，他将自动添加滚动条，使用户可以滚动查阅所有选项。</a>

<a id="ftnote5">5 单选按钮标签(Radio button labels)</a>

<a id="ftnote6">6 状态栏文本(Status bar text) ![](img/statusbar.png)</a>

<a id="ftnote7">7 列标题(Column headings) ![](img/columnheadings.png)</a>

<a id="ftnote8">8 菜单和菜单项(menu items) ![](img/menuitems.png)</a>

<a id="ftnote9">9 调色板标题(palette items)

<a id="ftnote10">10 Portlets: 是一种Web组件，就像 servlets 是专为将合成页面里的内容聚集在一起而设计的。通常请求一个 portal 页面会引发多个 portlets 被调 用。每个 portlet 都会生成标记段，并与别的 portlets 生成的标记段组合在一起嵌入到 portal 页面的标记内。

<a id="ftnote11">11 选项卡标题(Tab titles)
