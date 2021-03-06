# British Library Labs Symposium 2014 #
*Dissemination Event, British Library Conference Centre. London*

## Monday, 3 November 2014 ##

### Alternative Notetakers ###

James W. Baker, BL, https://gist.github.com/drjwbaker/fe66934864179ba7b401

### Keynote: Big Data, Small Data and Meaning: the conundrums of tool use in the humanities ###
Tim Hitchcock, Professor of Digital History, University of Sussex

#### Blurb ####
While 'big data' has grabbed the headlines in recent years, the creation of new digital tools has also changed how we undertake forms of 'close reading'. This talk will explore how 'big data' and 'close reading' can be more effectively integrated into a single research strategy that acknowledges the importance of seeing inherited culture both in detail - close up; and in context - at scale. It will also consider these methodological developments in light of the continuing importance of more traditional humanist theory.

#### Notes ####

[..in media res...]

+ We must remember the 'power of the particular' in macroscopic analyses
  + Big Data falls down when it fails to refocus
  + TH worries that we are losing our ability to see detail in a way that make Thompson et al so compelling. 

+ Humanities scholars should have self-confidence in their abilities
  + We can do certain things STEM scholars don't do very well
  + Close reading of a single datum
  + Big data supposedly let's you 'get away with dirty data'
  + We need tools to do a close reading of data that makes up big data
  
+ Radical conceptualisation
  + Understand the history and usage of a word so we can recognise when it is used in a way that is new or would look odd to contemporary readers
  + "Where is the tool to do that? Where is the project?"

### The Text to Image Linking Tool - winner of the British Library Labs 2014 competition ###
Desmond Schmidt, Research Scientist and Anna Gerber, Technical Project Manager of the University of Queensland

#### Blurb ####
Historical printed and manuscript material is often difficult to read and understand. Once digitised, researchers create detailed transcriptions, but making links between page images and the transcribed text is difficult and time-consuming. Desmond and Anna have been developing semi-automated techniques to build these links, to verify them, and to capture information that goes beyond text to include differences in lineation, type-size and line-spacing.

#### Notes ####

Background to the problem
+ Why link text to images
  + Library contain thousands of literary and historical texts
  + People expect to be able to access them on their ipads!
+ Digitisation is an obvious first step
  +'Bewildering' number of thumbnails
+ Can attach text to page image (on top)
  + OCR 
  + hard to fix errors
  + text can't be formatted / annotated
  + can search
+ Can put it side by side (page level)
  + Need to be synchronised
  + Lots of mental effort to move back and forth between formats / size / etc
+ Link at line level
  + Can't reflow
+ Word Level
  + Works even if hyphenated across lines

Manual Approach
+ Manually draw shapes around words
+ Link to text with mark up
+ Tedious, expensive
+ Markup too complex
+ Two transcriptions needed
  + One for links
  + One for formatting
  
Basic Idea of TILT
+ Find words in an image **without** recognising their content
+ Use and existing transcription of the page content
+ Link these two components mostly automatically
+ GeoJSON overlay links to image and transcription but not part of either

Method
+ Colour to greyscale
+ to Black and White
+ Find lines (can handle curves and slants)
+ Find words shapes (blobs of connected pixels with small gaps between them)
  + If you have 300 words, are the 299 biggest gaps the spaces?
+ link word-shapes to text

*Please don't have black vertical lines when digitising text!*

+ update anchors whenever words get out of alignment 
+ last resort: manually draw polygon around words

Questions:

Is your software available for integration into open-source projects like (wikisource)?
+ Yes, but without GUI it won't be that useful
  ++ They would want their own
+ Yes. They could go and do what they like with it.  GPL license on Github.

So good that you are doing this / disseminating this so we don't reinvent the world
+ Thanks. Would love to collaborate but disagreements about 'how' to do the program and how to present it. Most other projects doing this do it manually, which disagrees with
  
Could you look for signifiers like capital letters for word shapes?
+ Want to get away from OCR

How portable is this programme?
+ Doesn't matter about text language so long as you can have transcription in Unicode / plaintext / html
+ Graphical and backend separated so you can have just one or the other if you want.

Can it do vertical languages?
+ We haven't configured it yet, but it should work fine

Could it work with Thai (spaces / word shape)?
+ 'Thai scares me'

Can it recognise idiosyncrasies of handwriting?  
+ That isn't the problem we were trying to address but could be a future work (it's a good idea). There are other good handwriting scanners (transcriptorium project).  We would need 'sexier' polygons

Advice for OCR providers?
+ We were trying to avoid skewing / warping image to 'make it recognisable' but to work with it as it is, which may not work for OCR providers  

### Victorian Meme Machine ###
Bob Nicholson, Lecturer, Edge Hill University

#### Blurb ####
Bob will present the work he has been doing with Labs on the Victorian Meme Machine. What would it take to make a Victorian joke funny again? While the great works of Victorian art and literature have been preserved and celebrated by successive generations, even the period�s most popular jokes have now been lost or forgotten. Fortunately, thousands of these endangered jests have been preserved within the British Library�s digital collections. This project has begun to find these forgotten jokes and bring them back to life.

#### Notes ####

**Warning, presentation will contain Victorian jokes -- Some are really bad! You are under no obligation to laugh**

#### Background ####

Perception of Victorians as humourless is unfair
+ Jokes were everywhere
+ We tend to downplay that humour

Jokes help us understand
+ Slang
+ Dialect
+ Other conversational aspects of language lost in 'canon' literature

Using an interface to explore jokes that was not at all suitable (Sorry BL, have to agree!)
+ Wanted to create a way to do this batter

#### Initial Idea ####

+ Find a way to extract
+ Mark up with additional data
+ (experimental) Find a way to map that joke to a BL image
+ Package data together (mashup / meme machine)
  + Brilliant examples shown!  Annoy @digivictorian for his slides!
  
#### Stage One: Finding Jokes ####

+ Best sources are books and newspapers
  + Aim to get 1000000 jokes
  + 'The Book of Humour, Wit, & Wisdom: A Manual of Table-Talk
    + Manually extracted jokes
    + Hope for automatic in longer timescale
  + Newspaper joke columns
    + Regular, weekly column
    + 20-30 gags
    + Mostly reprints
    + Some changed title every week (very frustrating!)
    + XML for some databases have <ti> title element

#### Stage Two: Developing Transcriptions ####

+ Because we want to republish jokes, we need better than 80% correct
  + Knew we needed manually transcription / fixing
  + Used OMEKA (and student labour)
    + Scripto plug-in
    + Found it quicker to transcribe than fix OCR
      + MHB: My students say the same!
+ Tag linguistic aspects (for future research use)

#### Stage Three: Publishing ####

+ Still want image / speech bubbles but it will take time
+ Demonstrates mockup with Victorian Automaton / 'Devilish looking chap'
  + All use Flickr BL images
  + Random pairings new sources of comedy (benefit of mashups)
  + Now automated
  
#### Publication ####

+ http://www.VictorianHumour.tumblr.com
+ Mechanical comedian will tweet jokes at lunchtimes (@victorianhumour)

#### Track Use ####

+ Compare Victorian reprinting with modern retweeting / reuse (Please retweet!)
+ Data will go up on site

#### What's Next ####

+ Begin automatic joke publishing
+ Invite users to reinterpret (revive) jokes

--End of Lab Stage--

+ Hope to expand project
  + External funding / new partnerships
  + Expand and automate joke extraction
  + Implement a new transcription platform
  + Develop an accessible online research archive of Victorian joke
  + Continue to experiment with ways to publish / reinvent the jokes
    + Invite youtube collaboration?

#### The Big Picture ####

+ Repurposing data
  + We digitise for a particular purpose and then it gets locked in
  + Take the data we've got and use it in new ways
+ Remixing
  + Take two different sets of data and make them speak to each other in new and interesting ways
+ Gamification
  + Something that could be done on the iphone app
    + Transcribe and get reward of image (and kudos for improving data!)
+ Thanks to BL Labs 

Questions:

Suggestions:
 + Could people just read it in using speech to text? Would also provide voice-over
 + Stand-up Steam Punk Comedians 
 
Would the Victorians have found them funny or were they always groaners?
 + Reprint demonstrates they were popular

### Projects using British Library digital content and data ###

#### Blurb ####

The British Library Labs have been working with researchers around the world to enable them to make use of the Library's digital content / data; the session highlights some examples.

### Palimpsest: an Edinburgh Literary Cityscape ###
Dr Beatrice Alex, Research Fellow in Text Mining, School of Informatics, University of Edinburgh 

#### Blurb ####

We are creating a literary cityscape through text mining vivid, evocative and dramatic extracts of Edinburgh-based literary works from the early modern period to the twentieth century. Palimpsest enables users to explore the dimensions of literary Edinburgh through their encounters with geo-located extracts of literary works either via the web resource or in the city streets via a smartphone or tablet. The project is producing an interactive website and database of Edinburgh - based literary texts which is revealing a range of cityscapes that will newly engage scholars and the public with the urban environment and its literature.

#### Notes ####

Aim: To (text) mine Edinburgh's literature

+ Genesis was Edinburgh picturesque --- geolocated extracts
+ Had to decided what can be considered "Edinburgh-ness'; a small extract? A whole text? Places that no longer exist?
+ Extract from **Trainspotting** "First time I've been able to put swear words on an academic slide"
+ Sources
  + HathiTrust
  + British Library Nineteenth Century books collection
  + Gutenberg
  + Oxford Text ARchive
  + National Library of Scotland data
  + ECCO/EEBO
  + Limited set of copyrighted material if author/publisher agrees
+ Workflow: Digitised documents --> Filtering --> Manual curation --> Text mining (Geoparser / Edinburgh Gazetteer)--> relational database -> User interface
+ Big Data in, Small Data out
+ Tasks
  + Retrieve literary works
  + Devise a method for identifying 'loco-specificity'
  + Create a fine-grained location gazetteer for Edinburgh
+ FIRST though
  + Common format
  + Written English text
  + Post-corrected automatically
  + Linguistically preprocessed
+ Curation choices
  + No poetry
+ Point of text mining is always discovery
  + Did find a few new works
+ Gazetteer Creation
  + Need a local gazetteer by aggregating:
    + OpenStreet MAp
    + OS Locator
    + RCAHMS and Historical Scotland    
  + Literature on the Go App (map and text)
+ Human element really important to this sort of project

### Digital Music Lab: Analysing Big Music Data ###
Daniel Wolff, Research Fellow for the Digital Music Lab project at the Music Informatics Research Group, City University London and Adam Tovell, Curator, Digital Music, British Library

#### Blurb ####
The Digital Music Lab is developing research methods and software infrastructure for exploring and analysing large-scale music collections, and to provide researchers and users with datasets and computational tools to analyse music audio, scores and metadata. The team will present some of their initial findings including some startling visualisations.

#### Notes ####

+ In terms of mining, sound had always been more difficult technologically, but that is now changing
+ Aims:
  + Develop and evaluate music research methods for Big Data
  + Develop and infrastructure
  + Develop tools for large-scale computational musicology
  + Use and produce Big Music Data Sets
+ Visualisation tools exist but have largely been used for small scale projects
  + Beginning to have large scale: automatic identification etc
+ Musicology Research
  + Changes in performance
  + Influence of composer / artist
  + Relation to genre
+ Digital research combining musicology and music Informatics
+ Why the BL?
  + Over 3 million unique recordings
  + Wide ranging: popular, world and traditional music
  + Detailed metadata
  + Has legal framework for access
  + Also uses CHARM and ILikeMusic
+ Technical aspects that were wanted
  + Automatic analysis
  + Structural analysis
  + Analysing styles and trends over time
  + New similarity metrics (performance-based)
  + Work across different heterogeneous collections
    + ILikeMusic: Chord detection
    + CHARM: Instrumentation, MIDI-Scale transcription, High-res transcription
    + BL: Key detection ,Chord detect, speech/music detection
  + Utilise external metadata and annotations (MHB: yes! very important)
  + Processed over 1million pieces in 6 weeks
  + Visualisations of commonalities.  No C# chords in Blues?
+ Outputs
  + Web interface to make derived data available globally
  + Aims to be scalable, sustainable (open source) and reproducible
  
Questions:

Wouldn't you need contextual details to prove correlation / causation?
  + Yes.  But the output is to help you ask these questions (not provide answers) (MHB: DH is about asking interesting questions)
  

### Measuring the value of public domain data ###
Peter Balman , Software Developer and Winner of the Technology Strategy Board and British Library's Innovation Challenge (IC Tomorrow) -The value of public-domain data.

#### Blurb ####
Peter will talk about a tool he is developing that will proactively search for British Library's digital content on the web and give a detailed breakdown of where, how and by whom it is being used. Having visibility on this kind of data could help the BL make choices around targeting users by releasing similar content and encourage further use and deeper engagement within these groups.

#### Notes ####

Challenge is to encourage and establish the necessary feedback to measure the use and impact of public-domain content available through existing online platforms
+ What is the value to providers (such as BL)
+ What is value of making this data available to end-users

Metrics
+ Raw hits
+ Demographics or users
+ What do people talk about when they talk about using this data (sentiment analysis / natural language processing)
  + Social media useful (RT, favourites, likes)
  + Can be more abstract when talking about images

Example of the journey of an image to Burning Man, to be burned.  But also images of the images before during and after burning.

Possible Metrics?
+ Small Data Sets with research questions
+ Large Data Set (and hope for the best)

Workflow
+ Select image / collection
+ Visual representation of data crunching
+ Macro-->micro view to find 'interesting results'
+ Share socially (tweet function!)

Working on Now
+ Filtering by time, etc to help understand demographics and other information

(MHB: This was a very visual presentation, might be useful to search out twitter images or online slides)

When can you use it?
+ It is generally complete so institutions should feel free to contact.

Questions:

How are you actually finding uses?
+ Tin eye, some Google, Imageraider
  + Does it matter they aren't photographs
    + No, but does cause difficulty determining where they got it from (you or another source? use chronology....maybe)

How many 'interesting' examples will you find?  Won't most be boring uses?
+ Its about context around it as well as 'quality of reuse.

Any part of the project that considers whether the 'public domain'ness makes a difference?
+ Yes. Maybe. Don't know.  It doesn't have to be public domain images.

### The surprising tale of the mechanical curator and 1 million images ###
Mahendra Mahey, Manager and Ben O'Steen, Technical Lead of the British Library Labs

#### Blurb ####

The Labs team will tell the surprising story of one digital collection that the Library holds and how their work with it produced results no one expected, not even them! They will show how and - more importantly - why they created the �Mechanical Curator� and uploaded over a million illustrations taken from books onto Flickr. These images have stirred great interest from artists, researchers and the general public, garnering 200 million views and over 100,000 descriptive tags in under a year. The team will provide some examples of the creative and academic work that the collection has inspired as well as showing the impact the release has had.

#### Notes ####

Our audience is anyone, but primarily UK academia, with or without an idea before hand, looking at our data
+ Ideas can change (will change?) once you see, experiment with data or when you engage with BL staff.  
  + Wants to encourage this continually, not just in competition.
  
Who we work with?
+ Digital Scholarship
+ Project Board
+ Digital Research
+ Access & Reuse Group
+ Advisory Board
+ Curators / Researchers
+ Developers / Technical Staff
  + Get the last two groups in contact with Digital Content
  
Work with Access and Reuse Group
+ Internal group with BL to help provide data

Sifting through Collections
+ Digital but not online
+ Available on site only due to (c)
+ Available online in Reading Room due to (c)
+ Digital and online

Questions to ask:
+ Copyright cleared?
+ Curated (what is the story behind the collection, does person know it?!)
+ Metadata available?
+ Where is it?
+ Most is in Arts and Humanities
+ Lots of meetings in canteen (MHB: so, so true)


They'll give you data if you speak to them *and* feel professional obliged to speak to other groups about it (and tell them about it)  
(MHB: easy enough!)

Types of research being supported:
+ Research is changing because of digital
  + Data broken down, recombined and duplicated
+ A new breed of researcher
  + Open, networked, digital (MHB: Be kind, share!)
  
Interesting graph (by Ben from BL Labs) on intersection of humanities / technical skills in a person / collaboration

How to engage?
+ Competition
+ Events
+ Funding calls

Short-term project advantages
+ We have to be quick, agile
+ Major part of decision making
+ Reach the parts that other parts cannot
+ Do the things that others cannot
+ Be the bridge

We want to work with REAL researchers, not ideal/imaginary/phantom ones 

Building bridges with rapid depreciation :)
+ Build needed bridges now, not perfectionist ones..eventually or never

The unifying theme to most requests it
+ Give me EVERYTHING (that might be important to my work)
+ We need a toolset to figure out what this is

We could have given it out and said "here you go, let us know how it goes"
+ But better to make it really accessible and usable

Why can't we just use the catalogue?
+ If we really knew exactly what we wanted, we wouldn't be coming to them

How search engines work:
+ Stopwords are removed (common AND assumed unimportant) (MHB: Please let me not do this.  Stopwords are my friends!)
+ Word changed to roots
+ All assumed to have 'most relevant' not 'complete set'

Why not all the data that **might** be useful?
+ Subjective
+ But AI is developing quickly
  + Creepy story about Google 'good smiles'
  + Even creepier image of '16 sad women'

Digital corpus not reflective of physical (spikes are flattened): samplegenerator.cloudapp.net
+ The MARC data can be very useful.  It might just need to be rephrased. 

Just say 'use the API' isn't helpful.  Needs to be partnership of showing how and working with.

Tried an experiment of finding faces in 19th century with facial recognition software.  
+ People came and looked over his shoulder
+ So made a tumbler <http://mechanicalcurator.tumblr.com/archive>
+ Not that worried about 'stealing' as resolution was not great for printing on t-shirts
+ Some degree of machine learning (finding similar images)

Machine Learning 101:
+ Turn raw data into numbers
  + lines, shapes, offset
+ Process data
  + remove noise and tone variation
  + turning a grid of pixels into independent trackable 'pints of interest'
  + hues, saturation, contrast
+ Annotate (manually or automatically)
+ Pass through on of many machine learning algorithms such as Scalable Vector Machine
+ Testing
+ Use process on rest of data

Analysis starts with a bulk set of data, a set of assumptions and testing
+ No-one can support all assumptions and ideas! 

Why had no one done mechanical curator before?
+ Data was technically available
+ But a lot of hoops to find out 'if it was even interesting to you'
+ Put up on flickr (All in one go!)
  + 5 million visitors in first day
  + Crowdsourced tagging

Releasing is hard because you don't really always get back data on use...but that's okay.
+ Raw hits
+ Some engagement (tagging metrics)
+ Recooping loses?
  + If you didn't know there was value in it, you aren't losing anything

Crowdsourcing:
+ Metadata Games
+ Wikipedia Synoptic Index
+ BL Georeferencer
+ Scott Nicholson's RECIPE for Meaningful Gaminication

"If you knew where you were going at the start, It wouldn't be research. It would just be work" -- Ben
"Nothing in the world that motivates people to do things more than someone else doing it wrong" -- Ben

### What the Library has learned from the British Library Labs project and how it will be supporting Digital Scholars in the future ###
Adam Farquhar, Head of Digital Scholarship and Principal Investigator of the British Library Labs project

#### Blurb ####

Adam will highlight key lessons that we�ve learned working closely with researchers since the Labs were formed and discuss how the Labs is transforming our approach to providing services to support digital research and scholarship. He will also outline plans for the Labs over the coming years and give further details of the 2015 Competition. 

#### Notes ####

Readers and Digital Behaviours (2014 Survey on Digital Research Behaviour)
+ Demographics
  + Mostly taken by females, academics, and people in the Arts and Humanities
  + Most takers were from London, though 25% from outside UK, mainly North America
+ Changes since 2010 survey
  + 3x increase in feeling that British Library was 'very important' in digital research
  + 63% satisfied with services
    + want better remote access
    + better wifi 
    + better delivery to tablets / phones
+ Changes in behaviour
  + Device use
    + 2x laptops
    + 4x smart phones
    + 10x tablets
+ Research still mainly done on textual material, but others increasing
  + More non-textual material becoming available online
  + More interest in existing materials (especially 19th century)
+ Digital skills
  + 1 in 2 aware of data wrangling / scripting
  + 1 in 3 use text or data mining
  + 1 in 6 programme

General Behaviours
+ Most researchers worked alone
+ 2x increase in use of social media to dissemination or talk about findings
+ Print format remains most popular
+ 30% have work in a digital repository
  + 44% didn't know if they did
+ There was a high 'awareness' of copyright issues 
  + Did not check for 'correctness'
  
Digitisation
+ Not based on making a representative sample
  + funding (projects), conservation needs, unusual or non-canonical works
+ Why can't I have it all?
  + So much data that it would take 1 and a half years at 100 Mbs (dedicated standard) broadband to download it all (if you even had somewhere to put it)
  
BL Labs want to help in Building Skills
+ Digital Scholarship Training Programme
+ Catalogue of one-day courses

**Shoutout to Programming Historian**

Competitions
+ Big Data Experiment
  + Project with uCL, Microsoft and Bl
  + MSc students developed platforms to interrogate public domain digital collections

+ David Normal, **Crossroads of Curiosity**, display at Burning Man
+ Off the Map 2014
  + Gothuclus Rift: http://nixgamingdevblog.blogspot.co.uk
+ Off the Map 2015
  + Alice's Adventures
  
Lesson 1: More is More
+ Digital legal deposit legislation will begin soon
+ Digitisation continuing
  + Work with Google and Microsoft
  
Lesson 2: Less is More
+ Tools available from BL
  + Lots of internal / external conflict about the 'best way' to do something
  + Don't want to dictate but rather facilitate use of data; don't want to 'pick winners'
  + Wants to allow access for people to create own tools
  
Lesson 3:Bring Your Own Tools

Lesson 4: Let people be creative
+ We can't prescribe other people's workflows

Lesson 5: Support 'starting small, finishing big'
+ Develop technique on small scale with support
+ Encourage continuing development

### Sound making today and in the Victorian era ###
Sarah Angliss, composer, automatist and sound historian

#### Blurb ####

Sarah explores some unlikely affinities between sound making today and in the Victorian era. This will include references to the phonograph, ventriloquism, the learned pig and recordings held at the British Library. She will be available during the final reception in the Chaucer room to talk about the technology behind her creations and will host a special drop in D.I.Y session where you will be able to record your own voice on a wax cylinder using an original Edison phonograph, and hear how this 19th century sound recording equipment changes the way you sound.

#### Notes ####

This was a highly anecdotal, visual and auditory presentation. Notes would not do it justice.
____
#### Nota Bene

***This work is licensed under a Creative Commons Attribution 3.0 Unported License.***

<a rel="license" href="http://creativecommons.org/licenses/by/3.0/"><img alt="Creative Commons License" style="border-width:0" src="http://i.creativecommons.org/l/by/3.0/88x31.png" /></a>

***Taken Live and should not be considered a definative or complete record